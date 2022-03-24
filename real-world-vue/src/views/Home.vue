<template>
  <h1>Events for Good</h1>
  <div class="events">
    <EventCard v-for="event in events" :key="event.id" :event="event" />
  </div>
</template>

<script>
// @ is an alias to /src
import EventCard from '@/components/EventCard.vue'

export default {
  name: 'HomeView',
  components: {
    EventCard,
  },
  data() {
    return {
      events: [
        {
          id: 5928101,
          category: 'animal welfare',
          title: 'Cat Adoption Day',
          description: 'Find your new feline friend at this event.',
          location: 'Meow Town',
          date: 'January 27, 2022',
          time: '12:00',
          petsAllowed: true,
          organizer: 'Kay Laydee',
        },
        {
          id: 5928273,
          category: 'food',
          title: 'Community Gardening',
          description: 'Planting edible plants',
          location: 'Floracity',
          date: 'January 31, 2022',
          time: '14:00',
          petsAllowed: true,
          organizer: 'Sharon Meese',
        },
        {
          id: 592781231,
          category: 'sustainability',
          title: 'Beach Cleanup',
          description: 'Help us clean up the shore.',
          location: 'St. Tropez',
          date: 'February 14th, 2022',
          time: '10:00',
          petsAllowed: true,
          organizer: 'Carey Wales',
        },
      ],
    }
  },
}
</script>

<style scoped>
.events {
  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>
