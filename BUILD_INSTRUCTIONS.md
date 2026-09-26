# Build Instructions for WhAlert

This document provides instructions for building the WhAlert Android application locally.

## Prerequisites

### Required Tools

1. **Android Studio** (latest stable version)
   - Download: https://developer.android.com/studio
   - Recommended: Android Studio Giraffe or newer

2. **Java Development Kit (JDK)**
   - Version: JDK 17 or higher
   - Download: https://www.oracle.com/java/technologies/javase/jdk17-archive-downloads.html
   - Or use OpenJDK: https://adoptium.net/

3. **Android SDK**
   - SDK Platform: Android 14 (API 34)
   - SDK Tools: Android SDK Build-Tools, Android Emulator
   - Minimum SDK: Android 7.0 (API 24)

4. **Gradle**
   - Version: 8.3 or higher (included with Android Studio)

### System Requirements

- **Operating System**: Windows 10/11, macOS 10.15+, or Linux
- **RAM**: 8GB minimum (16GB recommended)
- **Storage**: 10GB free disk space
- **Internet Connection**: Required for downloading dependencies

## Setup Instructions

### 1. Clone the Repository

```bash
# Clone the repository
git clone https://github.com/mamadoubdoumbia9-sudo/My-room.git
cd My-room/WhAlert

# Check out the main branch (if not already)
git checkout main
```

### 2. Open in Android Studio

1. Launch Android Studio
2. Select "Open an Existing Project"
3. Navigate to the `WhAlert` directory
4. Click "OK" to open the project

### 3. Configure the Project

Android Studio will automatically:
- Download required Gradle dependencies
- Sync the project
- Index the files

If prompted:
- Accept the default Gradle settings
- Allow Android Studio to download missing SDK packages

### 4. Configure Signing (Optional for Debug)

For debug builds, no signing configuration is needed.

For release builds, you need to set up a signing key:

1. Create a keystore file (or use an existing one):
   ```bash
   keytool -genkey -v -keystore whalert_keystore.jks \
     -alias whalert_key \
     -keyalg RSA \
     -keysize 2048 \
     -validity 10000
   ```

2. Place the keystore file in the `app` directory

3. Update `app/build.gradle.kts` with your keystore details:
   ```kotlin
   signingConfigs {
       create("release") {
           storeFile = file("whalert_keystore.jks")
           storePassword = System.getenv("WHALERT_STORE_PASSWORD") ?: "your_store_password"
           keyAlias = System.getenv("WHALERT_KEY_ALIAS") ?: "whalert_key"
           keyPassword = System.getenv("WHALERT_KEY_PASSWORD") ?: "your_key_password"
       }
   }
   ```

### 5. Configure Firebase (Optional)

WhAlert uses Firebase for authentication and data storage. To enable Firebase features:

1. Create a Firebase project at https://console.firebase.google.com/

2. Add an Android app to your Firebase project:
   - Package name: `com.whalert.app`
   - SHA-1 fingerprint: Get from your keystore or debug keystore

3. Download the `google-services.json` file

4. Place the file in the `app` directory

5. Enable the following Firebase services:
   - Authentication (Email/Password)
   - Firestore Database
   - Storage

## Building the App

### Debug Build

To build a debug APK:

```bash
# Using Android Studio
# - Click "Build" > "Build Bundle(s) / APK(s)" > "Build APK"

# Using Gradle command line
./gradlew clean assembleDebug
```

The debug APK will be generated at:
```
app/build/outputs/apk/debug/app-debug.apk
```

### Release Build

To build a release APK:

```bash
# Make sure you have configured signing (see step 4 above)
./gradlew clean assembleRelease
```

The release APK will be generated at:
```
app/build/outputs/apk/release/app-release.apk
```

### Bundle Build (for Google Play)

To build an Android App Bundle:

```bash
./gradlew clean bundleRelease
```

The bundle will be generated at:
```
app/build/outputs/bundle/release/app-release.aab
```

## Running the App

### On an Emulator

1. Create an Android emulator in Android Studio:
   - AVD Manager > Create Virtual Device
   - Select a device (e.g., Pixel 6)
   - Select a system image (Android 14 or higher)
   - Finish and start the emulator

2. Run the app:
   ```bash
   ./gradlew installDebug
   ```

Or use Android Studio:
- Click "Run" > "Run 'app'"
- Select the emulator
- Click "OK"

### On a Physical Device

1. Enable USB debugging on your device:
   - Settings > About phone > Tap "Build number" 7 times
   - Settings > Developer options > Enable "USB debugging"

2. Connect your device to your computer via USB

3. Run the app:
   ```bash
   ./gradlew installDebug
   ```

Or use Android Studio:
- Click "Run" > "Run 'app'"
- Select your device
- Click "OK"

## Running Tests

### Unit Tests

To run all unit tests:

```bash
./gradlew testDebugUnitTest
```

To run a specific test class:
```bash
./gradlew testDebugUnitTest --tests "com.whalert.app.PhoneNumberValidatorTest"
```

### UI Tests

To run Android instrumentation tests:

```bash
# Connect a device or start an emulator first
./gradlew connectedDebugAndroidTest
```

## Troubleshooting

### Common Issues

#### 1. Gradle Build Failed

**Error**: `Could not find com.android.tools.build:gradle:8.3.0`

**Solution**: Update Gradle in Android Studio:
- File > Settings > Build, Execution, Deployment > Build Tools > Gradle
- Check "Use Gradle from:" and select "gradle-wrapper.properties file"
- Click "OK" and sync the project

#### 2. SDK Not Found

**Error**: `Failed to find Platform SDK with path: platforms/android-34`

**Solution**: Install the required SDK:
- Tools > SDK Manager
- Select "Android 14 (API 34)" under SDK Platforms
- Click "Apply" and "OK"

#### 3. Java Version Error

**Error**: `Unsupported class file major version 61`

**Solution**: Make sure you're using JDK 17 or higher:
- File > Project Structure > SDK Location
- Select JDK 17 or higher
- Click "OK"

#### 4. Out of Memory

**Error**: `Out of memory: Java heap space`

**Solution**: Increase Gradle memory:
- Edit `gradle.properties` file
- Add or update:
  ```properties
  org.gradle.jvmargs=-Xmx4096m -Dfile.encoding=UTF-8
  ```
- Sync the project

#### 5. Firebase Configuration Missing

**Error**: `File google-services.json is missing`

**Solution**: 
- Either add the Firebase configuration file (see step 5 above)
- Or remove Firebase dependencies if you don't need them

### Clean Build

If you encounter persistent issues, try a clean build:

```bash
./gradlew clean
./gradlew cleanBuildCache
./gradlew assembleDebug
```

### Invalidate Caches

In Android Studio:
- File > Invalidate Caches / Restart > Invalidate and Restart

## Project Structure

```
WhAlert/
├── app/                          # Main application module
│   ├── src/
│   │   ├── main/                 # Production code
│   │   │   ├── java/com/whalert/app/
│   │   │   │   ├── data/           # Data layer
│   │   │   │   ├── di/             # Dependency injection
│   │   │   │   ├── domain/         # Domain layer
│   │   │   │   ├── presentation/   # UI layer
│   │   │   │   └── util/           # Utility classes
│   │   │   └── res/               # Resources
│   │   └── test/                 # Unit tests
│   └── build.gradle.kts           # App module build file
├── build.gradle.kts              # Project build file
├── settings.gradle.kts           # Project settings
├── gradle.properties             # Gradle properties
└── README.md                     # Project documentation
```

## Configuration Options

### Changing Application ID

To change the application ID (package name):

1. Update `app/build.gradle.kts`:
   ```kotlin
   android {
       defaultConfig {
           applicationId = "com.yourcompany.whalert"
       }
   }
   ```

2. Update `AndroidManifest.xml`:
   ```xml
   <manifest package="com.yourcompany.whalert">
   ```

### Changing Version

To change the app version:

1. Update `app/build.gradle.kts`:
   ```kotlin
   android {
       defaultConfig {
           versionCode = 2
           versionName = "1.0.1"
       }
   }
   ```

### Changing Minimum SDK

To change the minimum SDK version:

1. Update `app/build.gradle.kts`:
   ```kotlin
   android {
       defaultConfig {
           minSdk = 21  // Change to your desired minimum
       }
   }
   ```

### Disabling Firebase

If you don't want to use Firebase:

1. Remove Firebase dependencies from `app/build.gradle.kts`
2. Remove Firebase plugins from the top-level `build.gradle.kts`
3. Remove Firebase-related code from the app
4. Remove `google-services.json` file

## Continuous Integration

For setting up CI/CD, you can use:

### GitHub Actions

Create a workflow file `.github/workflows/android.yml`:

```yaml
name: Android CI

on:
  push:
    branches: [ main ]
  pull_request:
    branches: [ main ]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@v3
    
    - name: Set up JDK 17
      uses: actions/setup-java@v3
      with:
        java-version: '17'
        distribution: 'temurin'
    
    - name: Build with Gradle
      run: ./gradlew clean assembleDebug
    
    - name: Run Unit Tests
      run: ./gradlew testDebugUnitTest
    
    - name: Upload APK
      uses: actions/upload-artifact@v3
      with:
        name: app-debug
        path: app/build/outputs/apk/debug/app-debug.apk
```

### Bitrise

For more advanced CI/CD, consider using Bitrise with Android support.

## Additional Resources

- [Android Developer Documentation](https://developer.android.com/docs)
- [Jetpack Compose Documentation](https://developer.android.com/jetpack/compose)
- [Firebase Documentation](https://firebase.google.com/docs)
- [Gradle Documentation](https://docs.gradle.org/)

## Support

If you encounter issues not covered in this document:

1. Check the [README](README.md) for general information
2. Check the [FAQ](README.md#faq) for common questions
3. Create an issue in the repository with details about your problem

## License

By building and using WhAlert, you agree to the [MIT License](LICENSE).
