<template>
  <main>
    <Map :locations="locations" />
    <p>Click on the pins above to see more information ^</p>
    <h3>Showing Locations:</h3>

    <div v-for="(information, name) in locations">
      <h4>{{ name }}</h4>
      <ul>
        <li>
          {{ information.coordinates }}
        </li>
      </ul>
    </div>


  </main>
</template>

<script setup>
import Map from '@/components/Map.vue';

const locations = {
  "Charles Library": {"coordinates": [39.9817, -75.1553], "description": "I have elvators"},
  "City Hall": {"coordinates": [39.9526, -75.1652], "description": "I have tacktile ground surface indactors"}
}
</script>