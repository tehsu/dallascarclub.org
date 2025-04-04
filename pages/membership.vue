<template>
  <div>
    <!-- Hero Section -->
    <section class="relative bg-gray-900 text-white">
      <div class="absolute inset-0 bg-gradient-to-r from-black/70 to-black/50 z-10"></div>
      <div class="absolute inset-0 bg-[url('/images/membership-hero.jpg')] bg-cover bg-center"></div>
      <div class="container-custom relative z-20 py-16 md:py-24">
        <h1 class="text-4xl md:text-5xl font-bold mb-6">Membership</h1>
        <p class="text-xl max-w-2xl">Join our community of car enthusiasts and enjoy exclusive benefits.</p>
      </div>
    </section>

    <!-- Membership Benefits -->
    <section class="section bg-white dark:bg-gray-900">
      <div class="container-custom">
        <h2 class="section-title text-center">Membership Benefits</h2>
        <p class="text-center mb-12 max-w-3xl mx-auto">Becoming a member of Dallas Car Club gives you access to a variety of exclusive benefits</p>
        
        <div class="grid md:grid-cols-3 gap-8">
          <div class="card p-6 hover:shadow-lg">
            <div class="bg-[var(--primary-color)]/10 w-16 h-16 rounded-full flex items-center justify-center mb-4">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8 text-[var(--primary-color)]" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 20h5v-2a3 3 0 00-5.356-1.857M17 20H7m10 0v-2c0-.656-.126-1.283-.356-1.857M7 20H2v-2a3 3 0 015.356-1.857M7 20v-2c0-.656.126-1.283.356-1.857m0 0a5.002 5.002 0 019.288 0M15 7a3 3 0 11-6 0 3 3 0 016 0zm6 3a2 2 0 11-4 0 2 2 0 014 0zM7 10a2 2 0 11-4 0 2 2 0 014 0z" />
              </svg>
            </div>
            <h3 class="text-xl font-bold mb-2">Community Access</h3>
            <ul class="space-y-2 mb-4 text-gray-600 dark:text-gray-400">
              <li class="flex items-start">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-green-500 mr-2 mt-0.5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                </svg>
                Private online forum access
              </li>
              <li class="flex items-start">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-green-500 mr-2 mt-0.5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                </svg>
                Member-only social events
              </li>
              <li class="flex items-start">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-green-500 mr-2 mt-0.5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                </svg>
                Networking opportunities
              </li>
            </ul>
          </div>
          
          <div class="card p-6 hover:shadow-lg">
            <div class="bg-[var(--primary-color)]/10 w-16 h-16 rounded-full flex items-center justify-center mb-4">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8 text-[var(--primary-color)]" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8c-1.657 0-3 .895-3 2s1.343 2 3 2 3 .895 3 2-1.343 2-3 2m0-8c1.11 0 2.08.402 2.599 1M12 8V7m0 1v8m0 0v1m0-1c-1.11 0-2.08-.402-2.599-1M21 12a9 9 0 11-18 0 9 9 0 0118 0z" />
              </svg>
            </div>
            <h3 class="text-xl font-bold mb-2">Exclusive Discounts</h3>
            <ul class="space-y-2 mb-4 text-gray-600 dark:text-gray-400">
              <li class="flex items-start">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-green-500 mr-2 mt-0.5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                </svg>
                10-20% off at partner auto shops
              </li>
              <li class="flex items-start">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-green-500 mr-2 mt-0.5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                </svg>
                Special pricing on parts and accessories
              </li>
              <li class="flex items-start">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-green-500 mr-2 mt-0.5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                </svg>
                Reduced entry fees for car shows
              </li>
            </ul>
          </div>
          
          <div class="card p-6 hover:shadow-lg">
            <div class="bg-[var(--primary-color)]/10 w-16 h-16 rounded-full flex items-center justify-center mb-4">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8 text-[var(--primary-color)]" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 7V3m8 4V3m-9 8h10M5 21h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v12a2 2 0 002 2z" />
              </svg>
            </div>
            <h3 class="text-xl font-bold mb-2">Priority Event Access</h3>
            <ul class="space-y-2 mb-4 text-gray-600 dark:text-gray-400">
              <li class="flex items-start">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-green-500 mr-2 mt-0.5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                </svg>
                Early registration for track days
              </li>
              <li class="flex items-start">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-green-500 mr-2 mt-0.5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                </svg>
                VIP access to car shows
              </li>
              <li class="flex items-start">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-green-500 mr-2 mt-0.5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                </svg>
                Member-only driving events
              </li>
            </ul>
          </div>
        </div>
      </div>
    </section>

    <!-- Membership Plans -->
    <section class="section bg-gray-100 dark:bg-gray-800">
      <div class="container-custom">
        <h2 class="section-title text-center">Membership Plans</h2>
        <p class="text-center mb-12 max-w-3xl mx-auto">Choose the membership plan that suits you best</p>
        
        <div class="grid md:grid-cols-3 gap-8">
          <!-- Basic Plan -->
          <div class="card hover:shadow-lg relative overflow-hidden">
            <div class="p-8">
              <h3 class="text-2xl font-bold mb-4">Basic</h3>
              <div class="text-3xl font-bold mb-6">$50<span class="text-lg font-normal text-gray-500">/year</span></div>
              
              <ul class="space-y-3 mb-8">
                <li class="flex items-start">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-green-500 mr-2 mt-0.5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                  </svg>
                  Forum access
                </li>
                <li class="flex items-start">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-green-500 mr-2 mt-0.5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                  </svg>
                  Monthly meetups
                </li>
                <li class="flex items-start">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-green-500 mr-2 mt-0.5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                  </svg>
                  Basic discounts
                </li>
                <li class="flex items-start text-gray-400">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-gray-400 mr-2 mt-0.5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
                  </svg>
                  Track day access
                </li>
                <li class="flex items-start text-gray-400">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-gray-400 mr-2 mt-0.5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
                  </svg>
                  VIP events
                </li>
              </ul>
              
              <button class="btn btn-outline w-full">Join Now</button>
            </div>
          </div>
          
          <!-- Premium Plan -->
          <div class="card hover:shadow-lg relative overflow-hidden">
            <div class="absolute top-0 right-0 bg-[var(--primary-color)] text-white px-4 py-1 text-sm font-bold">
              POPULAR
            </div>
            <div class="p-8">
              <h3 class="text-2xl font-bold mb-4">Premium</h3>
              <div class="text-3xl font-bold mb-6">$100<span class="text-lg font-normal text-gray-500">/year</span></div>
              
              <ul class="space-y-3 mb-8">
                <li class="flex items-start">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-green-500 mr-2 mt-0.5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                  </svg>
                  All Basic benefits
                </li>
                <li class="flex items-start">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-green-500 mr-2 mt-0.5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                  </svg>
                  Track day access (2/year)
                </li>
                <li class="flex items-start">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-green-500 mr-2 mt-0.5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                  </svg>
                  Premium discounts
                </li>
                <li class="flex items-start">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-green-500 mr-2 mt-0.5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                  </svg>
                  Club merchandise
                </li>
                <li class="flex items-start text-gray-400">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-gray-400 mr-2 mt-0.5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
                  </svg>
                  Unlimited track days
                </li>
              </ul>
              
              <button class="btn btn-primary w-full">Join Now</button>
            </div>
          </div>
          
          <!-- Elite Plan -->
          <div class="card hover:shadow-lg relative overflow-hidden">
            <div class="p-8">
              <h3 class="text-2xl font-bold mb-4">Elite</h3>
              <div class="text-3xl font-bold mb-6">$200<span class="text-lg font-normal text-gray-500">/year</span></div>
              
              <ul class="space-y-3 mb-8">
                <li class="flex items-start">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-green-500 mr-2 mt-0.5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                  </svg>
                  All Premium benefits
                </li>
                <li class="flex items-start">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-green-500 mr-2 mt-0.5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                  </svg>
                  Unlimited track days
                </li>
                <li class="flex items-start">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-green-500 mr-2 mt-0.5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                  </svg>
                  VIP event access
                </li>
                <li class="flex items-start">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-green-500 mr-2 mt-0.5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                  </svg>
                  Driving instruction
                </li>
                <li class="flex items-start">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-green-500 mr-2 mt-0.5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                  </svg>
                  Exclusive elite events
                </li>
              </ul>
              
              <button class="btn btn-outline w-full">Join Now</button>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Join Form -->
    <section class="section bg-white dark:bg-gray-900">
      <div class="container-custom">
        <div class="max-w-3xl mx-auto">
          <h2 class="section-title text-center">Join Dallas Car Club</h2>
          <p class="text-center mb-8">Fill out the form below to start your membership application</p>
          
          <form @submit.prevent="submitMembershipForm" class="card p-8">
            <div class="grid md:grid-cols-2 gap-6 mb-6">
              <div>
                <label for="firstName" class="block mb-2 font-medium">First Name</label>
                <input type="text" id="firstName" v-model="form.firstName" required class="w-full px-4 py-2 border border-gray-300 dark:border-gray-700 rounded-md focus:outline-none focus:ring-2 focus:ring-[var(--primary-color)]">
              </div>
              <div>
                <label for="lastName" class="block mb-2 font-medium">Last Name</label>
                <input type="text" id="lastName" v-model="form.lastName" required class="w-full px-4 py-2 border border-gray-300 dark:border-gray-700 rounded-md focus:outline-none focus:ring-2 focus:ring-[var(--primary-color)]">
              </div>
            </div>
            
            <div class="mb-6">
              <label for="email" class="block mb-2 font-medium">Email</label>
              <input type="email" id="email" v-model="form.email" required class="w-full px-4 py-2 border border-gray-300 dark:border-gray-700 rounded-md focus:outline-none focus:ring-2 focus:ring-[var(--primary-color)]">
            </div>
            
            <div class="mb-6">
              <label for="phone" class="block mb-2 font-medium">Phone</label>
              <input type="tel" id="phone" v-model="form.phone" class="w-full px-4 py-2 border border-gray-300 dark:border-gray-700 rounded-md focus:outline-none focus:ring-2 focus:ring-[var(--primary-color)]">
            </div>
            
            <div class="mb-6">
              <label class="block mb-2 font-medium">Membership Type</label>
              <div class="grid md:grid-cols-3 gap-4">
                <div class="flex items-center">
                  <input type="radio" id="basic" v-model="form.membershipType" value="basic" class="mr-2">
                  <label for="basic">Basic ($50/year)</label>
                </div>
                <div class="flex items-center">
                  <input type="radio" id="premium" v-model="form.membershipType" value="premium" class="mr-2">
                  <label for="premium">Premium ($100/year)</label>
                </div>
                <div class="flex items-center">
                  <input type="radio" id="elite" v-model="form.membershipType" value="elite" class="mr-2">
                  <label for="elite">Elite ($200/year)</label>
                </div>
              </div>
            </div>
            
            <div class="mb-6">
              <label for="carInfo" class="block mb-2 font-medium">Tell us about your car(s)</label>
              <textarea id="carInfo" v-model="form.carInfo" rows="4" class="w-full px-4 py-2 border border-gray-300 dark:border-gray-700 rounded-md focus:outline-none focus:ring-2 focus:ring-[var(--primary-color)]"></textarea>
            </div>
            
            <div class="mb-6">
              <div class="flex items-start">
                <input type="checkbox" id="terms" v-model="form.termsAccepted" required class="mt-1 mr-2">
                <label for="terms">I agree to the <a href="#" class="text-[var(--primary-color)] hover:underline">terms and conditions</a> and understand that my membership is subject to approval.</label>
              </div>
            </div>
            
            <div>
              <button type="submit" class="btn btn-primary w-full">Submit Application</button>
            </div>
          </form>
        </div>
      </div>
    </section>
  </div>
</template>

<script setup>
import { ref } from 'vue'

definePageMeta({
  title: 'Membership - Dallas Car Club',
  description: 'Join Dallas Car Club and become part of our community of car enthusiasts'
})

// Form state
const form = ref({
  firstName: '',
  lastName: '',
  email: '',
  phone: '',
  membershipType: 'premium',
  carInfo: '',
  termsAccepted: false
})

// Form submission
const submitMembershipForm = () => {
  // Here you would typically send the form data to your backend
  alert('Thank you for your application! We will contact you shortly.')
  // Reset form
  form.value = {
    firstName: '',
    lastName: '',
    email: '',
    phone: '',
    membershipType: 'premium',
    carInfo: '',
    termsAccepted: false
  }
}
</script>
