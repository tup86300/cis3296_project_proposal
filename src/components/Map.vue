<template>
    <div id="map"></div>
</template>

<script setup>
import { onMounted } from 'vue'

const props = defineProps({
    locations: {
        type: Object,
        required: true
    }
})

onMounted(() => {
    const locations = props.locations

    const map = window.L.map('map').setView([39.9526, -75.1652], 12.5)

    window.L.tileLayer('https://tile.openstreetmap.org/{z}/{x}/{y}.png', {
        maxZoom: 19,
        attribution: '&copy; OpenStreetMap'
    }).addTo(map)

    for (const name in locations) {
        let location = locations[name];
        const mapsUrl = `https://www.google.com/maps/dir/?api=1&destination=${location.coordinates[0]},${location.coordinates[1]}`;
        window.L.marker(location.coordinates).addTo(map)
            .bindPopup(`${location.description}<br><a href="${mapsUrl}" target="_blank">Get Directions</a>`)
            .addTo(map)
    }
})
</script>

<style scoped>
#map {
    height: 500px;
    width: 600px;
}
</style>