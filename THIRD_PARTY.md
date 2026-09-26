# Third-Party Libraries

This document lists all third-party libraries used in WhAlert, along with their licenses and versions.

## AndroidX Libraries

| Library | Version | License | Usage |
|---------|---------|---------|-------|
| androidx.core:core-ktx | 1.12.0 | Apache License 2.0 | Core Kotlin extensions |
| androidx.appcompat:appcompat | 1.6.1 | Apache License 2.0 | AppCompat support |
| com.google.android.material:material | 1.11.0 | Apache License 2.0 | Material Design components |
| androidx.constraintlayout:constraintlayout | 2.1.4 | Apache License 2.0 | ConstraintLayout support |
| androidx.lifecycle:lifecycle-runtime-ktx | 2.7.0 | Apache License 2.0 | Lifecycle components |
| androidx.lifecycle:lifecycle-viewmodel-compose | 2.7.0 | Apache License 2.0 | ViewModel for Compose |
| androidx.lifecycle:lifecycle-runtime-compose | 2.7.0 | Apache License 2.0 | Lifecycle for Compose |
| androidx.activity:activity-compose | 1.8.2 | Apache License 2.0 | Activity Compose integration |
| androidx.compose.ui:ui | 1.5.4 | Apache License 2.0 | Jetpack Compose UI |
| androidx.compose.material3:material3 | 1.2.0 | Apache License 2.0 | Material 3 Compose components |
| androidx.compose.ui:ui-tooling-preview | 1.5.4 | Apache License 2.0 | Compose tooling preview |
| androidx.compose.material:material-icons-extended | 1.5.4 | Apache License 2.0 | Material icons |
| androidx.navigation:navigation-compose | 2.7.7 | Apache License 2.0 | Compose Navigation |
| androidx.room:room-runtime | 2.6.1 | Apache License 2.0 | Room database |
| androidx.room:room-ktx | 2.6.1 | Apache License 2.0 | Room Kotlin extensions |
| androidx.room:room-compiler | 2.6.1 | Apache License 2.0 | Room annotation processor |
| androidx.security:security-crypto | 1.1.0-alpha06 | Apache License 2.0 | Security crypto |

## Kotlin Libraries

| Library | Version | License | Usage |
|---------|---------|---------|-------|
| org.jetbrains.kotlin:kotlin-stdlib-jdk7 | 1.9.20 | Apache License 2.0 | Kotlin standard library |
| org.jetbrains.kotlinx:kotlinx-coroutines-android | 1.7.3 | Apache License 2.0 | Coroutines for Android |
| org.jetbrains.kotlinx:kotlinx-coroutines-core | 1.7.3 | Apache License 2.0 | Coroutines core |

## Network Libraries

| Library | Version | License | Usage |
|---------|---------|---------|-------|
| com.squareup.retrofit2:retrofit | 2.9.0 | Apache License 2.0 | HTTP client |
| com.squareup.okhttp3:okhttp | 4.12.0 | Apache License 2.0 | HTTP client |
| com.squareup.okhttp3:logging-interceptor | 4.12.0 | Apache License 2.0 | HTTP logging |
| com.google.code.gson:gson | 2.10.1 | Apache License 2.0 | JSON serialization |
| com.squareup.retrofit2:converter-gson | 2.9.0 | Apache License 2.0 | Gson converter for Retrofit |

## Firebase Libraries

| Library | Version | License | Usage |
|---------|---------|---------|-------|
| com.google.firebase:firebase-bom | 32.7.0 | Apache License 2.0 | Firebase BOM |
| com.google.firebase:firebase-analytics-ktx | 32.7.0 | Apache License 2.0 | Firebase Analytics |
| com.google.firebase:firebase-auth-ktx | 32.7.0 | Apache License 2.0 | Firebase Authentication |
| com.google.firebase:firebase-firestore-ktx | 32.7.0 | Apache License 2.0 | Firebase Firestore |
| com.google.firebase:firebase-storage-ktx | 32.7.0 | Apache License 2.0 | Firebase Storage |
| com.google.gms.google-services | 4.4.0 | Apache License 2.0 | Google Services plugin |
| com.google.firebase.crashlytics | 2.9.9 | Apache License 2.0 | Firebase Crashlytics |

## Image Loading

| Library | Version | License | Usage |
|---------|---------|---------|-------|
| io.coil-kt:coil-compose | 2.5.0 | Apache License 2.0 | Image loading for Compose |

## Phone Number Validation

| Library | Version | License | Usage |
|---------|---------|---------|-------|
| com.google.android.libraries:libphonenumber | 8.13.4 | Apache License 2.0 | Phone number validation |

## Testing Libraries

| Library | Version | License | Usage |
|---------|---------|---------|-------|
| junit:junit | 4.13.2 | Eclipse Public License 1.0 | Unit testing |
| org.junit.jupiter:junit-jupiter-api | 5.10.0 | Eclipse Public License 2.0 | JUnit 5 testing |
| org.mockito:mockito-core | 5.11.0 | MIT License | Mocking framework |
| org.mockito.kotlin:mockito-kotlin | 5.1.0 | MIT License | Mockito Kotlin extensions |
| org.jetbrains.kotlinx:kotlinx-coroutines-test | 1.7.3 | Apache License 2.0 | Coroutines testing |
| androidx.test.ext:junit | 1.1.5 | Apache License 2.0 | AndroidX testing |
| androidx.test.espresso:espresso-core | 3.5.1 | Apache License 2.0 | UI testing |
| androidx.compose.ui:ui-test-junit4 | 1.5.4 | Apache License 2.0 | Compose UI testing |
| androidx.test:rules | 1.5.0 | Apache License 2.0 | Test rules |

## Dependency Injection

| Library | Version | License | Usage |
|---------|---------|---------|-------|
| io.insert-koin:koin-android | 3.5.0 | Apache License 2.0 | Dependency injection |
| io.insert-koin:koin-androidx-compose | 3.5.0 | Apache License 2.0 | Koin Compose integration |

## Build Tools

| Tool | Version | License | Usage |
|------|---------|---------|-------|
| com.android.tools.build:gradle | 8.3.0 | Apache License 2.0 | Android Gradle plugin |
| org.jetbrains.kotlin:kotlin-gradle-plugin | 1.9.20 | Apache License 2.0 | Kotlin Gradle plugin |

## License Summary

All third-party libraries used in WhAlert are open-source and use permissive licenses (Apache 2.0, MIT, or Eclipse Public License). This ensures that WhAlert can be freely used, modified, and distributed.

### Apache License 2.0
The majority of libraries use the Apache License 2.0, which requires:
- Attribution (giving credit to the original authors)
- Inclusion of the original license
- Notification of changes made to the source code
- No use of the original trademarks

### MIT License
Some libraries (like Mockito) use the MIT License, which only requires:
- Inclusion of the original copyright notice and license

### Eclipse Public License
JUnit uses the Eclipse Public License, which requires:
- Inclusion of the original license
- Notification of modifications

## Compliance

WhAlert complies with all license requirements by:
1. Including this THIRD_PARTY.md file listing all dependencies
2. Including the original licenses in the project
3. Not modifying the original library source code
4. Giving proper attribution to all library authors

## Updates

This document will be updated whenever new dependencies are added or existing ones are updated. The versions listed are the ones used in the current release of WhAlert.

---

*Last updated: WhAlert v1.0.0*
