# Water Pollution Reporter

A comprehensive Flutter mobile application designed to help citizens report and track water pollution incidents in their communities. This app empowers users to document environmental concerns with photo evidence, location data, and severity assessments.

## 🌟 Features

### Core Functionality
- **Photo Evidence Capture**: Take photos of pollution incidents directly within the app
- **GPS Location Detection**: Automatically detect and record incident coordinates
- **Severity Assessment**: Classify incidents as Low, Medium, or High severity
- **Report Generation**: Create detailed incident reports with timestamps
- **Local Storage**: Save reports locally using SharedPreferences
- **Report Management**: View, search, and filter all submitted reports
- **Data Export**: Export reports in text format for further analysis

### User Experience
- **Animated Splash Screen**: Engaging sewage water flow animation
- **Intuitive Navigation**: Bottom navigation between reporting and viewing reports
- **Beautiful UI**: Modern Material Design with lime/green color scheme
- **Responsive Design**: Optimized for various screen sizes
- **Permission Handling**: Proper camera and location permission management

## 📱 Screenshots

*(Add screenshots of your app here when available)*

## 🚀 Getting Started

### Prerequisites

Before running this application, ensure you have the following installed:

- **Flutter SDK**: Version 3.0.0 or higher
  ```bash
  flutter --version
  ```

- **Dart SDK**: Included with Flutter SDK

- **Android Studio** or **VS Code** with Flutter extensions

- **Android/iOS Device** or Emulator for testing

### Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/iqembulamanzi/mobile.git
   cd mobile
   ```

2. **Install dependencies**:
   ```bash
   flutter pub get
   ```

3. **Generate launcher icons** (optional):
   ```bash
   flutter pub run flutter_launcher_icons
   ```

4. **Run the application**:
   ```bash
   flutter run
   ```

### Platform-Specific Setup

#### Android
- Ensure you have Android SDK installed
- Set up an Android Virtual Device (AVD) or connect a physical device
- Enable USB debugging for physical devices

#### iOS (macOS only)
- Ensure you have Xcode installed
- Set up iOS Simulator or connect an iOS device
- Run `flutter doctor` to check iOS setup

## 📂 Project Structure

```
water_pollution_app/
├── android/                    # Android-specific files
├── ios/                       # iOS-specific files
├── lib/                       # Main Flutter application code
│   └── main.dart             # Entry point and all UI screens
├── assets/                    # Static assets
│   └── icons/
│       └── water-pollution.png
├── test/                      # Unit and widget tests
├── linux/                     # Linux desktop support
├── macos/                     # macOS desktop support
├── windows/                   # Windows desktop support
├── web/                       # Web platform support
├── pubspec.yaml              # Flutter dependencies and configuration
├── pubspec.lock              # Lockfile for dependencies
└── README.md                 # This file
```

## 🏗️ Architecture

### Main Components

#### 1. **SplashScreen**
- Animated introduction with sewage water flow effect
- Transitions to login screen after animation sequence

#### 2. **LoginScreen**
- Simple authentication form (demo purposes - accepts any credentials)
- Gradient background with water-themed styling

#### 3. **MainScreen**
- Bottom navigation between Report and Reports screens
- Manages app state and navigation

#### 4. **ReportScreen**
- Photo capture using device camera
- GPS location detection
- Severity level selection
- Form validation and report generation
- Local storage of reports

#### 5. **ReportsListScreen**
- Display all saved reports
- Search and filter functionality
- Export reports to text format
- Navigate to detailed report view

#### 6. **ReportDetailScreen**
- Detailed view of individual reports
- Display photo evidence and all report metadata

### Data Models

#### PollutionReport
```dart
class PollutionReport {
  final String id;
  final String coordinates;
  final String severity;
  final String imagePath;
  final DateTime timestamp;
  final String status;
}
```

## 📋 Dependencies

### Production Dependencies
- **flutter**: SDK for building the UI
- **image_picker**: For capturing photos from camera/gallery
- **shared_preferences**: Local data persistence
- **geolocator**: GPS location services
- **permission_handler**: Managing app permissions

### Development Dependencies
- **flutter_test**: Unit and widget testing
- **flutter_lints**: Code linting and analysis
- **flutter_launcher_icons**: Generate app icons

## 🔧 Configuration

### Permissions

The app requires the following permissions:

#### Android (android/app/src/main/AndroidManifest.xml)
```xml
<uses-permission android:name="android.permission.CAMERA" />
<uses-permission android:name="android.permission.ACCESS_FINE_LOCATION" />
<uses-permission android:name="android.permission.ACCESS_COARSE_LOCATION" />
```

#### iOS (ios/Runner/Info.plist)
```xml
<key>NSCameraUsageDescription</key>
<string>This app needs camera access to capture pollution evidence</string>
<key>NSLocationWhenInUseUsageDescription</key>
<string>This app needs location access to record pollution incident locations</string>
```

## 🧪 Testing

Run the test suite:
```bash
flutter test
```

Run tests with coverage:
```bash
flutter test --coverage
```

## 📦 Building for Production

### Android APK
```bash
flutter build apk --release
```

### iOS (macOS only)
```bash
flutter build ios --release
```

### Web
```bash
flutter build web --release
```

## 🚀 Deployment

### Google Play Store (Android)
1. Build release APK/AAB
2. Create Google Play Console account
3. Upload and configure store listing
4. Publish to production

### Apple App Store (iOS)
1. Build release IPA
2. Create Apple Developer account
3. Configure App Store Connect
4. Submit for review and publish

## 🤝 Contributing

We welcome contributions to improve the Water Pollution Reporter app!

### How to Contribute
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

### Development Guidelines
- Follow Flutter best practices
- Write clear, documented code
- Add tests for new features
- Ensure UI is responsive and accessible
- Test on multiple devices/emulators

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🙏 Acknowledgments

- Flutter team for the amazing framework
- Material Design for UI inspiration
- Open source community for various packages used

## 📞 Support

If you encounter any issues or have questions:

1. Check the Issues section on GitHub
2. Create a new issue with detailed description
3. Include device information, Flutter version, and error logs

## 🔄 Future Enhancements

- [ ] Cloud storage integration (Firebase/AWS)
- [ ] Real-time reporting to authorities
- [ ] Social sharing of reports
- [ ] Analytics and reporting dashboard
- [ ] Multi-language support
- [ ] Offline map integration
- [ ] Push notifications for report updates
- [ ] Integration with environmental agencies

---

**Made with ❤️ for a cleaner environment**
