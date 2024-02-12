# PY-Weather

## Project Overview
The Weather App is a Flask application that fetches and displays real-time weather information for a specified city using the OpenWeatherMap API. Users can interact with the system through a simple web interface. The application is built using Flask for handling web requests, and it utilizes Thymeleaf for server-side templating. Weather data is stored and retrieved from the OpenWeatherMap API, offering a comprehensive view of temperature, description, humidity, and more.

## Table of Contents
- [Project Structure](#project-structure)
- [Dependencies](#dependencies)
- [Usage](#usage)
- [Endpoints](#endpoints)
- [Database Configuration](#openweathermap-api-configuration)
- [Error Handling](#error-handling)
- [Contributing](#contributing)
- [License](#license)

## Project Structure
The project follows a straightforward Flask structure:

- **app.py:** Main application file with the Flask setup.
- **templates/index.html:** Thymeleaf template for rendering the main page.
- **templates/about.html:** Thymeleaf template for rendering the about page.
- **templates/error.html:** Thymeleaf template for rendering error pages.

## Dependencies
The application relies on the following key dependencies:

- Flask
- Flask-Caching
- Requests

Ensure these dependencies are installed before running the project.

## Usage
To use the application:

1. Clone the repository: `git clone <repository-url>`
2. Obtain a valid OpenWeatherMap API key and replace `api_key` in `app.py` with your key.
3. Run the application: `python app.py`
4. Access the application in a web browser: [http://127.0.0.1:5000/](http://127.0.0.1:5000/)

## Endpoints
- **/**: Main page for entering city names and fetching weather data.
- **/about:** About page providing additional information about the application.
- **/country/{country_code}:** API endpoint to retrieve information about a country using its alpha-3 country code.

## OpenWeatherMap API Configuration
Configure the OpenWeatherMap API connection in `app.py`:

```python
api_key = "your_openweathermap_api_key"
weather_url = f"http://api.openweathermap.org/data/2.5/weather?q={{city}}&appid={api_key}"
****
