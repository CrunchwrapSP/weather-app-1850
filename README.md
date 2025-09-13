# weather-app-1850
EzWeather
A feature-rich, terminal-based weather application written in C. EzWeather fetches real-time data from the OpenWeatherMap API and presents it with an intuitive NCurses interface, complete with ASCII art and personalized suggestions.

Features
Real-Time Weather Data: Fetches and displays current temperature, "feels like" temperature, highs, lows, humidity, wind speed/direction, cloud coverage, and precipitation.

Multiple User Profiles: Save up to 3 user profiles with unique names, zip codes, and display preferences.

Interactive Terminal UI: Uses NCurses for a clean, formatted display that stays in the terminal.

Visual Weather Graphics: Displays custom ASCII art based on current weather conditions (Sunny, Cloudy, Rainy, Snowy).

Personalized Suggestions: Provides intelligent clothing and activity recommendations based on the current weather.

Extreme Weather Alerts: Issues warnings for dangerous conditions like tornadoes, severe thunderstorms, high winds, and extreme heat.

How to Build & Run
Prerequisites
Before compiling, you must install the required development libraries:

On Ubuntu/Debian:

bash
sudo apt-get install libcurl4-openssl-dev libjson-c-dev libncurses-dev
On Fedora/RHEL:

bash
sudo dnf install libcurl-devel json-c-devel ncurses-devel
Compilation
Clone or download the source code.

Insert your API key: Replace INSERT_API_KEY_HERE in the createApiURL function within ezweather.c with your free API key from OpenWeatherMap.

Compile the program:

bash
gcc -o ezweather ezweather.c -lcurl -ljson-c -lncurses
Execution
Run the compiled binary:

bash
./ezweather
How to Use
Start the Program: Launch the application from your terminal.

Profile Management:

You will be prompted to either display weather for an existing profile or create a new one.

To create a profile, provide a name, a valid 5-digit US zip code, and choose which optional data (humidity, wind speed, cloud coverage) you want to display.

You can manage up to 3 profiles.

Viewing Weather: Select a profile to view its weather report. The application will fetch the latest data and present it in a full-screen NCurses display.

Interpreting the Display:

The top-left shows your profile name, location, and a general description.

The center column shows core temperature data.

The right column shows your chosen optional data.

The bottom section provides personalized suggestions and any critical weather warnings.

Exiting: Press any key to close the weather display and return to the profile selection menu.

Project Structure
text
ezweather/
├── ezweather.c          # Main application source code
├── profiles.txt         # Auto-generated file storing user profiles
├── current-weather.json # Auto-generated file caching API responses
└── README.md           # This file
Dependencies
libcurl - For handling HTTP requests to the API.

libjson-c - For parsing the JSON data returned from the API.

NCurses - For creating the text-based user interface.

API Reference
This application uses the OpenWeatherMap Current Weather Data API. You must sign up for a free account to obtain an API key.

Disclaimer
This project is for educational and personal use. Always rely on official weather sources and emergency alerts for critical weather information and warnings.
