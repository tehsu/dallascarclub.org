<template>
  <div>
    <!-- Hero Section -->
    <section class="relative bg-gray-900 text-white">
      <div class="absolute inset-0 bg-gradient-to-r from-black/70 to-black/50 z-10"></div>
      <div class="absolute inset-0 bg-[url('/images/events-hero.jpg')] bg-cover bg-center"></div>
      <div class="container-custom relative z-20 py-16 md:py-24">
        <h1 class="text-4xl md:text-5xl font-bold mb-6">Events</h1>
        <p class="text-xl max-w-2xl">Join us at our upcoming events and connect with fellow car enthusiasts in the Dallas area.</p>
      </div>
    </section>

    <!-- Events Filter -->
    <section class="section bg-white dark:bg-gray-900">
      <div class="container-custom">
        <div class="flex flex-wrap gap-4 mb-8">
          <button 
            @click="activeFilter = 'all'" 
            :class="['btn', activeFilter === 'all' ? 'btn-primary' : 'btn-outline']"
          >
            All Events
          </button>
          <button 
            @click="activeFilter = 'meetups'" 
            :class="['btn', activeFilter === 'meetups' ? 'btn-primary' : 'btn-outline']"
          >
            Meetups
          </button>
          <button 
            @click="activeFilter = 'shows'" 
            :class="['btn', activeFilter === 'shows' ? 'btn-primary' : 'btn-outline']"
          >
            Car Shows
          </button>
          <button 
            @click="activeFilter = 'drives'" 
            :class="['btn', activeFilter === 'drives' ? 'btn-primary' : 'btn-outline']"
          >
            Group Drives
          </button>
          <button 
            @click="activeFilter = 'track'" 
            :class="['btn', activeFilter === 'track' ? 'btn-primary' : 'btn-outline']"
          >
            Track Days
          </button>
        </div>

        <!-- Events Grid -->
        <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
          <!-- Event cards will be filtered based on activeFilter -->
          <div v-for="event in filteredEvents" :key="event.id" class="card hover:shadow-lg">
            <img :src="event.image" :alt="event.title" class="w-full h-48 object-cover">
            <div class="p-6">
              <div class="flex justify-between items-center mb-4">
                <span class="text-sm font-semibold bg-[var(--primary-color)] text-white px-3 py-1 rounded-full">{{ event.date }}</span>
                <span class="text-sm text-gray-600 dark:text-gray-400">{{ event.time }}</span>
              </div>
              <h3 class="text-xl font-bold mb-2">{{ event.title }}</h3>
              <div class="flex items-start space-x-2 mb-4">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mt-0.5 text-gray-500 dark:text-gray-400 flex-shrink-0" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z" />
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 11a3 3 0 11-6 0 3 3 0 016 0z" />
                </svg>
                <span class="text-gray-600 dark:text-gray-400">{{ event.location }}</span>
              </div>
              <p class="text-gray-600 dark:text-gray-400 mb-4">{{ event.description }}</p>
              <div class="flex items-center justify-between">
                <span class="text-sm font-medium px-3 py-1 rounded-full" :class="getEventTypeClass(event.type)">{{ event.type }}</span>
                <button class="btn btn-primary">RSVP</button>
              </div>
            </div>
          </div>
        </div>

        <!-- Load More Button -->
        <div class="text-center mt-12">
          <button @click="loadMoreEvents" class="btn btn-outline">Load More Events</button>
        </div>
      </div>
    </section>

    <!-- Calendar Section -->
    <section class="section bg-gray-100 dark:bg-gray-800">
      <div class="container-custom">
        <h2 class="section-title text-center">Event Calendar</h2>
        <p class="text-center mb-12">View our full event schedule</p>
        
        <!-- Calendar placeholder - in a real implementation, this would be a calendar component -->
        <div class="bg-white dark:bg-gray-900 rounded-lg shadow-md p-6">
          <div class="text-center p-12 border-2 border-dashed border-gray-300 dark:border-gray-700 rounded-lg">
            <h3 class="text-xl font-bold mb-4">Interactive Calendar Coming Soon</h3>
            <p class="text-gray-600 dark:text-gray-400">Our interactive event calendar is under development. Check back soon!</p>
          </div>
        </div>
      </div>
    </section>

    <!-- Host an Event -->
    <section class="section bg-white dark:bg-gray-900">
      <div class="container-custom">
        <div class="bg-gray-100 dark:bg-gray-800 rounded-lg p-8 md:p-12">
          <div class="md:flex items-center justify-between">
            <div class="md:w-2/3 mb-6 md:mb-0">
              <h2 class="text-2xl md:text-3xl font-bold mb-4">Want to host a club event?</h2>
              <p class="text-gray-600 dark:text-gray-400">We're always looking for new event ideas and venues. If you'd like to host or suggest an event, get in touch with our events team.</p>
            </div>
            <div>
              <NuxtLink to="/contact" class="btn btn-primary">Contact Us</NuxtLink>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script setup>
import { ref, computed } from 'vue'

definePageMeta({
  title: 'Events - Dallas Car Club',
  description: 'Upcoming car meets, shows, drives, and track days organized by Dallas Car Club'
})

// Filter state
const activeFilter = ref('all')

// Sample events data (in a real app, this would come from an API)
const events = ref([
  {
    id: 1,
    title: 'Monthly Meetup',
    date: 'Apr 15, 2025',
    time: '7:00 PM',
    location: 'White Rock Lake, Dallas',
    description: 'Join us for our monthly gathering at White Rock Lake. Bring your ride and meet fellow enthusiasts.',
    image: '/images/event1.jpg',
    type: 'Meetup'
  },
  {
    id: 2,
    title: 'Spring Car Show',
    date: 'May 8, 2025',
    time: '10:00 AM',
    location: 'Fair Park, Dallas',
    description: 'Our annual Spring Car Show featuring hundreds of vehicles, food trucks, and family activities.',
    image: '/images/event2.jpg',
    type: 'Car Show'
  },
  {
    id: 3,
    title: 'Track Day',
    date: 'Jun 22, 2025',
    time: '9:00 AM',
    location: 'Texas Motor Speedway',
    description: 'Hit the track with us at Texas Motor Speedway. Open to all skill levels with instructors available.',
    image: '/images/event3.jpg',
    type: 'Track Day'
  },
  {
    id: 4,
    title: 'Hill Country Drive',
    date: 'Jul 12, 2025',
    time: '8:00 AM',
    location: 'Starting at Reunion Tower',
    description: 'A scenic group drive through the Texas Hill Country with stops at local attractions and restaurants.',
    image: '/images/event4.jpg',
    type: 'Group Drive'
  },
  {
    id: 5,
    title: 'Cars & Coffee',
    date: 'Aug 5, 2025',
    time: '8:00 AM',
    location: 'Legacy West, Plano',
    description: 'Early morning car meet with coffee and breakfast. All makes and models welcome.',
    image: '/images/event5.jpg',
    type: 'Meetup'
  },
  {
    id: 6,
    title: 'Charity Auto Show',
    date: 'Sep 18, 2025',
    time: '11:00 AM',
    location: 'Klyde Warren Park',
    description: 'Annual charity auto show benefiting local children\'s hospitals. Registration required for display vehicles.',
    image: '/images/event6.jpg',
    type: 'Car Show'
  }
])

// Filter events based on active filter
const filteredEvents = computed(() => {
  if (activeFilter.value === 'all') {
    return events.value
  } else {
    const filterMap = {
      'meetups': 'Meetup',
      'shows': 'Car Show',
      'drives': 'Group Drive',
      'track': 'Track Day'
    }
    return events.value.filter(event => event.type === filterMap[activeFilter.value])
  }
})

// Function to get class based on event type
const getEventTypeClass = (type) => {
  const classes = {
    'Meetup': 'bg-blue-100 text-blue-800 dark:bg-blue-900 dark:text-blue-200',
    'Car Show': 'bg-purple-100 text-purple-800 dark:bg-purple-900 dark:text-purple-200',
    'Group Drive': 'bg-green-100 text-green-800 dark:bg-green-900 dark:text-green-200',
    'Track Day': 'bg-red-100 text-red-800 dark:bg-red-900 dark:text-red-200'
  }
  return classes[type] || 'bg-gray-100 text-gray-800 dark:bg-gray-700 dark:text-gray-200'
}

// Load more events function (placeholder)
const loadMoreEvents = () => {
  // In a real app, this would load more events from an API
  alert('In a real application, this would load more events from the server.')
}
</script>
