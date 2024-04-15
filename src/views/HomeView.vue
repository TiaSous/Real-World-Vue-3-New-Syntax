<script setup>
import EventCard from '../components/EventCard.vue';
import { ref } from 'vue'

const events = ref([
{  
  id: 5928101,
  category: 'animal welfare',
  title: 'Cat Adoption Day',
  description: 'Find your new feline friend at this event.',
  location: 'Meow Town',
  date: 'January 28, 2022',
  time: '12:00',
  petsAllowed: true,
  organizer: 'Kat Laydee',
},
{  
  id: 4582797,
  category: 'food',
  title: 'Eat in restaurent',
  description: 'Join us to test a new restaurant.',
  location: 'Flora City',
  date: 'March 21, 2022',
  time: '10:00',
  petsAllowed: true,
  organizer: 'Fern Pollin',
},
{  
  id: 8419988,
  category: 'work',
  title: 'Create an API',
  description: 'Help me to crate an API',
  location: 'Beach City',
  date: 'July 22, 2022',
  time: '11:00',
  petsAllowed: true,
  organizer: 'Carvey Wales',
},
])
</script>

<template>
  <h1>Events For Good</h1>
  <div class="events">
    <EventCard v-for="event in events" :key="event.id" :event="event"/>
  </div>
</template>

<style scoped>
.events {
  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>