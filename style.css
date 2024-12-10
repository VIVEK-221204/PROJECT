document.getElementById('getWeatherBtn').addEventListener('click', getWeather);

async function getWeather() {
    const city = document.getElementById('city').value;
    const apiKey = '0585a404fa29a21eb467b591f269998e'; // Replace with your OpenWeatherMap API key
    const url = `https://api.openweathermap.org/data/2.5/weather?q=${city}&appid=${apiKey}&units=metric`;

    if (!city) {
        alert("Please enter a city name.");
        return;
    }

    try {
        const response = await fetch(url);
        const data = await response.json();

        if (data.cod === '404') {
            alert('City not found');
            return;
        }

        // Show the weather info
        document.getElementById('cityName').textContent = `${data.name}, ${data.sys.country}`;
        document.getElementById('temperature').textContent = `Temperature: ${data.main.temp}°C`;
        document.getElementById('description').textContent = `Description: ${data.weather[0].description}`;
        document.getElementById('humidity').textContent = `Humidity: ${data.main.humidity}%`;
        document.getElementById('windSpeed').textContent = `Wind Speed: ${data.wind.speed} m/s`;

        document.getElementById('weatherInfo').style.display = 'block';
    } catch (error) {
        console.error(error);
        alert("An error occurred. Please try again later.");
    }
}
