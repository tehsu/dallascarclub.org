<template>
  <div class="min-h-screen flex flex-col">
    <header class="bg-white dark:bg-gray-900 shadow-md sticky top-0 z-50">
      <nav class="container-custom py-4">
        <div class="flex items-center justify-between">
          <NuxtLink to="/" class="flex items-center space-x-2">
            <span class="text-2xl font-bold text-[var(--primary-color)]">Dallas Car Club</span>
          </NuxtLink>
          
          <div class="hidden md:flex items-center space-x-8">
            <NuxtLink to="/" class="nav-link">Home</NuxtLink>
            <NuxtLink to="/events" class="nav-link">Events</NuxtLink>
            <NuxtLink to="/gallery" class="nav-link">Gallery</NuxtLink>
            <NuxtLink to="/membership" class="nav-link">Membership</NuxtLink>
            <NuxtLink to="/about" class="nav-link">About Us</NuxtLink>
            <NuxtLink to="/contact" class="nav-link">Contact</NuxtLink>
          </div>
          
          <button @click="toggleMobileMenu" class="md:hidden text-gray-800 dark:text-white">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path v-if="!mobileMenuOpen" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
              <path v-else stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
            </svg>
          </button>
        </div>
        
        <!-- Mobile Menu -->
        <div v-if="mobileMenuOpen" class="md:hidden mt-4 pb-4">
          <div class="flex flex-col space-y-4">
            <NuxtLink to="/" class="nav-link" @click="mobileMenuOpen = false">Home</NuxtLink>
            <NuxtLink to="/events" class="nav-link" @click="mobileMenuOpen = false">Events</NuxtLink>
            <NuxtLink to="/gallery" class="nav-link" @click="mobileMenuOpen = false">Gallery</NuxtLink>
            <NuxtLink to="/membership" class="nav-link" @click="mobileMenuOpen = false">Membership</NuxtLink>
            <NuxtLink to="/about" class="nav-link" @click="mobileMenuOpen = false">About Us</NuxtLink>
            <NuxtLink to="/contact" class="nav-link" @click="mobileMenuOpen = false">Contact</NuxtLink>
          </div>
        </div>
      </nav>
    </header>
    
    <main class="flex-grow">
      <slot />
    </main>
    
    <footer class="bg-[var(--secondary-color)] text-white py-12">
      <div class="container-custom">
        <div class="grid grid-cols-1 md:grid-cols-4 gap-8">
          <div>
            <h3 class="text-xl font-bold mb-4">Dallas Car Club</h3>
            <p class="mb-4">Connecting car enthusiasts in Dallas since 1995.</p>
            <div class="flex space-x-4">
              <a href="#" class="text-white hover:text-[var(--primary-color)]">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="currentColor" viewBox="0 0 24 24">
                  <path d="M22.675 0h-21.35c-.732 0-1.325.593-1.325 1.325v21.351c0 .731.593 1.324 1.325 1.324h11.495v-9.294h-3.128v-3.622h3.128v-2.671c0-3.1 1.893-4.788 4.659-4.788 1.325 0 2.463.099 2.795.143v3.24l-1.918.001c-1.504 0-1.795.715-1.795 1.763v2.313h3.587l-.467 3.622h-3.12v9.293h6.116c.73 0 1.323-.593 1.323-1.325v-21.35c0-.732-.593-1.325-1.325-1.325z" />
                </svg>
              </a>
              <a href="#" class="text-white hover:text-[var(--primary-color)]">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="currentColor" viewBox="0 0 24 24">
                  <path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zm0-2.163c-3.259 0-3.667.014-4.947.072-4.358.2-6.78 2.618-6.98 6.98-.059 1.281-.073 1.689-.073 4.948 0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98 1.281.058 1.689.072 4.948.072 3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98-1.281-.059-1.69-.073-4.949-.073zm0 5.838c-3.403 0-6.162 2.759-6.162 6.162s2.759 6.163 6.162 6.163 6.162-2.759 6.162-6.163c0-3.403-2.759-6.162-6.162-6.162zm0 10.162c-2.209 0-4-1.79-4-4 0-2.209 1.791-4 4-4s4 1.791 4 4c0 2.21-1.791 4-4 4zm6.406-11.845c-.796 0-1.441.645-1.441 1.44s.645 1.44 1.441 1.44c.795 0 1.439-.645 1.439-1.44s-.644-1.44-1.439-1.44z" />
                </svg>
              </a>
              <a href="#" class="text-white hover:text-[var(--primary-color)]">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="currentColor" viewBox="0 0 24 24">
                  <path d="M24 4.557c-.883.392-1.832.656-2.828.775 1.017-.609 1.798-1.574 2.165-2.724-.951.564-2.005.974-3.127 1.195-.897-.957-2.178-1.555-3.594-1.555-3.179 0-5.515 2.966-4.797 6.045-4.091-.205-7.719-2.165-10.148-5.144-1.29 2.213-.669 5.108 1.523 6.574-.806-.026-1.566-.247-2.229-.616-.054 2.281 1.581 4.415 3.949 4.89-.693.188-1.452.232-2.224.084.626 1.956 2.444 3.379 4.6 3.419-2.07 1.623-4.678 2.348-7.29 2.04 2.179 1.397 4.768 2.212 7.548 2.212 9.142 0 14.307-7.721 13.995-14.646.962-.695 1.797-1.562 2.457-2.549z" />
                </svg>
              </a>
              <a href="#" class="text-white hover:text-[var(--primary-color)]">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="currentColor" viewBox="0 0 24 24">
                  <path d="M19.615 3.184c-3.604-.246-11.631-.245-15.23 0-3.897.266-4.356 2.62-4.385 8.816.029 6.185.484 8.549 4.385 8.816 3.6.245 11.626.246 15.23 0 3.897-.266 4.356-2.62 4.385-8.816-.029-6.185-.484-8.549-4.385-8.816zm-10.615 12.816v-8l8 3.993-8 4.007z" />
                </svg>
              </a>
            </div>
          </div>
          
          <div>
            <h3 class="text-xl font-bold mb-4">Quick Links</h3>
            <ul class="space-y-2">
              <li><NuxtLink to="/" class="hover:text-[var(--primary-color)]">Home</NuxtLink></li>
              <li><NuxtLink to="/events" class="hover:text-[var(--primary-color)]">Events</NuxtLink></li>
              <li><NuxtLink to="/gallery" class="hover:text-[var(--primary-color)]">Gallery</NuxtLink></li>
              <li><NuxtLink to="/membership" class="hover:text-[var(--primary-color)]">Membership</NuxtLink></li>
              <li><NuxtLink to="/about" class="hover:text-[var(--primary-color)]">About Us</NuxtLink></li>
              <li><NuxtLink to="/contact" class="hover:text-[var(--primary-color)]">Contact</NuxtLink></li>
            </ul>
          </div>
          
          <div>
            <h3 class="text-xl font-bold mb-4">Contact Us</h3>
            <ul class="space-y-2">
              <li class="flex items-start space-x-2">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 mt-0.5 flex-shrink-0" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z" />
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 11a3 3 0 11-6 0 3 3 0 016 0z" />
                </svg>
                <span>123 Main Street, Dallas, TX 75201</span>
              </li>
              <li class="flex items-start space-x-2">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 mt-0.5 flex-shrink-0" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z" />
                </svg>
                <span>info@dallascarclub.org</span>
              </li>
              <li class="flex items-start space-x-2">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 mt-0.5 flex-shrink-0" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z" />
                </svg>
                <span>(214) 555-1234</span>
              </li>
            </ul>
          </div>
          
          <div>
            <h3 class="text-xl font-bold mb-4">Newsletter</h3>
            <p class="mb-4">Subscribe to our newsletter for the latest updates and events.</p>
            <form @submit.prevent="subscribeNewsletter" class="space-y-2">
              <input type="email" v-model="newsletterEmail" placeholder="Your email" required class="w-full px-4 py-2 rounded-md bg-white/10 border border-white/20 focus:outline-none focus:ring-2 focus:ring-[var(--primary-color)]">
              <button type="submit" class="w-full btn btn-primary">Subscribe</button>
            </form>
          </div>
        </div>
        
        <div class="mt-8 pt-8 border-t border-white/20 text-center">
          <p>&copy; {{ new Date().getFullYear() }} Dallas Car Club. All rights reserved.</p>
        </div>
      </div>
    </footer>
  </div>
</template>

<script setup>
const mobileMenuOpen = ref(false)
const newsletterEmail = ref('')

const toggleMobileMenu = () => {
  mobileMenuOpen.value = !mobileMenuOpen.value
}

const subscribeNewsletter = () => {
  // Here you would typically send the email to your backend
  alert(`Thank you for subscribing with ${newsletterEmail.value}!`)
  newsletterEmail.value = ''
}
</script>

<style scoped>
.nav-link {
  @apply text-gray-700 dark:text-gray-300 hover:text-[var(--primary-color)] dark:hover:text-[var(--primary-color)] font-medium transition-colors duration-200;
}

.nav-link.router-link-active {
  @apply text-[var(--primary-color)] font-semibold;
}

.nav-link {
  @apply text-gray-700 dark:text-gray-300 hover:text-[var(--primary-color)] dark:hover:text-[var(--primary-color)] transition-colors duration-200;
}
</style>
