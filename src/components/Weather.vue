
I

<template>
    <div v-if="weather">
      <h1>{{ weather.name }}'s Weather</h1>
      <p>{{ weather.weather[0].main }} - {{ weather.weather[0].description }}</p>
      <p>Temperature: {{ weather.main.temp }}°C</p>
      <p>Feels Like: {{ weather.main.feels_like }}°C</p>
      <p>Humidity: {{ weather.main.humidity }}%</p>
      <p>Wind Speed: {{ weather.wind.speed }} m/s</p>
    </div>
    <div v-else>
      <p>Loading...</p>
    </div>
  </template>
  
  <script>
  import axios from 'axios';
  
  export default {
    data() {
      return {
        weather: null,
      };
    },
    async created() {
      const response = await axios.get(
        `https://api.openweathermap.org/data/2.5/weather?q=Tokyo&units=metric&APPID=${import.meta.env.VITE_WEATHER_API_KEY}`
      );
      this.weather = response.data;
    },
  };
  </script>
  
  