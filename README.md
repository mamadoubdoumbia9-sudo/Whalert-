# WhAlert

**WhAlert** is a legitimate Android application that helps users document and report suspicious or malicious WhatsApp accounts through official channels. It provides a structured way to organize evidence, generate professional reports, and submit them using WhatsApp's official reporting mechanisms.

## Features

### Core Functionality
- **Report Creation**: Create detailed reports for suspicious WhatsApp accounts
- **Evidence Organization**: Attach screenshots, text evidence, and other proof
- **Official Submission**: Submit reports through WhatsApp's official channels
- **Report Tracking**: Track the status of your submitted reports
- **Report History**: View all your past reports

### User Experience
- **Modern UI**: Built with Jetpack Compose and Material 3 design
- **Responsive Design**: Works on all Android devices and screen sizes
- **Dark/Light Mode**: Supports both light and dark themes
- **Accessibility**: Fully accessible with proper screen reader support

### Security & Privacy
- **No Private APIs**: Only uses officially documented WhatsApp features
- **Data Protection**: All user data is encrypted and protected
- **Secure Storage**: Uses Android Keystore for sensitive data
- **No Spam**: Prevents abuse with daily limits and validation

### Transparency
- **Clear Limitations**: Explicitly states what the app can and cannot do
- **No False Promises**: Never claims to guarantee account suspensions
- **Official Channels Only**: All reports go through WhatsApp's official mechanisms

## Installation

### From APK
1. Download the latest `app-release.apk` from the releases
2. Enable "Unknown Sources" in your Android settings
3. Install the APK file
4. Open WhAlert and follow the on-screen instructions

### From Source
1. Clone this repository
2. Open in Android Studio
3. Build and run on your device or emulator

## Usage

### Creating a Report
1. Tap "New Report" from the home screen
2. Enter the phone number of the account you want to report
3. Select the appropriate category (spam, scams, impersonation, etc.)
4. Provide a detailed description of what happened
5. Add any evidence (screenshots, messages, etc.)
6. Review and confirm your report
7. Submit through the official WhatsApp reporting mechanism

### Viewing Report History
1. Tap "My Reports" from the home screen
2. Browse your list of submitted reports
3. Tap on any report to view its details and status

### Settings
- Configure app theme (light/dark/system)
- Enable/disable notifications
- Set up biometric authentication
- Adjust daily report limits

## Technical Details

### Architecture
- **Language**: Kotlin
- **UI Framework**: Jetpack Compose
- **Architecture**: MVVM (Model-View-ViewModel)
- **Dependency Injection**: Koin
- **Database**: Room
- **Network**: Retrofit + OkHttp
- **Firebase**: Authentication, Firestore, Storage

### Libraries Used
See [THIRD_PARTY.md](THIRD_PARTY.md) for a complete list of third-party libraries and their licenses.

### Minimum Requirements
- Android 7.0 (API 24) or higher
- Internet connection (Wi-Fi or mobile data)

## What WhAlert CAN Do

✅ **Prepare a report dossier** - Organize all information and evidence for your report

✅ **Organize evidence** - Keep track of screenshots, messages, and other proof

✅ **Generate report text** - Create a professional, fact-based report text

✅ **Request confirmation** - Ask for your explicit confirmation before submission

✅ **Transmit via available channels** - Use official WhatsApp reporting mechanisms

✅ **Store your report history** - Keep a record of all your submitted reports

✅ **Show technical confirmations** - Display confirmations received from official channels

## What WhAlert CANNOT Do

❌ **Guarantee account suspension** - Only WhatsApp can decide to suspend an account

❌ **Know WhatsApp's internal decisions** - WhatsApp does not provide public confirmation of moderation decisions

❌ **Send false reports** - All reports must be genuine and based on real experiences

❌ **Multiply reports artificially** - Each report must correspond to a real incident

❌ **Bypass WhatsApp protections** - This app respects all of WhatsApp's security measures

❌ **Force WhatsApp to suspend an account** - Suspension decisions are made solely by WhatsApp

## Security Features

### Data Protection
- All sensitive data is encrypted at rest
- No plain text storage of user credentials
- Uses Android Keystore for cryptographic operations

### Rate Limiting
- Daily report limit (default: 3 reports per 24 hours)
- Prevents abuse and spam
- Configurable by the user

### Authentication
- Optional user accounts with email/password
- Firebase Authentication integration
- Biometric authentication support

### Network Security
- All communications use HTTPS
- Certificate pinning
- Request validation

## Privacy Policy

This application respects your privacy:

- **No Data Collection**: We don't collect or share your personal information
- **Local Storage Only**: All your reports are stored locally on your device
- **No Tracking**: We don't track your usage or behavior
- **No Third-Party Analytics**: No analytics or tracking services are used

For more details, see our full Privacy Policy.

## Terms of Service

By using WhAlert, you agree to:

1. Only report accounts that you genuinely believe are involved in malicious activities
2. Provide accurate and truthful information
3. Not use the app for harassment or abuse
4. Respect all applicable laws and regulations
5. Not attempt to reverse engineer or modify the app

## Reporting Issues

If you encounter any issues with WhAlert:

1. Check the [FAQ](#faq) below
2. Review the [Troubleshooting](#troubleshooting) section
3. Create an issue in this repository

## FAQ

### Q: Can WhAlert actually ban WhatsApp accounts?
A: No. WhAlert only helps you create and submit reports through WhatsApp's official channels. Only WhatsApp can decide to suspend or ban accounts.

### Q: How do I know if my report was successful?
A: WhAlert will show you the confirmation from the official WhatsApp reporting mechanism. However, WhatsApp does not always provide feedback on report status.

### Q: Can I report multiple accounts at once?
A: Yes, but each report must be for a different account and a genuine incident. The app has a daily limit to prevent abuse.

### Q: Is WhAlert affiliated with WhatsApp?
A: No. WhAlert is an independent application and is not affiliated with, endorsed by, or sponsored by WhatsApp Inc. or Meta Platforms, Inc.

### Q: Does WhAlert store my reports on a server?
A: No. By default, all your reports are stored locally on your device. You can optionally back them up to Firebase if you choose to create an account.

## Troubleshooting

### Installation Issues
- **"App not installed"**: Make sure you have enough storage space and that the APK is not corrupted
- **"Unknown sources blocked"**: Enable "Unknown Sources" in your Android security settings
- **"Incompatible device"**: WhAlert requires Android 7.0 or higher

### Usage Issues
- **Reports not submitting**: Check your internet connection and try again
- **App crashing**: Try clearing the app cache or reinstalling
- **Features not working**: Make sure you're using the latest version

### Performance Issues
- **Slow performance**: Close other apps and try again
- **App freezing**: Restart your device and try again
- **High battery usage**: This is normal for the first few uses as the app caches data

## Contributing

Contributions are welcome! Please read our [Contributing Guidelines](CONTRIBUTING.md) before submitting pull requests.

## License

WhAlert is released under the MIT License. See [LICENSE](LICENSE) for details.

## Contact

For questions or support, please create an issue in this repository.

---

**WhAlert v1.0.0**

Copyright © 2024 WhAlert Team

*This application is not affiliated with, endorsed by, or sponsored by WhatsApp Inc. or Meta Platforms, Inc. All trademarks and registered trademarks are the property of their respective owners.*
