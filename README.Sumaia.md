# Weather Information App

## Overview
The Weather Information App is a Java-based desktop application that provides users with current weather information and forecasts for various locations. Utilizing the OpenWeatherMap API, this application allows users to input a city name and receive detailed weather data, including temperature, humidity, wind speed, and a 5-day weather forecast. 

## Features

### Server:
- Integrates with the OpenWeatherMap API for real-time weather data retrieval.
- Handles HTTP requests and JSON responses for fetching current weather and forecast data.

### Client:
- User-friendly graphical interface built with Swing.
- Allows users to input location (city name) and fetch weather data.
- Displays current weather conditions, including temperature, humidity, and wind speed.
- Provides a 5-day weather forecast.
- Option to select temperature units (Celsius or Fahrenheit).
- Maintains a searchable history of previous weather searches.

## Requirements
- Java Development Kit (JDK) 8 or higher
- Apache Maven (optional for dependency management)
- An active internet connection to access the OpenWeatherMap API.
- OpenWeatherMap API key (replace with your own in the WeatherAPI class).

## Getting Started

### Steps
1. *Clone the Repository*: 
   ```bash
   git clone <repository-url>
   cd WeatherInfoApp

	2.	Set Up Your API Key:
	•	Replace the placeholder API key in the WeatherAPI class with your own OpenWeatherMap API key:

private static final String OPEN_WEATHER_API_KEY = "YOUR_API_KEY_HERE";


	3.	Compile the Application:
	•	Use your IDE (like IntelliJ IDEA) to open the project or compile it via command line.

javac -d bin src/weatherInfoApp/*.java


	4.	Run the Application:
	•	Execute the main class to launch the application.

java -cp bin weatherInfoApp.WeatherApp


	5.	Use the Application:
	•	Input a city name in the provided text field and click the “Search” button to retrieve weather data.
	•	Use the combo box to switch between Celsius and Fahrenheit for temperature display.
	•	View search history by double-clicking previous searches in the list.

License

This project is licensed under the MIT License - see the LICENSE file for details.

Acknowledgements

	•	This application uses the OpenWeatherMap API for fetching weather data. Visit their official website for more information.
