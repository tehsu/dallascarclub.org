<template>
  <div>
    <!-- Hero Section -->
    <section class="relative bg-gray-900 text-white">
      <div class="absolute inset-0 bg-gradient-to-r from-black/70 to-black/50 z-10"></div>
      <div class="absolute inset-0 bg-[url('/images/about-hero.jpg')] bg-cover bg-center"></div>
      <div class="container-custom relative z-20 py-16 md:py-24">
        <h1 class="text-4xl md:text-5xl font-bold mb-6">About Us</h1>
        <p class="text-xl max-w-2xl">Learn about our club's history, mission, and the passionate team behind Dallas Car Club.</p>
      </div>
    </section>

    <!-- Our Story -->
    <section class="section bg-white dark:bg-gray-900">
      <div class="container-custom">
        <div class="grid md:grid-cols-2 gap-12 items-center">
          <div>
            <h2 class="section-title">Our Story</h2>
            <p class="mb-6">Founded in 1995 by a small group of car enthusiasts, Dallas Car Club began as informal weekend meetups at local parking lots. What started as a handful of friends sharing their passion for cars has grown into one of the largest and most respected car clubs in the Dallas-Fort Worth area.</p>
            <p class="mb-6">Over the years, we've expanded our activities to include regular car shows, track days, group drives, and community service events. Our club has been featured in local and national automotive publications and has raised over $100,000 for various charities through our annual charity car shows.</p>
            <p>Today, with over 500 active members, we continue to celebrate our love for all things automotive while fostering a welcoming community for enthusiasts of all backgrounds and interests.</p>
          </div>
          <div class="rounded-lg overflow-hidden shadow-xl">
            <img src="/images/club-history.jpg" alt="Club history" class="w-full h-auto">
          </div>
        </div>
      </div>
    </section>

    <!-- Our Mission -->
    <section class="section bg-gray-100 dark:bg-gray-800">
      <div class="container-custom">
        <h2 class="section-title text-center">Our Mission</h2>
        <div class="max-w-3xl mx-auto text-center">
          <p class="text-xl mb-8">To foster a vibrant community of automotive enthusiasts, promote responsible car culture, and share our passion with the greater Dallas area.</p>
          
          <div class="grid md:grid-cols-3 gap-8 mt-12">
            <div class="card p-6 hover:shadow-lg">
              <div class="bg-[var(--primary-color)]/10 w-16 h-16 mx-auto rounded-full flex items-center justify-center mb-4">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8 text-[var(--primary-color)]" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 20h5v-2a3 3 0 00-5.356-1.857M17 20H7m10 0v-2c0-.656-.126-1.283-.356-1.857M7 20H2v-2a3 3 0 015.356-1.857M7 20v-2c0-.656.126-1.283.356-1.857m0 0a5.002 5.002 0 019.288 0M15 7a3 3 0 11-6 0 3 3 0 016 0zm6 3a2 2 0 11-4 0 2 2 0 014 0zM7 10a2 2 0 11-4 0 2 2 0 014 0z" />
                </svg>
              </div>
              <h3 class="text-xl font-bold mb-2">Community</h3>
              <p class="text-gray-600 dark:text-gray-400">Building a diverse and inclusive community of car enthusiasts who support and learn from each other.</p>
            </div>
            
            <div class="card p-6 hover:shadow-lg">
              <div class="bg-[var(--primary-color)]/10 w-16 h-16 mx-auto rounded-full flex items-center justify-center mb-4">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8 text-[var(--primary-color)]" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9.663 17h4.673M12 3v1m6.364 1.636l-.707.707M21 12h-1M4 12H3m3.343-5.657l-.707-.707m2.828 9.9a5 5 0 117.072 0l-.548.547A3.374 3.374 0 0014 18.469V19a2 2 0 11-4 0v-.531c0-.895-.356-1.754-.988-2.386l-.548-.547z" />
                </svg>
              </div>
              <h3 class="text-xl font-bold mb-2">Education</h3>
              <p class="text-gray-600 dark:text-gray-400">Sharing knowledge and skills to help members better understand, maintain, and enjoy their vehicles.</p>
            </div>
            
            <div class="card p-6 hover:shadow-lg">
              <div class="bg-[var(--primary-color)]/10 w-16 h-16 mx-auto rounded-full flex items-center justify-center mb-4">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8 text-[var(--primary-color)]" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 12a9 9 0 01-9 9m9-9a9 9 0 00-9-9m9 9H3m9 9a9 9 0 01-9-9m9 9c1.657 0 3-4.03 3-9s-1.343-9-3-9m0 18c-1.657 0-3-4.03-3-9s1.343-9 3-9m-9 9a9 9 0 019-9" />
                </svg>
              </div>
              <h3 class="text-xl font-bold mb-2">Outreach</h3>
              <p class="text-gray-600 dark:text-gray-400">Engaging with the broader community through charity events and promoting responsible automotive culture.</p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Leadership Team -->
    <section class="section bg-white dark:bg-gray-900">
      <div class="container-custom">
        <h2 class="section-title text-center">Our Leadership Team</h2>
        <p class="text-center mb-12 max-w-3xl mx-auto">Meet the dedicated individuals who help organize and run Dallas Car Club</p>
        
        <div class="grid md:grid-cols-4 gap-8">
          <!-- Team Member 1 -->
          <div class="card overflow-hidden hover:shadow-lg">
            <img src="/images/team1.jpg" alt="Michael Thompson" class="w-full h-64 object-cover">
            <div class="p-6">
              <h3 class="text-xl font-bold mb-1">Michael Thompson</h3>
              <p class="text-[var(--primary-color)] mb-4">President</p>
              <p class="text-gray-600 dark:text-gray-400 mb-4">Classic car enthusiast and founder of Dallas Car Club. Driving a restored 1968 Ford Mustang.</p>
              <div class="flex space-x-3">
                <a href="#" class="text-gray-400 hover:text-[var(--primary-color)]">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="currentColor" viewBox="0 0 24 24">
                    <path d="M22.675 0h-21.35c-.732 0-1.325.593-1.325 1.325v21.351c0 .731.593 1.324 1.325 1.324h11.495v-9.294h-3.128v-3.622h3.128v-2.671c0-3.1 1.893-4.788 4.659-4.788 1.325 0 2.463.099 2.795.143v3.24l-1.918.001c-1.504 0-1.795.715-1.795 1.763v2.313h3.587l-.467 3.622h-3.12v9.293h6.116c.73 0 1.323-.593 1.323-1.325v-21.35c0-.732-.593-1.325-1.325-1.325z" />
                  </svg>
                </a>
                <a href="#" class="text-gray-400 hover:text-[var(--primary-color)]">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="currentColor" viewBox="0 0 24 24">
                    <path d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z" />
                  </svg>
                </a>
              </div>
            </div>
          </div>
          
          <!-- Team Member 2 -->
          <div class="card overflow-hidden hover:shadow-lg">
            <img src="/images/team2.jpg" alt="Sarah Johnson" class="w-full h-64 object-cover">
            <div class="p-6">
              <h3 class="text-xl font-bold mb-1">Sarah Johnson</h3>
              <p class="text-[var(--primary-color)] mb-4">Vice President</p>
              <p class="text-gray-600 dark:text-gray-400 mb-4">Performance driving instructor and track day coordinator. Drives a modified Subaru WRX STI.</p>
              <div class="flex space-x-3">
                <a href="#" class="text-gray-400 hover:text-[var(--primary-color)]">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="currentColor" viewBox="0 0 24 24">
                    <path d="M22.675 0h-21.35c-.732 0-1.325.593-1.325 1.325v21.351c0 .731.593 1.324 1.325 1.324h11.495v-9.294h-3.128v-3.622h3.128v-2.671c0-3.1 1.893-4.788 4.659-4.788 1.325 0 2.463.099 2.795.143v3.24l-1.918.001c-1.504 0-1.795.715-1.795 1.763v2.313h3.587l-.467 3.622h-3.12v9.293h6.116c.73 0 1.323-.593 1.323-1.325v-21.35c0-.732-.593-1.325-1.325-1.325z" />
                  </svg>
                </a>
                <a href="#" class="text-gray-400 hover:text-[var(--primary-color)]">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="currentColor" viewBox="0 0 24 24">
                    <path d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z" />
                  </svg>
                </a>
              </div>
            </div>
          </div>
          
          <!-- Team Member 3 -->
          <div class="card overflow-hidden hover:shadow-lg">
            <img src="/images/team3.jpg" alt="David Rodriguez" class="w-full h-64 object-cover">
            <div class="p-6">
              <h3 class="text-xl font-bold mb-1">David Rodriguez</h3>
              <p class="text-[var(--primary-color)] mb-4">Events Coordinator</p>
              <p class="text-gray-600 dark:text-gray-400 mb-4">Car show specialist and community outreach leader. Owns a custom Nissan 370Z.</p>
              <div class="flex space-x-3">
                <a href="#" class="text-gray-400 hover:text-[var(--primary-color)]">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="currentColor" viewBox="0 0 24 24">
                    <path d="M22.675 0h-21.35c-.732 0-1.325.593-1.325 1.325v21.351c0 .731.593 1.324 1.325 1.324h11.495v-9.294h-3.128v-3.622h3.128v-2.671c0-3.1 1.893-4.788 4.659-4.788 1.325 0 2.463.099 2.795.143v3.24l-1.918.001c-1.504 0-1.795.715-1.795 1.763v2.313h3.587l-.467 3.622h-3.12v9.293h6.116c.73 0 1.323-.593 1.323-1.325v-21.35c0-.732-.593-1.325-1.325-1.325z" />
                  </svg>
                </a>
                <a href="#" class="text-gray-400 hover:text-[var(--primary-color)]">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="currentColor" viewBox="0 0 24 24">
                    <path d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z" />
                  </svg>
                </a>
              </div>
            </div>
          </div>
          
          <!-- Team Member 4 -->
          <div class="card overflow-hidden hover:shadow-lg">
            <img src="/images/team4.jpg" alt="Emily Chen" class="w-full h-64 object-cover">
            <div class="p-6">
              <h3 class="text-xl font-bold mb-1">Emily Chen</h3>
              <p class="text-[var(--primary-color)] mb-4">Treasurer</p>
              <p class="text-gray-600 dark:text-gray-400 mb-4">Financial advisor and membership coordinator. Drives a BMW M3 Competition.</p>
              <div class="flex space-x-3">
                <a href="#" class="text-gray-400 hover:text-[var(--primary-color)]">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="currentColor" viewBox="0 0 24 24">
                    <path d="M22.675 0h-21.35c-.732 0-1.325.593-1.325 1.325v21.351c0 .731.593 1.324 1.325 1.324h11.495v-9.294h-3.128v-3.622h3.128v-2.671c0-3.1 1.893-4.788 4.659-4.788 1.325 0 2.463.099 2.795.143v3.24l-1.918.001c-1.504 0-1.795.715-1.795 1.763v2.313h3.587l-.467 3.622h-3.12v9.293h6.116c.73 0 1.323-.593 1.323-1.325v-21.35c0-.732-.593-1.325-1.325-1.325z" />
                  </svg>
                </a>
                <a href="#" class="text-gray-400 hover:text-[var(--primary-color)]">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="currentColor" viewBox="0 0 24 24">
                    <path d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z" />
                  </svg>
                </a>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Testimonials -->
    <section class="section bg-gray-100 dark:bg-gray-800">
      <div class="container-custom">
        <h2 class="section-title text-center">Member Testimonials</h2>
        <div class="grid md:grid-cols-3 gap-8 mt-12">
          <div class="bg-white dark:bg-gray-900 p-8 rounded-lg shadow-md">
            <div class="flex items-center mb-4">
              <div class="text-[var(--primary-color)]">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8" fill="currentColor" viewBox="0 0 24 24">
                  <path d="M13 14.725c0-5.141 3.892-10.519 10-11.725l.984 2.126c-2.215.835-4.163 3.742-4.38 5.746 2.491.392 4.396 2.547 4.396 5.149 0 3.182-2.584 4.979-5.199 4.979-3.015 0-5.801-2.305-5.801-6.275zm-13 0c0-5.141 3.892-10.519 10-11.725l.984 2.126c-2.215.835-4.163 3.742-4.38 5.746 2.491.392 4.396 2.547 4.396 5.149 0 3.182-2.584 4.979-5.199 4.979-3.015 0-5.801-2.305-5.801-6.275z" />
                </svg>
              </div>
            </div>
            <p class="mb-4 text-gray-600 dark:text-gray-300 italic">Dallas Car Club has been like a second family to me. The knowledge and friendships I've gained are invaluable. From helping me restore my Camaro to teaching me performance driving, this club has enhanced my automotive journey tremendously.</p>
            <div class="flex items-center">
              <img src="/images/testimonial1.jpg" alt="Member" class="w-12 h-12 rounded-full mr-4">
              <div>
                <h4 class="font-bold">Robert Wilson</h4>
                <p class="text-sm text-gray-500 dark:text-gray-400">Member since 2018</p>
              </div>
            </div>
          </div>
          
          <div class="bg-white dark:bg-gray-900 p-8 rounded-lg shadow-md">
            <div class="flex items-center mb-4">
              <div class="text-[var(--primary-color)]">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8" fill="currentColor" viewBox="0 0 24 24">
                  <path d="M13 14.725c0-5.141 3.892-10.519 10-11.725l.984 2.126c-2.215.835-4.163 3.742-4.38 5.746 2.491.392 4.396 2.547 4.396 5.149 0 3.182-2.584 4.979-5.199 4.979-3.015 0-5.801-2.305-5.801-6.275zm-13 0c0-5.141 3.892-10.519 10-11.725l.984 2.126c-2.215.835-4.163 3.742-4.38 5.746 2.491.392 4.396 2.547 4.396 5.149 0 3.182-2.584 4.979-5.199 4.979-3.015 0-5.801-2.305-5.801-6.275z" />
                </svg>
              </div>
            </div>
            <p class="mb-4 text-gray-600 dark:text-gray-300 italic">As a woman in the car scene, I was initially hesitant to join a car club. Dallas Car Club has been incredibly welcoming and supportive. The inclusive environment and emphasis on education rather than competition makes this club stand out.</p>
            <div class="flex items-center">
              <img src="/images/testimonial2.jpg" alt="Member" class="w-12 h-12 rounded-full mr-4">
              <div>
                <h4 class="font-bold">Jessica Martinez</h4>
                <p class="text-sm text-gray-500 dark:text-gray-400">Member since 2021</p>
              </div>
            </div>
          </div>
          
          <div class="bg-white dark:bg-gray-900 p-8 rounded-lg shadow-md">
            <div class="flex items-center mb-4">
              <div class="text-[var(--primary-color)]">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8" fill="currentColor" viewBox="0 0 24 24">
                  <path d="M13 14.725c0-5.141 3.892-10.519 10-11.725l.984 2.126c-2.215.835-4.163 3.742-4.38 5.746 2.491.392 4.396 2.547 4.396 5.149 0 3.182-2.584 4.979-5.199 4.979-3.015 0-5.801-2.305-5.801-6.275zm-13 0c0-5.141 3.892-10.519 10-11.725l.984 2.126c-2.215.835-4.163 3.742-4.38 5.746 2.491.392 4.396 2.547 4.396 5.149 0 3.182-2.584 4.979-5.199 4.979-3.015 0-5.801-2.305-5.801-6.275z" />
                </svg>
              </div>
            </div>
            <p class="mb-4 text-gray-600 dark:text-gray-300 italic">The charity work that Dallas Car Club does is what initially attracted me. Using our shared passion for cars to give back to the community is incredibly rewarding. Plus, the technical knowledge I've gained has saved me thousands in maintenance costs.</p>
            <div class="flex items-center">
              <img src="/images/testimonial3.jpg" alt="Member" class="w-12 h-12 rounded-full mr-4">
              <div>
                <h4 class="font-bold">Thomas Lee</h4>
                <p class="text-sm text-gray-500 dark:text-gray-400">Member since 2017</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Join CTA -->
    <section class="section bg-white dark:bg-gray-900">
      <div class="container-custom">
        <div class="bg-[var(--secondary-color)] text-white rounded-lg p-8 md:p-12">
          <div class="md:flex items-center justify-between">
            <div class="md:w-2/3 mb-6 md:mb-0">
              <h2 class="text-2xl md:text-3xl font-bold mb-4">Ready to join our community?</h2>
              <p>Become a member today and connect with fellow car enthusiasts in the Dallas area.</p>
            </div>
            <div>
              <NuxtLink to="/membership" class="btn bg-white text-[var(--secondary-color)] hover:bg-gray-100">Join Now</NuxtLink>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script setup>
definePageMeta({
  title: 'About Us - Dallas Car Club',
  description: 'Learn about Dallas Car Club, our history, mission, and the team behind our community of car enthusiasts'
})
</script>
