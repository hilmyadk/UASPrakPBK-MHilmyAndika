<template>
  <q-page class="q-pa-md flex flex-center">
    <q-card class="q-pa-md transparent-card" style="width: 1000px;">
      <div class="weather">
        <h4>Ingin Tau Bagaimana Cuaca Hari Ini?</h4>
        <q-input v-model="city" label="Masukkan Nama Kota" @keyup.enter="getWeather" filled />
        <q-btn @click="getWeather" label="Cek Cuaca" color="cyan" class="q-mt-md" />
        <div v-if="weather" class="q-mt-md">
          <q-card class="transparent-card">
            <q-card-section>
              <div class="text-h6">{{ weather.name }}</div>
              <div>Weather : {{ weather.weather[0].description }}</div>
              <div>Temperature : {{ weather.main.temp }}°C</div>
            </q-card-section>
          </q-card>
        </div>
      </div>
    </q-card>
  </q-page>
</template>
  
<script>
  import axios from 'axios';
  
  export default {
    data() {
      return {
        city: '',
        weather: null,
      };
    },
    methods: {
      async getWeather() {
        try {
          const apiKey = '5794d4556b62db90e55e0cf80e279406';
          const response = await axios.get(
            `https://api.openweathermap.org/data/2.5/weather?q=${this.city}&units=metric&appid=${apiKey}`
          );
          this.weather = response.data;
        } catch (error) {
          console.error(error);
        }
      },
    },
  };
</script>
  
<style scoped>
  .weather {
    text-align: center;
    margin-top: 20px;
  }

  .transparent-card {
  background-color: rgba(255, 255, 255, 0.5);
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
  border-radius: 8px;
  }
</style>
  
  