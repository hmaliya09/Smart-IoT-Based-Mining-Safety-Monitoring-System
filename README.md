# Smart-IoT-Based-Mining-Safety-Monitoring-System
Overview
This project aims to create a safer and more responsive mining environment by leveraging IoT technologies, focusing on real-time monitoring of environmental conditions in coal mines. It integrates sensors for temperature, humidity, light, gas, and rain detection using Arduino Uno, ESP8266, and the Blynk app for remote monitoring. The system is designed to enhance safety, improve operational efficiency, and reduce the risk of accidents or health hazards for workers in the mining industry.

Features
Real-time Data Monitoring: Continuously monitors temperature, humidity, light levels, and gas concentrations in the environment.
Remote Alerts: Sends alerts to a mobile app through the Blynk platform when unsafe conditions are detected.
Gas Detection with Safety Alarm: Activates a buzzer when dangerous gas levels are detected using an MQ2 sensor.
Light Detection: Uses an LDR (Light Dependent Resistor) to detect changes in light levels, triggering an LED when necessary.
Future-Ready: Includes provisions for rain detection, which can be enabled with further code development.
Hardware Requirements
Arduino Uno
ESP8266 Wi-Fi Module
DHT11 Sensor (Temperature and Humidity)
MQ2 Gas Sensor
LDR (Light Dependent Resistor)
Rain Sensor (optional, currently disabled in the code)
Buzzer
LED
Resistors and connecting wires
Breadboard
Software Requirements
Arduino IDE
Blynk app (available on Android/iOS)
Libraries: ESP8266WiFi, BlynkSimpleEsp8266, DHT
Installation and Setup
Clone the Repository:

bash
Copy code
git clone https://github.com/hmaliya09/Smart-IoT-Based-Mining-Safety-Monitoring-System
cd IoT-Mining-Safety-Monitoring
Library Installation:

Install the ESP8266WiFi and Blynk libraries from the Arduino Library Manager.
Include the DHT library for temperature and humidity readings.
Wiring the Sensors:

Connect the DHT11 sensor to the specified pin on the Arduino.
Wire the MQ2 gas sensor, LDR, buzzer, and other components as per the pin definitions in the code.
Upload the Code:

Open the code in the Arduino IDE.
Enter your Wi-Fi SSID and password, and your Blynk authentication token.
Upload the code to your Arduino Uno.
Configure Blynk App:

Create a new project in the Blynk app.
Add virtual pins for temperature, humidity, gas level, and light detection as specified in the code (V0, V1, V2, V5).
Set up notifications to receive alerts when conditions cross predefined thresholds.
Code Breakdown
1. Libraries and Definitions
Includes Blynk, ESP8266WiFi, and DHT libraries for handling Wi-Fi communication, temperature/humidity sensor, and Blynk integration.
Defines pins for the sensors, buzzer, and LED.
2. Setup Function
Initializes serial communication for debugging.
Establishes a connection with the Blynk server using Wi-Fi credentials.
Sets up the DHT sensor and initializes other components like the buzzer.
3. Loop Function
Runs the Blynk service to maintain a connection.
Reads temperature and humidity data from the DHT11 sensor.
Sends sensor readings to the Blynk app and triggers alerts if values exceed safe thresholds.
Checks gas levels with the MQ2 sensor and activates the buzzer if the gas concentration is too high.
4. Blynk Integration
Uses virtual pins to send temperature, humidity, gas, and light data to the Blynk app.
Allows remote monitoring and provides real-time feedback on environmental conditions.
Future Improvements
Enable Rain Detection: Complete the code for rain sensor functionality to provide feedback on weather conditions in mining areas.
Expand Sensor Array: Integrate additional sensors for parameters like CO2 levels and air quality.
Optimize Power Consumption: Implement sleep modes for energy efficiency during data collection.
Data Analytics: Store and analyze collected data over time for predictive maintenance and trend analysis.
Contributing
Contributions are welcome! Feel free to open an issue or submit a pull request for bug fixes or improvements.
