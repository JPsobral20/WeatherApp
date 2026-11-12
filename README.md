# WeatherApp 🌤️

A feature-rich weather application built with **Flutter and Dart**, providing real-time weather information, hourly forecasts, weekly statistics, and customizable weather preferences through an intuitive interface.

## Overview

WeatherApp is a cross-platform mobile application designed to help users explore weather conditions and forecasts for different locations.

By integrating the Visual Crossing Weather API, the application retrieves meteorological data and presents it through interactive dashboards, detailed weather cards, and graphical visualizations.

Users can check the weather in their current location, search for cities, save their favorite locations, and customize how weather information is displayed.

## Features

### 🌍 Location and City Management
- Retrieve weather information for the user's current location.
- Search for cities and explore their weather conditions.
- Save favorite cities for quick access.
- Manage saved locations by adding or removing cities.

### 🌡️ Weather Information
- Real-time weather conditions, including temperature and current weather descriptions.
- Daily maximum and minimum temperatures.
- Detailed meteorological information, including:
  - Humidity and precipitation.
  - Wind speed, direction, and gusts.
  - Atmospheric pressure.
  - Cloud coverage and visibility.
  - UV index and solar radiation.
  - Dew point and perceived temperature.
- Sunrise, sunset, and moon phase information.

### 📅 Forecasts and Visualizations
- Hourly weather forecasts.
- Weather forecasts for the upcoming seven days.
- Interactive charts displaying weekly weather statistics.
- Visualization of different weather metrics, including temperature, humidity, precipitation, wind speed, and atmospheric pressure.
- Sun position visualization.

### ⚙️ Customization and Preferences
- Switch between Celsius and Fahrenheit.
- Choose preferred measurement units for speed and precipitation.
- Toggle additional weather details.
- Persist user preferences locally between application sessions.

## Technology Stack

| Technology | Purpose |
|---|---|
| Flutter | Cross-platform application development |
| Dart | Application programming language |
| Provider | State management |
| SQLite (sqflite) | Local data persistence |
| Visual Crossing API | Weather data retrieval |
| fl_chart | Interactive weather charts |
| HTTP | API communication |
| Geolocation | Current location detection |

## Architecture

The application follows a modular structure that separates the user interface, state management, data retrieval, and local persistence.

```text
lib/
├── db/
│   ├── city_database.dart
│   └── settings_database.dart
├── pages/
│   ├── settings_page.dart
│   └── weather_details.dart
├── provider/
│   ├── city_provider.dart
│   └── weather_provider.dart
├── services/
│   └── weather_service.dart
├── widgets/
│   ├── weather_card.dart
│   ├── weather_info_tile.dart
│   ├── hourly_forecast_row.dart
│   └── ...
├── main.dart
└── utils.dart
```

**Main architectural components:**
- **Pages:** Application screens and user interactions.
- **Providers:** Application state management and data synchronization.
- **Services:** Communication with external weather APIs.
- **Database:** Local persistence of saved cities and user preferences.
- **Widgets:** Reusable interface components and weather visualizations.

## Getting Started

### Prerequisites

- Flutter SDK
- Dart SDK
- Android Studio or Visual Studio Code
- A Visual Crossing Weather API key

### Installation

1. Clone the repository:

```bash
git clone https://github.com/JPsobral20/WeatherApp.git
cd WeatherApp
```

2. Install the project dependencies:

```bash
flutter pub get
```

3. Configure your Visual Crossing API key.

For security, store the API key outside the source code rather than hardcoding it in `weather_service.dart`. For example, you can load it through a Dart environment variable:

```bash
flutter run --dart-define=WEATHER_API_KEY=your_api_key
```

The application must be configured to read the `WEATHER_API_KEY` value accordingly.

4. Run the application:

```bash
flutter run
```

## API Integration

WeatherApp uses the [Visual Crossing Weather API](https://www.visualcrossing.com/weather-api/) to retrieve meteorological information.

The application requests current conditions, hourly forecasts, and daily weather data, which are processed and presented through the application's interface.

An API key is required to access the service.

## License

This project was developed as an academic and personal software development project.
