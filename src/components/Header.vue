<template>
  <header class="fixed top-0 left-0 right-0 z-50 transition-all duration-300" 
          :class="isScrolled ? 'bg-white/50 backdrop-blur-md shadow-xl border-b border-gray-200/50' : 'bg-transparent'">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex justify-between items-center py-4">
        <!-- Logo -->
        <div class="flex items-center group">
          <div class="flex-shrink-0 relative">
            <div class="absolute inset-0 bg-gradient-to-r from-blue-600 to-blue-800 rounded-xl blur opacity-20 group-hover:opacity-30 transition-opacity duration-300"></div>
            <div class="relative bg-gradient-to-r from-blue-600 to-blue-800 text-white px-4 py-2 rounded-xl shadow-lg">
              <h1 class="text-2xl font-bold tracking-tight">Kevser Rijschool</h1>
              <!-- <p class="text-xs text-blue-100 font-medium">Rijschool</p> -->
            </div>
          </div>
        </div>

        <!-- Desktop Navigation -->
        <nav class="hidden md:flex items-center space-x-1">
          <a href="#home"
            class="relative px-4 py-2 text-sm font-medium transition-all duration-300 rounded-lg group"
            :class="isScrolled ? 'text-gray-700 hover:text-blue-600' : 'text-white hover:text-blue-200'">
            <span class="relative z-10">Home</span>
            <div class="absolute inset-0 bg-white/10 rounded-lg opacity-0 group-hover:opacity-100 transition-opacity duration-300"></div>
          </a>
          <a href="#services"
            class="relative px-4 py-2 text-sm font-medium transition-all duration-300 rounded-lg group"
            :class="isScrolled ? 'text-gray-700 hover:text-blue-600' : 'text-white hover:text-blue-200'">
            <span class="relative z-10">Diensten</span>
            <div class="absolute inset-0 bg-white/10 rounded-lg opacity-0 group-hover:opacity-100 transition-opacity duration-300"></div>
          </a>
          <a href="#pricing"
            class="relative px-4 py-2 text-sm font-medium transition-all duration-300 rounded-lg group"
            :class="isScrolled ? 'text-gray-700 hover:text-blue-600' : 'text-white hover:text-blue-200'">
            <span class="relative z-10">Prijzen</span>
            <div class="absolute inset-0 bg-white/10 rounded-lg opacity-0 group-hover:opacity-100 transition-opacity duration-300"></div>
          </a>
          <a href="#instructors"
            class="relative px-4 py-2 text-sm font-medium transition-all duration-300 rounded-lg group"
            :class="isScrolled ? 'text-gray-700 hover:text-blue-600' : 'text-white hover:text-blue-200'">
            <span class="relative z-10">Instructeurs</span>
            <div class="absolute inset-0 bg-white/10 rounded-lg opacity-0 group-hover:opacity-100 transition-opacity duration-300"></div>
          </a>
          <a href="#testimonials"
            class="relative px-4 py-2 text-sm font-medium transition-all duration-300 rounded-lg group"
            :class="isScrolled ? 'text-gray-700 hover:text-blue-600' : 'text-white hover:text-blue-200'">
            <span class="relative z-10">Referenties</span>
            <div class="absolute inset-0 bg-white/10 rounded-lg opacity-0 group-hover:opacity-100 transition-opacity duration-300"></div>
          </a>
          <a href="#contact"
            class="relative px-4 py-2 text-sm font-medium transition-all duration-300 rounded-lg group"
            :class="isScrolled ? 'text-gray-700 hover:text-blue-600' : 'text-white hover:text-blue-200'">
            <span class="relative z-10">Contact</span>
            <div class="absolute inset-0 bg-white/10 rounded-lg opacity-0 group-hover:opacity-100 transition-opacity duration-300"></div>
          </a>
        </nav>

        <!-- Contact Info & CTA -->
        <div class="hidden lg:flex items-center space-x-4">
          <div class="text-right">
            <p class="text-xs font-medium" :class="isScrolled ? 'text-gray-500' : 'text-white/80'">Bel direct</p>
            <a href="tel:+31612345678"
              class="text-lg font-bold transition-all duration-300 hover:scale-105"
              :class="isScrolled ? 'text-blue-600 hover:text-blue-700' : 'text-white hover:text-blue-200'">
              +31 6 1234 5678
            </a>
          </div>
          <button
            class="relative bg-gradient-to-r from-orange-500 to-orange-600 text-white px-6 py-3 rounded-xl font-bold text-sm shadow-lg hover:shadow-xl transition-all duration-300 hover:scale-105 group overflow-hidden">
            <span class="relative z-10">Gratis Advies</span>
            <div class="absolute inset-0 bg-gradient-to-r from-orange-600 to-orange-700 opacity-0 group-hover:opacity-100 transition-opacity duration-300"></div>
          </button>
        </div>

        <!-- Mobile menu button -->
        <div class="md:hidden">
          <button @click="toggleMobileMenu"
            class="relative p-2 rounded-lg transition-all duration-300 hover:bg-white/10 focus:outline-none"
            :class="isScrolled ? 'text-gray-700 hover:text-blue-600' : 'text-white hover:text-blue-200'">
            <div class="w-6 h-6 flex flex-col justify-center items-center">
              <span class="block w-5 h-0.5 bg-current transition-all duration-300"
                    :class="mobileMenuOpen ? 'rotate-45 translate-y-1' : '-translate-y-1'"></span>
              <span class="block w-5 h-0.5 bg-current transition-all duration-300"
                    :class="mobileMenuOpen ? 'opacity-0' : 'opacity-100'"></span>
              <span class="block w-5 h-0.5 bg-current transition-all duration-300"
                    :class="mobileMenuOpen ? '-rotate-45 -translate-y-1' : 'translate-y-1'"></span>
            </div>
          </button>
        </div>
      </div>

      <!-- Mobile Navigation with Headless UI Transition -->
      <Transition enter-active-class="transition duration-300 ease-out" enter-from-class="opacity-0 -translate-y-4"
        enter-to-class="opacity-100 translate-y-0" leave-active-class="transition duration-200 ease-in"
        leave-from-class="opacity-100 translate-y-0" leave-to-class="opacity-0 -translate-y-4">
        <div v-if="mobileMenuOpen" class="md:hidden mt-4 p-6 rounded-2xl backdrop-blur-md border border-white/20"
             :class="isScrolled ? 'bg-white/90' : 'bg-white/10'">
          <div class="flex flex-col space-y-3">
            <TransitionGroup enter-active-class="transition duration-300 ease-out"
              enter-from-class="opacity-0 translate-x-4" enter-to-class="opacity-100 translate-x-0"
              leave-active-class="transition duration-200 ease-in" leave-from-class="opacity-100 translate-x-0"
              leave-to-class="opacity-0 -translate-x-4" tag="div" class="space-y-3">
              <a key="home" href="#home"
                class="block px-4 py-3 text-sm font-medium transition-all duration-300 rounded-xl group"
                :class="isScrolled ? 'text-gray-700 hover:text-blue-600 hover:bg-blue-50' : 'text-white hover:text-blue-200 hover:bg-white/10'"
                @click="closeMobileMenu">
                <span class="flex items-center">
                  <svg class="w-4 h-4 mr-3" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 12l2-2m0 0l7-7 7 7M5 10v10a1 1 0 001 1h3m10-11l2 2m-2-2v10a1 1 0 01-1 1h-3m-6 0a1 1 0 001-1v-4a1 1 0 011-1h2a1 1 0 011 1v4a1 1 0 001 1m-6 0h6" />
                  </svg>
                  Home
                </span>
              </a>
              <a key="services" href="#services"
                class="block px-4 py-3 text-sm font-medium transition-all duration-300 rounded-xl group"
                :class="isScrolled ? 'text-gray-700 hover:text-blue-600 hover:bg-blue-50' : 'text-white hover:text-blue-200 hover:bg-white/10'"
                @click="closeMobileMenu">
                <span class="flex items-center">
                  <svg class="w-4 h-4 mr-3" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 21V5a2 2 0 00-2-2H7a2 2 0 00-2 2v16m14 0h2m-2 0h-5m-9 0H3m2 0h5M9 7h1m-1 4h1m4-4h1m-1 4h1m-5 10v-5a1 1 0 011-1h2a1 1 0 011 1v5m-4 0h4" />
                  </svg>
                  Diensten
                </span>
              </a>
              <a key="pricing" href="#pricing"
                class="block px-4 py-3 text-sm font-medium transition-all duration-300 rounded-xl group"
                :class="isScrolled ? 'text-gray-700 hover:text-blue-600 hover:bg-blue-50' : 'text-white hover:text-blue-200 hover:bg-white/10'"
                @click="closeMobileMenu">
                <span class="flex items-center">
                  <svg class="w-4 h-4 mr-3" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8c-1.657 0-3 .895-3 2s1.343 2 3 2 3 .895 3 2-1.343 2-3 2m0-8c1.11 0 2.08.402 2.599 1M12 8V7m0 1v8m0 0v1m0-1c-1.11 0-2.08-.402-2.599-1" />
                  </svg>
                  Prijzen
                </span>
              </a>
              <a key="instructors" href="#instructors"
                class="block px-4 py-3 text-sm font-medium transition-all duration-300 rounded-xl group"
                :class="isScrolled ? 'text-gray-700 hover:text-blue-600 hover:bg-blue-50' : 'text-white hover:text-blue-200 hover:bg-white/10'"
                @click="closeMobileMenu">
                <span class="flex items-center">
                  <svg class="w-4 h-4 mr-3" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 4.354a4 4 0 110 5.292M15 21H3v-1a6 6 0 0112 0v1zm0 0h6v-1a6 6 0 00-9-5.197m13.5-9a2.5 2.5 0 11-5 0 2.5 2.5 0 015 0z" />
                  </svg>
                  Instructeurs
                </span>
              </a>
              <a key="testimonials" href="#testimonials"
                class="block px-4 py-3 text-sm font-medium transition-all duration-300 rounded-xl group"
                :class="isScrolled ? 'text-gray-700 hover:text-blue-600 hover:bg-blue-50' : 'text-white hover:text-blue-200 hover:bg-white/10'"
                @click="closeMobileMenu">
                <span class="flex items-center">
                  <svg class="w-4 h-4 mr-3" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 12h.01M12 12h.01M16 12h.01M21 12c0 4.418-4.03 8-9 8a9.863 9.863 0 01-4.255-.949L3 20l1.395-3.72C3.512 15.042 3 13.574 3 12c0-4.418 4.03-8 9-8s9 3.582 9 8z" />
                  </svg>
                  Referenties
                </span>
              </a>
              <a key="contact" href="#contact"
                class="block px-4 py-3 text-sm font-medium transition-all duration-300 rounded-xl group"
                :class="isScrolled ? 'text-gray-700 hover:text-blue-600 hover:bg-blue-50' : 'text-white hover:text-blue-200 hover:bg-white/10'"
                @click="closeMobileMenu">
                <span class="flex items-center">
                  <svg class="w-4 h-4 mr-3" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 4.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z" />
                  </svg>
                  Contact
                </span>
              </a>
            </TransitionGroup>

            <div class="pt-4 border-t border-white/20">
              <Transition enter-active-class="transition duration-500 ease-out delay-200"
                enter-from-class="opacity-0 translate-y-4" enter-to-class="opacity-100 translate-y-0"
                leave-active-class="transition duration-200 ease-in" leave-from-class="opacity-100 translate-y-0"
                leave-to-class="opacity-0 translate-y-4">
                <div v-if="mobileMenuOpen" class="space-y-4">
                  <div class="text-center">
                    <p class="text-sm font-medium mb-2" :class="isScrolled ? 'text-gray-500' : 'text-white/80'">Bel direct</p>
                    <a href="tel:+31612345678"
                      class="text-lg font-bold transition-all duration-300 hover:scale-105"
                      :class="isScrolled ? 'text-blue-600 hover:text-blue-700' : 'text-white hover:text-blue-200'">
                      +31 6 1234 5678
                    </a>
                  </div>
                  <button
                    class="w-full bg-gradient-to-r from-orange-500 to-orange-600 text-white px-6 py-3 rounded-xl font-bold text-sm shadow-lg hover:shadow-xl transition-all duration-300 hover:scale-105">
                    Gratis Advies
                  </button>
                </div>
              </Transition>
            </div>
          </div>
        </div>
      </Transition>
    </div>
  </header>
</template>

<script setup>
import { ref, Transition, TransitionGroup, onMounted, onUnmounted } from 'vue'

const mobileMenuOpen = ref(false)
const isScrolled = ref(false)

const toggleMobileMenu = () => {
  mobileMenuOpen.value = !mobileMenuOpen.value
}

const closeMobileMenu = () => {
  mobileMenuOpen.value = false
}

const handleScroll = () => {
  isScrolled.value = window.scrollY > 100
}

onMounted(() => {
  window.addEventListener('scroll', handleScroll)
  handleScroll() // Initial check
})

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll)
})
</script>
