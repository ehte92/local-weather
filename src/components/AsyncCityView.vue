<template>
    <div class="flex flex-col flex-1 items-center">
        <!-- Banner -->
        <div v-if="route.query.preview" class="text-white p-4 bg-weather-secondary w-full text-center">
            <p>You are currently previewing this city. Click '+' icon to start tracking this city.</p>
        </div>
        <!-- Weather Overview -->
        <div class="flex flex-col items-center text-white py-12">
            <h1 class="text-4xl mb-2">{{ route.params.city }}</h1>
            <p class="text-sm mb-12">
                {{
                    new Date(weatherData.currentTime).toLocaleDateString(
                        "en-US",
                        {
                            weekday: "short",
                            month: "long",
                            day: "2-digit"
                        }
                    )
                }}
                {{
                    new Date(weatherData.currentTime).toLocaleTimeString(
                        "en-US",
                        {
                            timeStyle: "short"
                        }
                    )
                }}
            </p>
            <p class="text-8xl mb-8">
                {{ Math.round(weatherData.current.temp) }}&deg;C
            </p>
            <p>Feels like {{ Math.round(weatherData.current.feels_like) }}&deg;C</p>
            <p class="capitalize">{{ weatherData.current.weather[0].description }}</p>
            <img class="w-[150px] h-auto"
                :src="`http://openweathermap.org/img/wn/${weatherData.current.weather[0].icon}@2x.png`" alt="weather-icon">
        </div>
        <hr class="border-white border-opacity-10 border w-full" />
        <!-- Hourly Weather -->
        <div class="max-w-screen-md w-full py-12">
            <div class="mx-8 text-white">
                <h2 class="mb-4">Hourly Weather</h2>
                <div class="flex gap-10 overflow-x-scroll no-scrollbar">
                    <div v-for="hourlyData in weatherData.hourly" :key="hourlyData.dt"
                        class="flex flex-col gap-4 items-center">
                        <p class="whitespace-nowrap text-md">
                            {{
                                new Date(hourlyData.currentTime).toLocaleTimeString(
                                    "en-US",
                                    {
                                        hour: "numeric",
                                    }
                                )
                            }}
                        </p>
                        <img :src="`http://openweathermap.org/img/wn/${hourlyData.weather[0].icon}@2x.png`"
                            alt="hourly-weather" class="w-auto h-[50px] object-cover">
                        <p class="text-xl">
                            {{ Math.round(hourlyData.temp) }}&deg;C
                        </p>
                    </div>
                </div>
            </div>
        </div>
        <hr class="border-white border-opacity-10 border w-full" />
        <!-- Weekly Weather -->
        <div class="max-w-screen-md w-full py-12">
            <div class="mx-8 text-white">
                <h2 class="mb-4">7 Day Forecast</h2>
                <div v-for="day in weatherData.daily" :key='day.dt' class="flex items-center">
                    <p class="flex-1">
                        {{
                            new Date(day.dt * 1000).toLocaleDateString(
                                "en-US",
                                {
                                    weekday: "long",
                                }
                            )
                        }}
                    </p>
                    <img class="w-[50px] h-[50px] object-cover"
                        :src="`http://openweathermap.org/img/wn/${day.weather[0].icon}@2x.png`" alt="weekly-weather">
                    <div class="flex gap-2 flex-1 justify-end">
                        <p>H: {{ Math.round(day.temp.max) }}</p>
                        <p>L: {{ Math.round(day.temp.min) }}</p>
                    </div>
                </div>
            </div>
        </div>

        <div v-if="!route.query.preview"
            class="flex items-center gap-2 py-12 text-white cursor-pointer duration-150 hover:text-red-500"
            @click="removeCity">
            <i class="fa-solid fa-trash"></i>
            <p>Remove City</p>
        </div>
    </div>
</template>

<script setup>
import axios from "axios";
import { useRoute, useRouter } from "vue-router";

const route = useRoute();
const router = useRouter();

const apiKey = import.meta.env.VITE_weatherToken;

const getWeatherData = async () => {
    try {
        const weatherData = await axios.get(`https://api.openweathermap.org/data/3.0/onecall?lat=${route.query.lat}&lon=${route.query.lng}&exclude={part}&appid=${apiKey}&units=metric`);

        //calculate current date and time
        const localOffset = new Date().getTimezoneOffset() * 60000;
        const utc = weatherData.data.current.dt * 1000 + localOffset;
        weatherData.data.currentTime = utc + 1000 * weatherData.data.timezone_offset;

        //calculate hourly weather offset
        weatherData.data.hourly.forEach((hour) => {
            const utc = hour.dt * 1000 + localOffset;
            hour.currentTime = utc + 1000 * weatherData.data.timezone_offset;
        });
        return weatherData.data;
    } catch (error) {
        console.log(error);
    }
}

const weatherData = await getWeatherData();

const removeCity = () => {
    const cities = JSON.parse(localStorage.getItem('savedCities'));
    const updatedCities = cities.filter((city) => city.id !== route.query.id);
    localStorage.setItem('savedCities', JSON.stringify(updatedCities));
    router.push({
        name: 'home'
    })
}
</script>