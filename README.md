# Flutter Weather App 🌤️

A beautiful and intuitive weather application built with **Flutter & Dart**. Get real-time weather information with a clean, modern interface for iOS and Android.

## 📋 Table of Contents
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [API Integration](#api-integration)
- [Contributing](#contributing)
- [License](#license)

## ✨ Features

- 🌍 **Real-time Weather Data** - Get current weather conditions instantly
- 📍 **Location-Based Search** - Automatic location detection and manual search
- 🌡️ **Detailed Metrics** - Temperature, humidity, wind speed, UV index, pressure
- 🎨 **Beautiful UI** - Modern, intuitive, and responsive interface
- 📅 **Weather Forecast** - 7-day and hourly forecast
- 🌙 **Dark Mode** - Eye-friendly dark theme support
- 📱 **Cross-Platform** - Works seamlessly on iOS and Android
- ⚡ **Fast & Lightweight** - Optimized performance and minimal app size
- 🔄 **Auto-Refresh** - Automatic weather updates at intervals
- ❤️ **Favorite Locations** - Save multiple locations
- 🌐 **Offline Support** - Cached data for offline access
- 🔔 **Weather Alerts** - Notifications for severe weather

## 🛠️ Tech Stack

- **Frontend**: Flutter 3.x
- **Language**: Dart
- **State Management**: Provider / Riverpod
- **Weather API**: OpenWeatherMap / WeatherAPI
- **Location Services**: Geolocator / Google Maps
- **Local Storage**: Hive / SQLite
- **HTTP Client**: Dio / http

## 📦 Installation

### Prerequisites
- Flutter SDK (3.0+)
- Dart SDK
- Android Studio / Xcode
- Git
- OpenWeatherMap API Key (free signup at [openweathermap.org](https://openweathermap.org/api))

### Setup Steps

```bash
# Clone the repository
git clone https://github.com/dugo-codes/flutter_weather_app.git
cd flutter_weather_app

# Get Flutter dependencies
flutter pub get

# Get API key from OpenWeatherMap
# Create/update lib/config/api_config.dart with your API key

# Run the app on iOS
flutter run -d ios

# Run the app on Android
flutter run -d android

# Build for release
flutter build apk --release   # Android
flutter build ios --release   # iOS
```

## 🚀 Usage

### First Launch
1. Grant location permissions when prompted
2. App automatically detects your current location
3. View current weather and forecast
4. Search for other cities
5. Add favorite locations

### Navigation
- **Home**: Current weather and forecast
- **Search**: Find weather by city
- **Favorites**: Your saved locations
- **Settings**: App preferences and units

## 📁 Project Structure

```
flutter_weather_app/
├── lib/
│   ├── main.dart                 # Entry point
│   ├── models/
│   │   ├── weather_model.dart
│   │   ├── forecast_model.dart
│   │   └── location_model.dart
│   ├── screens/
│   │   ├── home_screen.dart
│   │   ├── search_screen.dart
│   │   ├── favorites_screen.dart
│   │   ├── forecast_screen.dart
│   │   └── settings_screen.dart
│   ├── providers/
│   │   ├── weather_provider.dart
│   │   ├── location_provider.dart
│   │   ├── theme_provider.dart
│   │   └── favorites_provider.dart
│   ├── services/
│   │   ├── weather_service.dart
│   │   ├── location_service.dart
│   │   ├── storage_service.dart
│   │   └── notification_service.dart
│   ├── widgets/
│   │   ├── weather_card.dart
│   │   ├── forecast_item.dart
│   │   ├── search_bar.dart
│   │   └── custom_appbar.dart
│   ├── config/
│   │   ├── api_config.dart
│   │   ├── theme_config.dart
│   │   └── constants.dart
│   └── utils/
│       ├── date_formatter.dart
│       └── weather_utils.dart
├── assets/
│   ├── images/
│   ├── icons/
│   └── animations/
├── pubspec.yaml
└── README.md
```

## 🔌 API Integration

### OpenWeatherMap Setup

1. Sign up at [OpenWeatherMap](https://openweathermap.org/api)
2. Get your free API key
3. Create `lib/config/api_config.dart`:

```dart
class ApiConfig {
  static const String OPEN_WEATHER_API_KEY = 'your_api_key_here';
  static const String BASE_URL = 'https://api.openweathermap.org/data/2.5';
}
```

### Key Endpoints

```
GET /weather          # Current weather
GET /forecast/5day    # 5-day forecast
GET /forecast/hourly  # Hourly forecast
GET /geo/direct       # Geocoding
GET /geo/reverse      # Reverse geocoding
```

## ⚙️ Configuration

### Update Theme
Edit `lib/config/theme_config.dart`:

```dart
const Color primaryColor = Color(0xFF1F77F2);      // Weather blue
const Color secondaryColor = Color(0xFFFF9500);    // Sunny orange
const Color backgroundColor = Color(0xFFF5F5F5);
```

### Change Weather Units
- Celsius (default)
- Fahrenheit
- Kelvin

## 📱 Screenshots

- Home screen with current weather
- Hourly and daily forecast
- City search functionality
- Favorite locations management
- Weather details page
- Settings and preferences

## 🧪 Testing

```bash
# Run all tests
flutter test

# Run specific test file
flutter test test/services/weather_service_test.dart

# Generate coverage report
flutter test --coverage
```

## 📦 Dependencies

```yaml
provider: ^6.0.0          # State management
dio: ^5.0.0               # HTTP client
geolocator: ^9.0.0        # Location services
hive: ^2.0.0              # Local storage
flutter_local_notifications: ^14.0.0  # Notifications
intl: ^0.18.0             # Internationalization
```

## 🚀 Deployment

### Android
```bash
# Generate release APK
flutter build apk --release

# Generate App Bundle for Play Store
flutter build appbundle --release
```

### iOS
```bash
# Generate release build
flutter build ios --release

# Archive for App Store
flutter build ios --release
```

### Publish to App Stores
- [Google Play Console](https://play.google.com/console)
- [Apple App Store Connect](https://appstoreconnect.apple.com/)

## 🐛 Troubleshooting

### Location not detected
- Check location permissions in app settings
- Ensure location services are enabled on device
- For emulator, set a mock location

### API errors
- Verify API key is valid
- Check internet connection
- Ensure API limits not exceeded

### Build issues
```bash
# Clean build
flutter clean

# Get latest dependencies
flutter pub get

# Upgrade Flutter
flutter upgrade
```

## 🤝 Contributing

Contributions are welcome! Please:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit changes (`git commit -m 'Add AmazingFeature'`)
4. Push to branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is open source and available under the MIT License.

## 🙏 Acknowledgments

- OpenWeatherMap for weather data API
- Flutter community for excellent documentation
- Package contributors for amazing libraries
- Beta testers for valuable feedback

## 📚 Resources

- [Flutter Documentation](https://docs.flutter.dev/)
- [OpenWeatherMap API Docs](https://openweathermap.org/api)
- [Dart Documentation](https://dart.dev/guides)
- [Provider Package](https://pub.dev/packages/provider)

---

**Made with ❤️ by [Dugo](https://github.com/dugo-codes)**

⭐ If you find this project helpful, please give it a star!