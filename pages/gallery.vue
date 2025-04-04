<template>
  <div>
    <!-- Hero Section -->
    <section class="relative bg-gray-900 text-white">
      <div class="absolute inset-0 bg-gradient-to-r from-black/70 to-black/50 z-10"></div>
      <div class="absolute inset-0 bg-[url('/images/gallery-hero.jpg')] bg-cover bg-center"></div>
      <div class="container-custom relative z-20 py-16 md:py-24">
        <h1 class="text-4xl md:text-5xl font-bold mb-6">Gallery</h1>
        <p class="text-xl max-w-2xl">Explore our collection of member vehicles and club events.</p>
      </div>
    </section>

    <!-- Gallery Filter -->
    <section class="section bg-white dark:bg-gray-900">
      <div class="container-custom">
        <div class="flex flex-wrap gap-4 mb-8">
          <button 
            @click="activeFilter = 'all'" 
            :class="['btn', activeFilter === 'all' ? 'btn-primary' : 'btn-outline']"
          >
            All Photos
          </button>
          <button 
            @click="activeFilter = 'cars'" 
            :class="['btn', activeFilter === 'cars' ? 'btn-primary' : 'btn-outline']"
          >
            Member Cars
          </button>
          <button 
            @click="activeFilter = 'events'" 
            :class="['btn', activeFilter === 'events' ? 'btn-primary' : 'btn-outline']"
          >
            Club Events
          </button>
          <button 
            @click="activeFilter = 'awards'" 
            :class="['btn', activeFilter === 'awards' ? 'btn-primary' : 'btn-outline']"
          >
            Award Winners
          </button>
        </div>

        <!-- Gallery Grid -->
        <div class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-4">
          <div 
            v-for="photo in filteredPhotos" 
            :key="photo.id" 
            class="overflow-hidden rounded-lg cursor-pointer"
            @click="openLightbox(photo)"
          >
            <div class="relative group">
              <img 
                :src="photo.thumbnail" 
                :alt="photo.title" 
                class="w-full h-64 object-cover transition-transform duration-300 group-hover:scale-110"
              >
              <div class="absolute inset-0 bg-black/50 opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-center justify-center">
                <div class="text-white text-center p-4">
                  <h3 class="font-bold">{{ photo.title }}</h3>
                  <p class="text-sm">{{ photo.category }}</p>
                </div>
              </div>
            </div>
          </div>
        </div>

        <!-- Load More Button -->
        <div class="text-center mt-12">
          <button @click="loadMorePhotos" class="btn btn-outline">Load More Photos</button>
        </div>
      </div>
    </section>

    <!-- Lightbox -->
    <div v-if="lightboxOpen" class="fixed inset-0 bg-black/90 z-50 flex items-center justify-center p-4">
      <div class="relative max-w-5xl w-full">
        <!-- Close button -->
        <button @click="closeLightbox" class="absolute top-4 right-4 text-white z-10">
          <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
          </svg>
        </button>
        
        <!-- Navigation buttons -->
        <button @click="prevPhoto" class="absolute left-4 top-1/2 -translate-y-1/2 text-white z-10">
          <svg xmlns="http://www.w3.org/2000/svg" class="h-12 w-12" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 19l-7-7 7-7" />
          </svg>
        </button>
        <button @click="nextPhoto" class="absolute right-4 top-1/2 -translate-y-1/2 text-white z-10">
          <svg xmlns="http://www.w3.org/2000/svg" class="h-12 w-12" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7" />
          </svg>
        </button>
        
        <!-- Image -->
        <img 
          :src="currentPhoto.fullsize" 
          :alt="currentPhoto.title" 
          class="w-full h-auto max-h-[80vh] object-contain mx-auto"
        >
        
        <!-- Caption -->
        <div class="text-white text-center mt-4">
          <h3 class="text-xl font-bold">{{ currentPhoto.title }}</h3>
          <p class="text-gray-300">{{ currentPhoto.description }}</p>
          <p class="text-gray-400 text-sm mt-2">Photo by: {{ currentPhoto.photographer }}</p>
        </div>
      </div>
    </div>

    <!-- Submit Your Photos -->
    <section class="section bg-gray-100 dark:bg-gray-800">
      <div class="container-custom">
        <div class="bg-white dark:bg-gray-900 rounded-lg shadow-md p-8 md:p-12">
          <div class="md:flex items-center justify-between">
            <div class="md:w-2/3 mb-6 md:mb-0">
              <h2 class="text-2xl md:text-3xl font-bold mb-4">Want to showcase your car?</h2>
              <p class="text-gray-600 dark:text-gray-400">We love featuring our members' vehicles! Submit your photos to be included in our gallery.</p>
            </div>
            <div>
              <NuxtLink to="/contact" class="btn btn-primary">Submit Photos</NuxtLink>
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
  title: 'Gallery - Dallas Car Club',
  description: 'Photo gallery of member vehicles and Dallas Car Club events'
})

// Filter state
const activeFilter = ref('all')

// Lightbox state
const lightboxOpen = ref(false)
const currentPhotoIndex = ref(0)

// Sample photos data (in a real app, this would come from an API)
const photos = ref([
  {
    id: 1,
    title: 'Classic Mustang',
    description: 'Restored 1967 Ford Mustang Fastback in Highland Green',
    photographer: 'John Smith',
    thumbnail: '/images/gallery1.jpg',
    fullsize: '/images/gallery1-full.jpg',
    category: 'Member Cars'
  },
  {
    id: 2,
    title: 'Spring Car Show',
    description: 'Lineup of vehicles at our annual Spring Car Show',
    photographer: 'Sarah Johnson',
    thumbnail: '/images/gallery2.jpg',
    fullsize: '/images/gallery2-full.jpg',
    category: 'Club Events'
  },
  {
    id: 3,
    title: 'Track Day Action',
    description: 'Members enjoying a day at Texas Motor Speedway',
    photographer: 'Mike Williams',
    thumbnail: '/images/gallery3.jpg',
    fullsize: '/images/gallery3-full.jpg',
    category: 'Club Events'
  },
  {
    id: 4,
    title: 'Best in Show Winner',
    description: '2023 Best in Show - 1970 Dodge Challenger R/T',
    photographer: 'David Rodriguez',
    thumbnail: '/images/gallery4.jpg',
    fullsize: '/images/gallery4-full.jpg',
    category: 'Award Winners'
  },
  {
    id: 5,
    title: 'Porsche 911',
    description: 'Modified Porsche 911 Turbo with custom wheels',
    photographer: 'Lisa Chen',
    thumbnail: '/images/gallery5.jpg',
    fullsize: '/images/gallery5-full.jpg',
    category: 'Member Cars'
  },
  {
    id: 6,
    title: 'Cars & Coffee Meetup',
    description: 'Morning gathering at our monthly Cars & Coffee event',
    photographer: 'James Wilson',
    thumbnail: '/images/gallery6.jpg',
    fullsize: '/images/gallery6-full.jpg',
    category: 'Club Events'
  },
  {
    id: 7,
    title: 'Vintage Corvette',
    description: 'Immaculately maintained 1963 Corvette Stingray',
    photographer: 'Robert Taylor',
    thumbnail: '/images/gallery7.jpg',
    fullsize: '/images/gallery7-full.jpg',
    category: 'Member Cars'
  },
  {
    id: 8,
    title: 'People\'s Choice Award',
    description: '2024 People\'s Choice Award - BMW M4 Competition',
    photographer: 'Emily Davis',
    thumbnail: '/images/gallery8.jpg',
    fullsize: '/images/gallery8-full.jpg',
    category: 'Award Winners'
  }
])

// Filter photos based on active filter
const filteredPhotos = computed(() => {
  if (activeFilter.value === 'all') {
    return photos.value
  } else {
    const filterMap = {
      'cars': 'Member Cars',
      'events': 'Club Events',
      'awards': 'Award Winners'
    }
    return photos.value.filter(photo => photo.category === filterMap[activeFilter.value])
  }
})

// Current photo for lightbox
const currentPhoto = computed(() => {
  return filteredPhotos.value[currentPhotoIndex.value] || {}
})

// Lightbox functions
const openLightbox = (photo) => {
  currentPhotoIndex.value = filteredPhotos.value.findIndex(p => p.id === photo.id)
  lightboxOpen.value = true
  // Prevent scrolling when lightbox is open
  document.body.style.overflow = 'hidden'
}

const closeLightbox = () => {
  lightboxOpen.value = false
  // Restore scrolling
  document.body.style.overflow = ''
}

const nextPhoto = () => {
  if (currentPhotoIndex.value < filteredPhotos.value.length - 1) {
    currentPhotoIndex.value++
  } else {
    currentPhotoIndex.value = 0
  }
}

const prevPhoto = () => {
  if (currentPhotoIndex.value > 0) {
    currentPhotoIndex.value--
  } else {
    currentPhotoIndex.value = filteredPhotos.value.length - 1
  }
}

// Load more photos function (placeholder)
const loadMorePhotos = () => {
  // In a real app, this would load more photos from an API
  alert('In a real application, this would load more photos from the server.')
}

// Handle keyboard navigation for lightbox
onMounted(() => {
  window.addEventListener('keydown', handleKeyDown)
})

onUnmounted(() => {
  window.removeEventListener('keydown', handleKeyDown)
})

const handleKeyDown = (e) => {
  if (!lightboxOpen.value) return
  
  if (e.key === 'Escape') {
    closeLightbox()
  } else if (e.key === 'ArrowRight') {
    nextPhoto()
  } else if (e.key === 'ArrowLeft') {
    prevPhoto()
  }
}
</script>
