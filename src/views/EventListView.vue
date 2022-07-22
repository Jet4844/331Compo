<template>
  <h1>Events for Good</h1>
  <div class="events">
    <!-- <img alt="Vue logo" src="../assets/logo.png" />
    <HelloWorld msg="Welcome to Your Vue.js App" /> -->
    <EventCard v-for="event in events" :key="event.id" :event="event" />
  </div>
  <div class="category">
    <Category v-for="event in events" :key="event.id" :event="event" />
  </div>
</template>

<script>
// @ is an alias to /src
import EventCard from '@/components/EventCard.vue'
import Category from '@/components/Category.vue'

export default {
  name: 'EventListView',
  components: {
    EventCard,
    Category
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
          date: 'January 22, 2022',
          time: '12:00',
          petsAllowed: false,
          organizer: 'Carey Wales'
        }
      ]
    }
  }
}
</script>
<style scoped>
.events {
  display: flex;
  flex-direction: column;
  align-items: center;
}
.category {
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: right;
}
</style>
