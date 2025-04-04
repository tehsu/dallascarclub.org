<template>
  <div>
    <!-- Hero Section -->
    <section class="relative bg-gray-900 text-white">
      <div class="absolute inset-0 bg-gradient-to-r from-black/70 to-black/50 z-10"></div>
      <div class="absolute inset-0 bg-[url('/images/hero-bg.jpg')] bg-cover bg-center"></div>
      <div class="container-custom relative z-20 py-20 md:py-32 flex flex-col items-center text-center">
        <h1 class="text-4xl md:text-6xl font-bold mb-6">Welcome to Dallas Car Club</h1>
        <p class="text-xl md:text-2xl mb-8 max-w-3xl">Connecting car enthusiasts across Dallas since 1995</p>
        <div class="flex flex-col sm:flex-row gap-4">
          <NuxtLink to="/membership" class="btn btn-primary">Join the Club</NuxtLink>
          <NuxtLink to="/events" class="btn btn-outline">Upcoming Events</NuxtLink>
        </div>
      </div>
    </section>

    <!-- About Section -->
    <section class="section bg-white dark:bg-gray-900">
      <div class="container-custom">
        <div class="grid md:grid-cols-2 gap-12 items-center">
          <div>
            <h2 class="section-title">About Our Club</h2>
            <p class="mb-6">Dallas Car Club is a community of passionate car enthusiasts dedicated to celebrating automotive culture in the Dallas-Fort Worth area. From classic cars to modern supercars, we welcome all automotive enthusiasts.</p>
            <p class="mb-6">Our club hosts regular meetups, drives, car shows, and social events throughout the year, providing opportunities for members to showcase their vehicles, share knowledge, and build lasting friendships.</p>
            <NuxtLink to="/about" class="btn btn-primary">Learn More</NuxtLink>
          </div>
          <div class="rounded-lg overflow-hidden shadow-xl">
            <img src="/images/about-club.jpg" alt="Car club members" class="w-full h-auto">
          </div>
        </div>
      </div>
    </section>

    <!-- Featured Events -->
    <section class="section bg-gray-100 dark:bg-gray-800">
      <div class="container-custom">
        <h2 class="section-title text-center">Upcoming Events</h2>
        <p class="text-center mb-12 max-w-3xl mx-auto">Join us at our upcoming events and connect with fellow car enthusiasts</p>
        
        <div class="grid md:grid-cols-3 gap-8">
          <!-- Event 1 -->
          <div class="card hover:shadow-lg">
            <img src="/images/event1.jpg" alt="Monthly Meetup" class="w-full h-48 object-cover">
            <div class="p-6">
              <div class="flex justify-between items-center mb-4">
                <span class="text-sm font-semibold bg-[var(--primary-color)] text-white px-3 py-1 rounded-full">Apr 15, 2025</span>
                <span class="text-sm text-gray-600 dark:text-gray-400">7:00 PM</span>
              </div>
              <h3 class="text-xl font-bold mb-2">Monthly Meetup</h3>
              <p class="text-gray-600 dark:text-gray-400 mb-4">Join us for our monthly gathering at White Rock Lake. Bring your ride and meet fellow enthusiasts.</p>
              <NuxtLink to="/events" class="text-[var(--primary-color)] font-medium hover:underline">Learn More →</NuxtLink>
            </div>
          </div>
          
          <!-- Event 2 -->
          <div class="card hover:shadow-lg">
            <img src="/images/event2.jpg" alt="Spring Car Show" class="w-full h-48 object-cover">
            <div class="p-6">
              <div class="flex justify-between items-center mb-4">
                <span class="text-sm font-semibold bg-[var(--primary-color)] text-white px-3 py-1 rounded-full">May 8, 2025</span>
                <span class="text-sm text-gray-600 dark:text-gray-400">10:00 AM</span>
              </div>
              <h3 class="text-xl font-bold mb-2">Spring Car Show</h3>
              <p class="text-gray-600 dark:text-gray-400 mb-4">Our annual Spring Car Show featuring hundreds of vehicles, food trucks, and family activities.</p>
              <NuxtLink to="/events" class="text-[var(--primary-color)] font-medium hover:underline">Learn More →</NuxtLink>
            </div>
          </div>
          
          <!-- Event 3 -->
          <div class="card hover:shadow-lg">
            <img src="/images/event3.jpg" alt="Track Day" class="w-full h-48 object-cover">
            <div class="p-6">
              <div class="flex justify-between items-center mb-4">
                <span class="text-sm font-semibold bg-[var(--primary-color)] text-white px-3 py-1 rounded-full">Jun 22, 2025</span>
                <span class="text-sm text-gray-600 dark:text-gray-400">9:00 AM</span>
              </div>
              <h3 class="text-xl font-bold mb-2">Track Day</h3>
              <p class="text-gray-600 dark:text-gray-400 mb-4">Hit the track with us at Texas Motor Speedway. Open to all skill levels with instructors available.</p>
              <NuxtLink to="/events" class="text-[var(--primary-color)] font-medium hover:underline">Learn More →</NuxtLink>
            </div>
          </div>
        </div>
        
        <div class="text-center mt-12">
          <NuxtLink to="/events" class="btn btn-primary">View All Events</NuxtLink>
        </div>
      </div>
    </section>

    <!-- Membership Benefits -->
    <section class="section bg-white dark:bg-gray-900">
      <div class="container-custom">
        <h2 class="section-title text-center">Membership Benefits</h2>
        <p class="text-center mb-12 max-w-3xl mx-auto">Join our community and enjoy exclusive benefits</p>
        
        <div class="grid md:grid-cols-4 gap-6">
          <div class="text-center p-6">
            <div class="bg-[var(--primary-color)]/10 w-16 h-16 mx-auto rounded-full flex items-center justify-center mb-4">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8 text-[var(--primary-color)]" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 20h5v-2a3 3 0 00-5.356-1.857M17 20H7m10 0v-2c0-.656-.126-1.283-.356-1.857M7 20H2v-2a3 3 0 015.356-1.857M7 20v-2c0-.656.126-1.283.356-1.857m0 0a5.002 5.002 0 019.288 0M15 7a3 3 0 11-6 0 3 3 0 016 0zm6 3a2 2 0 11-4 0 2 2 0 014 0zM7 10a2 2 0 11-4 0 2 2 0 014 0z" />
              </svg>
            </div>
            <h3 class="text-xl font-bold mb-2">Community</h3>
            <p class="text-gray-600 dark:text-gray-400">Connect with like-minded car enthusiasts and build lasting friendships</p>
          </div>
          
          <div class="text-center p-6">
            <div class="bg-[var(--primary-color)]/10 w-16 h-16 mx-auto rounded-full flex items-center justify-center mb-4">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8 text-[var(--primary-color)]" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 7V3m8 4V3m-9 8h10M5 21h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v12a2 2 0 002 2z" />
              </svg>
            </div>
            <h3 class="text-xl font-bold mb-2">Events</h3>
            <p class="text-gray-600 dark:text-gray-400">Access to exclusive club events, drives, and track days</p>
          </div>
          
          <div class="text-center p-6">
            <div class="bg-[var(--primary-color)]/10 w-16 h-16 mx-auto rounded-full flex items-center justify-center mb-4">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8 text-[var(--primary-color)]" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8c-1.657 0-3 .895-3 2s1.343 2 3 2 3 .895 3 2-1.343 2-3 2m0-8c1.11 0 2.08.402 2.599 1M12 8V7m0 1v8m0 0v1m0-1c-1.11 0-2.08-.402-2.599-1M21 12a9 9 0 11-18 0 9 9 0 0118 0z" />
              </svg>
            </div>
            <h3 class="text-xl font-bold mb-2">Discounts</h3>
            <p class="text-gray-600 dark:text-gray-400">Exclusive discounts with our partner shops and service providers</p>
          </div>
          
          <div class="text-center p-6">
            <div class="bg-[var(--primary-color)]/10 w-16 h-16 mx-auto rounded-full flex items-center justify-center mb-4">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8 text-[var(--primary-color)]" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9.663 17h4.673M12 3v1m6.364 1.636l-.707.707M21 12h-1M4 12H3m3.343-5.657l-.707-.707m2.828 9.9a5 5 0 117.072 0l-.548.547A3.374 3.374 0 0014 18.469V19a2 2 0 11-4 0v-.531c0-.895-.356-1.754-.988-2.386l-.548-.547z" />
              </svg>
            </div>
            <h3 class="text-xl font-bold mb-2">Knowledge</h3>
            <p class="text-gray-600 dark:text-gray-400">Access to workshops, tech sessions, and automotive expertise</p>
          </div>
        </div>
        
        <div class="text-center mt-12">
          <NuxtLink to="/membership" class="btn btn-primary">Join Now</NuxtLink>
        </div>
      </div>
    </section>

    <!-- Gallery Preview -->
    <section class="section bg-gray-100 dark:bg-gray-800">
      <div class="container-custom">
        <h2 class="section-title text-center">Gallery Highlights</h2>
        <p class="text-center mb-12 max-w-3xl mx-auto">Check out some of our members' amazing vehicles</p>
        
        <div class="grid grid-cols-2 md:grid-cols-4 gap-4">
          <div class="overflow-hidden rounded-lg">
            <img src="/images/gallery1.jpg" alt="Car 1" class="w-full h-64 object-cover hover:scale-110 transition-transform duration-300">
          </div>
          <div class="overflow-hidden rounded-lg">
            <img src="/images/gallery2.jpg" alt="Car 2" class="w-full h-64 object-cover hover:scale-110 transition-transform duration-300">
          </div>
          <div class="overflow-hidden rounded-lg">
            <img src="/images/gallery3.jpg" alt="Car 3" class="w-full h-64 object-cover hover:scale-110 transition-transform duration-300">
          </div>
          <div class="overflow-hidden rounded-lg">
            <img src="/images/gallery4.jpg" alt="Car 4" class="w-full h-64 object-cover hover:scale-110 transition-transform duration-300">
          </div>
        </div>
        
        <div class="text-center mt-12">
          <NuxtLink to="/gallery" class="btn btn-primary">View Full Gallery</NuxtLink>
        </div>
      </div>
    </section>

    <!-- Testimonials -->
    <section class="section bg-white dark:bg-gray-900">
      <div class="container-custom">
        <h2 class="section-title text-center">What Our Members Say</h2>
        <div class="grid md:grid-cols-3 gap-8 mt-12">
          <div class="bg-gray-50 dark:bg-gray-800 p-8 rounded-lg shadow-md">
            <div class="flex items-center mb-4">
              <div class="text-[var(--primary-color)]">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8" fill="currentColor" viewBox="0 0 24 24">
                  <path d="M13 14.725c0-5.141 3.892-10.519 10-11.725l.984 2.126c-2.215.835-4.163 3.742-4.38 5.746 2.491.392 4.396 2.547 4.396 5.149 0 3.182-2.584 4.979-5.199 4.979-3.015 0-5.801-2.305-5.801-6.275zm-13 0c0-5.141 3.892-10.519 10-11.725l.984 2.126c-2.215.835-4.163 3.742-4.38 5.746 2.491.392 4.396 2.547 4.396 5.149 0 3.182-2.584 4.979-5.199 4.979-3.015 0-5.801-2.305-5.801-6.275z" />
                </svg>
              </div>
            </div>
            <p class="mb-4 text-gray-600 dark:text-gray-300 italic">Joining Dallas Car Club was one of the best decisions I've made. I've met amazing people who share my passion for cars and have learned so much from fellow members.</p>
            <div class="flex items-center">
              <img src="/images/member1.jpg" alt="Member" class="w-12 h-12 rounded-full mr-4">
              <div>
                <h4 class="font-bold">Michael Johnson</h4>
                <p class="text-sm text-gray-500 dark:text-gray-400">Member since 2020</p>
              </div>
            </div>
          </div>
          
          <div class="bg-gray-50 dark:bg-gray-800 p-8 rounded-lg shadow-md">
            <div class="flex items-center mb-4">
              <div class="text-[var(--primary-color)]">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8" fill="currentColor" viewBox="0 0 24 24">
                  <path d="M13 14.725c0-5.141 3.892-10.519 10-11.725l.984 2.126c-2.215.835-4.163 3.742-4.38 5.746 2.491.392 4.396 2.547 4.396 5.149 0 3.182-2.584 4.979-5.199 4.979-3.015 0-5.801-2.305-5.801-6.275zm-13 0c0-5.141 3.892-10.519 10-11.725l.984 2.126c-2.215.835-4.163 3.742-4.38 5.746 2.491.392 4.396 2.547 4.396 5.149 0 3.182-2.584 4.979-5.199 4.979-3.015 0-5.801-2.305-5.801-6.275z" />
                </svg>
              </div>
            </div>
            <p class="mb-4 text-gray-600 dark:text-gray-300 italic">The track days organized by the club are fantastic! As a new performance driver, I've received great coaching and improved my skills tremendously.</p>
            <div class="flex items-center">
              <img src="/images/member2.jpg" alt="Member" class="w-12 h-12 rounded-full mr-4">
              <div>
                <h4 class="font-bold">Sarah Williams</h4>
                <p class="text-sm text-gray-500 dark:text-gray-400">Member since 2022</p>
              </div>
            </div>
          </div>
          
          <div class="bg-gray-50 dark:bg-gray-800 p-8 rounded-lg shadow-md">
            <div class="flex items-center mb-4">
              <div class="text-[var(--primary-color)]">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8" fill="currentColor" viewBox="0 0 24 24">
                  <path d="M13 14.725c0-5.141 3.892-10.519 10-11.725l.984 2.126c-2.215.835-4.163 3.742-4.38 5.746 2.491.392 4.396 2.547 4.396 5.149 0 3.182-2.584 4.979-5.199 4.979-3.015 0-5.801-2.305-5.801-6.275zm-13 0c0-5.141 3.892-10.519 10-11.725l.984 2.126c-2.215.835-4.163 3.742-4.38 5.746 2.491.392 4.396 2.547 4.396 5.149 0 3.182-2.584 4.979-5.199 4.979-3.015 0-5.801-2.305-5.801-6.275z" />
                </svg>
              </div>
            </div>
            <p class="mb-4 text-gray-600 dark:text-gray-300 italic">The discounts at local shops have saved me thousands on my project car. Plus, the technical knowledge shared by other members is invaluable!</p>
            <div class="flex items-center">
              <img src="/images/member3.jpg" alt="Member" class="w-12 h-12 rounded-full mr-4">
              <div>
                <h4 class="font-bold">David Rodriguez</h4>
                <p class="text-sm text-gray-500 dark:text-gray-400">Member since 2019</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script setup>
definePageMeta({
  title: 'Home - Dallas Car Club',
  description: 'Welcome to Dallas Car Club - Connecting car enthusiasts in Dallas, Texas since 1995'
})
</script>
