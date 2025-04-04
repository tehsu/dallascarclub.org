<template>
  <div>
    <!-- Hero Section -->
    <section class="relative bg-gray-900 text-white">
      <div class="absolute inset-0 bg-gradient-to-r from-black/70 to-black/50 z-10"></div>
      <div class="absolute inset-0 bg-[url('/images/contact-hero.jpg')] bg-cover bg-center"></div>
      <div class="container-custom relative z-20 py-16 md:py-24">
        <h1 class="text-4xl md:text-5xl font-bold mb-6">Contact Us</h1>
        <p class="text-xl max-w-2xl">Get in touch with the Dallas Car Club team. We'd love to hear from you!</p>
      </div>
    </section>

    <!-- Contact Information -->
    <section class="section bg-white dark:bg-gray-900">
      <div class="container-custom">
        <div class="grid md:grid-cols-2 gap-12">
          <!-- Contact Form -->
          <div>
            <h2 class="section-title">Send Us a Message</h2>
            <p class="mb-6">Have a question or want to get involved? Fill out the form below and we'll get back to you as soon as possible.</p>
            
            <form @submit.prevent="submitContactForm" class="space-y-6">
              <div>
                <label for="name" class="block mb-2 font-medium">Your Name</label>
                <input 
                  type="text" 
                  id="name" 
                  v-model="form.name" 
                  required 
                  class="w-full px-4 py-2 border border-gray-300 dark:border-gray-700 rounded-md focus:outline-none focus:ring-2 focus:ring-[var(--primary-color)]"
                >
              </div>
              
              <div>
                <label for="email" class="block mb-2 font-medium">Email Address</label>
                <input 
                  type="email" 
                  id="email" 
                  v-model="form.email" 
                  required 
                  class="w-full px-4 py-2 border border-gray-300 dark:border-gray-700 rounded-md focus:outline-none focus:ring-2 focus:ring-[var(--primary-color)]"
                >
              </div>
              
              <div>
                <label for="subject" class="block mb-2 font-medium">Subject</label>
                <select 
                  id="subject" 
                  v-model="form.subject" 
                  required 
                  class="w-full px-4 py-2 border border-gray-300 dark:border-gray-700 rounded-md focus:outline-none focus:ring-2 focus:ring-[var(--primary-color)]"
                >
                  <option value="">Select a subject</option>
                  <option value="General Inquiry">General Inquiry</option>
                  <option value="Membership">Membership</option>
                  <option value="Events">Events</option>
                  <option value="Sponsorship">Sponsorship</option>
                  <option value="Other">Other</option>
                </select>
              </div>
              
              <div>
                <label for="message" class="block mb-2 font-medium">Message</label>
                <textarea 
                  id="message" 
                  v-model="form.message" 
                  rows="6" 
                  required 
                  class="w-full px-4 py-2 border border-gray-300 dark:border-gray-700 rounded-md focus:outline-none focus:ring-2 focus:ring-[var(--primary-color)]"
                ></textarea>
              </div>
              
              <button type="submit" class="btn btn-primary">Send Message</button>
            </form>
          </div>
          
          <!-- Contact Information -->
          <div>
            <h2 class="section-title">Contact Information</h2>
            <p class="mb-8">You can reach us through the following channels or visit us at our monthly meetups.</p>
            
            <div class="space-y-6">
              <div class="flex items-start space-x-4">
                <div class="bg-[var(--primary-color)]/10 p-3 rounded-full">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-[var(--primary-color)]" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z" />
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 11a3 3 0 11-6 0 3 3 0 016 0z" />
                  </svg>
                </div>
                <div>
                  <h3 class="text-xl font-bold mb-2">Address</h3>
                  <p class="text-gray-600 dark:text-gray-400">123 Main Street<br>Dallas, TX 75201</p>
                  <p class="text-gray-600 dark:text-gray-400 mt-2">
                    <span class="font-medium">Monthly Meetup Location:</span><br>
                    White Rock Lake, Parking Lot E<br>
                    Dallas, TX
                  </p>
                </div>
              </div>
              
              <div class="flex items-start space-x-4">
                <div class="bg-[var(--primary-color)]/10 p-3 rounded-full">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-[var(--primary-color)]" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z" />
                  </svg>
                </div>
                <div>
                  <h3 class="text-xl font-bold mb-2">Email</h3>
                  <p class="text-gray-600 dark:text-gray-400">info@dallascarclub.org</p>
                  <p class="text-gray-600 dark:text-gray-400 mt-2">
                    <span class="font-medium">Membership Inquiries:</span><br>
                    membership@dallascarclub.org
                  </p>
                  <p class="text-gray-600 dark:text-gray-400 mt-2">
                    <span class="font-medium">Events:</span><br>
                    events@dallascarclub.org
                  </p>
                </div>
              </div>
              
              <div class="flex items-start space-x-4">
                <div class="bg-[var(--primary-color)]/10 p-3 rounded-full">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-[var(--primary-color)]" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z" />
                  </svg>
                </div>
                <div>
                  <h3 class="text-xl font-bold mb-2">Phone</h3>
                  <p class="text-gray-600 dark:text-gray-400">(214) 555-1234</p>
                  <p class="text-gray-600 dark:text-gray-400 mt-2">
                    <span class="font-medium">Office Hours:</span><br>
                    Monday - Friday: 9:00 AM - 5:00 PM
                  </p>
                </div>
              </div>
              
              <div class="flex items-start space-x-4">
                <div class="bg-[var(--primary-color)]/10 p-3 rounded-full">
                  <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-[var(--primary-color)]" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z" />
                  </svg>
                </div>
                <div>
                  <h3 class="text-xl font-bold mb-2">Social Media</h3>
                  <div class="flex space-x-4 mt-2">
                    <a href="#" class="text-gray-600 dark:text-gray-400 hover:text-[var(--primary-color)]">
                      <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="currentColor" viewBox="0 0 24 24">
                        <path d="M22.675 0h-21.35c-.732 0-1.325.593-1.325 1.325v21.351c0 .731.593 1.324 1.325 1.324h11.495v-9.294h-3.128v-3.622h3.128v-2.671c0-3.1 1.893-4.788 4.659-4.788 1.325 0 2.463.099 2.795.143v3.24l-1.918.001c-1.504 0-1.795.715-1.795 1.763v2.313h3.587l-.467 3.622h-3.12v9.293h6.116c.73 0 1.323-.593 1.323-1.325v-21.35c0-.732-.593-1.325-1.325-1.325z" />
                      </svg>
                    </a>
                    <a href="#" class="text-gray-600 dark:text-gray-400 hover:text-[var(--primary-color)]">
                      <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="currentColor" viewBox="0 0 24 24">
                        <path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zm0-2.163c-3.259 0-3.667.014-4.947.072-4.358.2-6.78 2.618-6.98 6.98-.059 1.281-.073 1.689-.073 4.948 0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98 1.281.058 1.689.072 4.948.072 3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98-1.281-.059-1.69-.073-4.949-.073zm0 5.838c-3.403 0-6.162 2.759-6.162 6.162s2.759 6.163 6.162 6.163 6.162-2.759 6.162-6.163c0-3.403-2.759-6.162-6.162-6.162zm0 10.162c-2.209 0-4-1.79-4-4 0-2.209 1.791-4 4-4s4 1.791 4 4c0 2.21-1.791 4-4 4zm6.406-11.845c-.796 0-1.441.645-1.441 1.44s.645 1.44 1.441 1.44c.795 0 1.439-.645 1.439-1.44s-.644-1.44-1.439-1.44z" />
                      </svg>
                    </a>
                    <a href="#" class="text-gray-600 dark:text-gray-400 hover:text-[var(--primary-color)]">
                      <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="currentColor" viewBox="0 0 24 24">
                        <path d="M24 4.557c-.883.392-1.832.656-2.828.775 1.017-.609 1.798-1.574 2.165-2.724-.951.564-2.005.974-3.127 1.195-.897-.957-2.178-1.555-3.594-1.555-3.179 0-5.515 2.966-4.797 6.045-4.091-.205-7.719-2.165-10.148-5.144-1.29 2.213-.669 5.108 1.523 6.574-.806-.026-1.566-.247-2.229-.616-.054 2.281 1.581 4.415 3.949 4.89-.693.188-1.452.232-2.224.084.626 1.956 2.444 3.379 4.6 3.419-2.07 1.623-4.678 2.348-7.29 2.04 2.179 1.397 4.768 2.212 7.548 2.212 9.142 0 14.307-7.721 13.995-14.646.962-.695 1.797-1.562 2.457-2.549z" />
                      </svg>
                    </a>
                    <a href="#" class="text-gray-600 dark:text-gray-400 hover:text-[var(--primary-color)]">
                      <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="currentColor" viewBox="0 0 24 24">
                        <path d="M19.615 3.184c-3.604-.246-11.631-.245-15.23 0-3.897.266-4.356 2.62-4.385 8.816.029 6.185.484 8.549 4.385 8.816 3.6.245 11.626.246 15.23 0 3.897-.266 4.356-2.62 4.385-8.816-.029-6.185-.484-8.549-4.385-8.816zm-10.615 12.816v-8l8 3.993-8 4.007z" />
                      </svg>
                    </a>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Map Section -->
    <section class="section bg-gray-100 dark:bg-gray-800">
      <div class="container-custom">
        <h2 class="section-title text-center">Find Us</h2>
        <p class="text-center mb-12 max-w-3xl mx-auto">Our office is located in downtown Dallas, and we host monthly meetups at White Rock Lake.</p>
        
        <!-- Map placeholder - in a real implementation, this would be an embedded Google Map -->
        <div class="bg-white dark:bg-gray-900 rounded-lg shadow-md p-6">
          <div class="text-center p-12 border-2 border-dashed border-gray-300 dark:border-gray-700 rounded-lg">
            <h3 class="text-xl font-bold mb-4">Interactive Map Coming Soon</h3>
            <p class="text-gray-600 dark:text-gray-400">Our interactive map is under development. In the meantime, you can find us at 123 Main Street, Dallas, TX 75201.</p>
          </div>
        </div>
      </div>
    </section>

    <!-- FAQ Section -->
    <section class="section bg-white dark:bg-gray-900">
      <div class="container-custom">
        <h2 class="section-title text-center">Frequently Asked Questions</h2>
        <p class="text-center mb-12 max-w-3xl mx-auto">Find answers to common questions about Dallas Car Club</p>
        
        <div class="max-w-3xl mx-auto">
          <div class="space-y-6">
            <div class="card p-6">
              <button 
                @click="toggleFaq(0)" 
                class="flex justify-between items-center w-full text-left"
              >
                <h3 class="text-lg font-bold">How do I become a member?</h3>
                <svg 
                  xmlns="http://www.w3.org/2000/svg" 
                  class="h-5 w-5 transition-transform" 
                  :class="{ 'rotate-180': openFaqs[0] }"
                  fill="none" 
                  viewBox="0 0 24 24" 
                  stroke="currentColor"
                >
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7" />
                </svg>
              </button>
              <div v-if="openFaqs[0]" class="mt-4 text-gray-600 dark:text-gray-400">
                <p>To become a member, visit our Membership page and fill out the application form. Once submitted, our membership team will review your application and contact you within 3-5 business days.</p>
              </div>
            </div>
            
            <div class="card p-6">
              <button 
                @click="toggleFaq(1)" 
                class="flex justify-between items-center w-full text-left"
              >
                <h3 class="text-lg font-bold">When and where are the monthly meetups?</h3>
                <svg 
                  xmlns="http://www.w3.org/2000/svg" 
                  class="h-5 w-5 transition-transform" 
                  :class="{ 'rotate-180': openFaqs[1] }"
                  fill="none" 
                  viewBox="0 0 24 24" 
                  stroke="currentColor"
                >
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7" />
                </svg>
              </button>
              <div v-if="openFaqs[1]" class="mt-4 text-gray-600 dark:text-gray-400">
                <p>Our monthly meetups are held on the first Saturday of each month at White Rock Lake, Parking Lot E, from 9:00 AM to 12:00 PM. Check our Events page for any schedule changes or special events.</p>
              </div>
            </div>
            
            <div class="card p-6">
              <button 
                @click="toggleFaq(2)" 
                class="flex justify-between items-center w-full text-left"
              >
                <h3 class="text-lg font-bold">Do I need to own a specific type of car to join?</h3>
                <svg 
                  xmlns="http://www.w3.org/2000/svg" 
                  class="h-5 w-5 transition-transform" 
                  :class="{ 'rotate-180': openFaqs[2] }"
                  fill="none" 
                  viewBox="0 0 24 24" 
                  stroke="currentColor"
                >
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7" />
                </svg>
              </button>
              <div v-if="openFaqs[2]" class="mt-4 text-gray-600 dark:text-gray-400">
                <p>No, we welcome all automotive enthusiasts regardless of what you drive. Our club includes members with classic cars, modern sports cars, imports, domestics, trucks, and even project cars. What matters is your passion for cars!</p>
              </div>
            </div>
            
            <div class="card p-6">
              <button 
                @click="toggleFaq(3)" 
                class="flex justify-between items-center w-full text-left"
              >
                <h3 class="text-lg font-bold">How can I sponsor a Dallas Car Club event?</h3>
                <svg 
                  xmlns="http://www.w3.org/2000/svg" 
                  class="h-5 w-5 transition-transform" 
                  :class="{ 'rotate-180': openFaqs[3] }"
                  fill="none" 
                  viewBox="0 0 24 24" 
                  stroke="currentColor"
                >
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7" />
                </svg>
              </button>
              <div v-if="openFaqs[3]" class="mt-4 text-gray-600 dark:text-gray-400">
                <p>We offer various sponsorship opportunities for businesses looking to connect with our community. Please contact us at sponsorship@dallascarclub.org for more information about our sponsorship packages and benefits.</p>
              </div>
            </div>
            
            <div class="card p-6">
              <button 
                @click="toggleFaq(4)" 
                class="flex justify-between items-center w-full text-left"
              >
                <h3 class="text-lg font-bold">Can I participate in track days if I'm a new driver?</h3>
                <svg 
                  xmlns="http://www.w3.org/2000/svg" 
                  class="h-5 w-5 transition-transform" 
                  :class="{ 'rotate-180': openFaqs[4] }"
                  fill="none" 
                  viewBox="0 0 24 24" 
                  stroke="currentColor"
                >
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7" />
                </svg>
              </button>
              <div v-if="openFaqs[4]" class="mt-4 text-gray-600 dark:text-gray-400">
                <p>Absolutely! Our track days include sessions for drivers of all experience levels. Novice drivers are paired with experienced instructors who provide guidance and ensure safety. We also offer classroom sessions to help you learn the fundamentals of performance driving.</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script setup>
import { ref } from 'vue'

definePageMeta({
  title: 'Contact Us - Dallas Car Club',
  description: 'Get in touch with Dallas Car Club. Contact information, location, and frequently asked questions.'
})

// Contact form state
const form = ref({
  name: '',
  email: '',
  subject: '',
  message: ''
})

// Form submission
const submitContactForm = () => {
  // Here you would typically send the form data to your backend
  alert('Thank you for your message! We will get back to you shortly.')
  // Reset form
  form.value = {
    name: '',
    email: '',
    subject: '',
    message: ''
  }
}

// FAQ accordion
const openFaqs = ref([false, false, false, false, false])

const toggleFaq = (index) => {
  openFaqs.value[index] = !openFaqs.value[index]
}
</script>
