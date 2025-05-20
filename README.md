# Weather App

## Project Overview
This Android application allows users to search for and display weather information for any location using the OpenWeatherMap API. The app shows current temperature, weather conditions, min/max temperatures, sunrise/sunset times, wind speed, pressure, and humidity.

## Features
- Search for weather by city name
- Display current weather information including:
  - Current temperature
  - Weather conditions (clear, cloudy, etc.)
  - Min/max temperatures
  - Sunrise and sunset times
  - Wind speed, pressure, and humidity
- Error handling for:
  - Empty city name input
  - Invalid city names
  - No internet connection
- Bonus feature: Shows weather for current device location by default

## Implementation Details
- **Language**: Kotlin
- **Architecture**: MVVM (Model-View-ViewModel)
- **API**: OpenWeatherMap API v2.5
- **Libraries**:
  - Retrofit for network calls
  - LiveData for reactive UI updates
  - Google Play Services Location for device location

## Setup Instructions
1. Clone the repository
2. Open the project in Android Studio
3. Replace `API_KEY` in MainActivity.kt with your OpenWeatherMap API key
4. Build and run the application

## Development Process
- Created UI design based on requirements and example videos
- Implemented data models for API responses
- Built network layer with Retrofit
- Created ViewModel for handling business logic
- Implemented UI with proper error handling
- Added location-based weather functionality

## Challenges Faced
- Handling various error scenarios gracefully
- Implementing location permissions and fallbacks
- Ensuring UI matches the design specifications

## Time Spent
Approximately 10 hours total:
- 2 hours for design and planning
- 6 hours for implementation
- 2 hours for testing and refinement

## References
- OpenWeatherMap API Documentation: https://openweathermap.org/api
- Android Developer Documentation: https://developer.android.com/
- Material Design Guidelines: https://material.io/design
- Stack Overflow for specific implementation questions

## Future Improvements
- Add weather icons based on conditions
- Implement data caching for offline access
- Add unit tests for better code reliability
- Add daily/weekly forecast functionality
