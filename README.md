# WeatherApp

**A Kotlin-based Android app** that fetches and displays real-time weather data from the OpenWeatherMap 2.5 API.  
By default it shows your device’s current location weather (Seattle, WA for this assignment), and lets you search any city by name.

---

## 📋 Objective

- **Design** the app UI in Figma 
- **Implement** a Kotlin Android application that integrates with an external REST API  
- **Display**:
  - City name  
  - Current temperature (°C)  
  - Weather condition (e.g. cloudy, sunny, rainy)  
  - Minimum & maximum temperatures  
  - Sunrise & sunset times  
  - Wind speed, pressure, humidity  

---

## 🎨 UI / Figma Mockup

Your Figma design should include:

1. **Header**  
   - City name (large, bold)
2. **Main Panel**  
   - Prominent current temperature  
   - Weather icon + condition text  
3. **Details Grid**  
   | Min Temp | Max Temp | Sunrise  | Sunset   |
   | -------- | -------- | -------- | -------- |
   | Wind     | Pressure | Humidity |          |
4. **Search Bar**  
   - Text input (placeholder: “Enter city name”)  
   - Search button  
5. **Error & Loading States**  
   - Inline error message or Toast for invalid/blank input  
   - “Please connect to internet” if offline  
   - Progress spinner while loading  

---

## ⚙️ Features

- **Automatic Location**  
  On launch, requests `ACCESS_FINE_LOCATION` and displays weather for latitude/longitude.

- **City Search**  
  Enter any city, tap **Search**, and view its weather data.

- **Robust Error Handling**  
  - Blank input → “City name cannot be blank”  
  - Invalid city → “Could not retrieve data. Check city name.”  
  - No Internet → “Please connect to internet”  
  - Location unavailable → Toast “Unable to get location”

- **Graceful Networking**  
  - All HTTP calls on a background thread (Kotlin Coroutines)  
  - UI updates on the main thread  
  - JSON parsed via Gson (or Kotlinx-Serialization + Ktor)
