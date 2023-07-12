<template>
    <div v-for="city in savedCities" :key="city.id">
        <CityCard :city="city" @click="goToCityView(city)" />
    </div>
    <p v-if="savedCities.length === 0">
        No location added. To start tracking a location, search in the field above.
    </p>
</template>

<script setup>
import axios from 'axios';
import { ref } from 'vue';
import CityCard from './CityCard.vue';
import { useRouter } from 'vue-router';

const router = useRouter();

const savedCities = ref([]);
const apiKey = import.meta.env.VITE_weatherToken;

const getCities = async () => {
    if (localStorage.getItem('savedCities')) {
        savedCities.value = JSON.parse(localStorage.getItem('savedCities'));

        const requests = []
        savedCities.value.forEach((city) => {
            requests.push(
                axios.get(`https://api.openweathermap.org/data/2.5/weather?lat=${city.coords.lat}&lon=${city.coords.lng}&appid=${apiKey}&units=metric`)
            )
        })

        const weatherData = await Promise.all(requests);

        weatherData.forEach((value, index) => {
            savedCities.value[index].weather = value.data;
        })
    }
}

await getCities();

const goToCityView = (city) => {
    router.push({
        name: 'city',
        params: {
            city: city.city,
            state: city.state
        },
        query: {
            id: city.id,
            lat: city.coords.lat,
            lng: city.coords.lng
        }
    })
}
</script>