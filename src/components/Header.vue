<template>
  <header class="bg-white shadow-lg sticky top-0 z-50">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex justify-between items-center py-4">
        <!-- Logo -->
        <div class="flex items-center">
          <div class="flex-shrink-0">
            <h1 class="text-2xl font-bold text-blue-600">Kevser Abla</h1>
            <p class="text-sm text-gray-600">Sürücü Kursu</p>
          </div>
        </div>

        <!-- Desktop Navigation -->
        <nav class="hidden md:flex space-x-8">
          <a href="#home" class="text-gray-700 hover:text-blue-600 px-3 py-2 text-sm font-medium transition-colors">
            Ana Sayfa
          </a>
          <a href="#services" class="text-gray-700 hover:text-blue-600 px-3 py-2 text-sm font-medium transition-colors">
            Hizmetlerimiz
          </a>
          <a href="#instructors" class="text-gray-700 hover:text-blue-600 px-3 py-2 text-sm font-medium transition-colors">
            Eğitmenlerimiz
          </a>
          <a href="#testimonials" class="text-gray-700 hover:text-blue-600 px-3 py-2 text-sm font-medium transition-colors">
            Referanslar
          </a>
          <a href="#contact" class="text-gray-700 hover:text-blue-600 px-3 py-2 text-sm font-medium transition-colors">
            İletişim
          </a>
        </nav>

        <!-- Contact Info & CTA -->
        <div class="hidden lg:flex items-center space-x-4">
          <div class="text-right">
            <p class="text-sm text-gray-600">Hemen Arayın</p>
            <a href="tel:+31612345678" class="text-lg font-semibold text-blue-600 hover:text-blue-700">
              +31 6 1234 5678
            </a>
          </div>
          <button class="bg-blue-600 text-white px-6 py-2 rounded-lg hover:bg-blue-700 transition-colors font-medium">
            Ücretsiz Danışmanlık
          </button>
        </div>

        <!-- Mobile menu button -->
        <div class="md:hidden">
          <button @click="toggleMobileMenu" class="text-gray-700 hover:text-blue-600 focus:outline-none">
            <svg class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path v-if="!mobileMenuOpen" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
              <path v-else stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
            </svg>
          </button>
        </div>
      </div>

      <!-- Mobile Navigation -->
      <div v-if="mobileMenuOpen" class="md:hidden border-t border-gray-200 py-4">
        <div class="flex flex-col space-y-2">
          <a href="#home" class="text-gray-700 hover:text-blue-600 px-3 py-2 text-sm font-medium" @click="closeMobileMenu">
            Ana Sayfa
          </a>
          <a href="#services" class="text-gray-700 hover:text-blue-600 px-3 py-2 text-sm font-medium" @click="closeMobileMenu">
            Hizmetlerimiz
          </a>
          <a href="#instructors" class="text-gray-700 hover:text-blue-600 px-3 py-2 text-sm font-medium" @click="closeMobileMenu">
            Eğitmenlerimiz
          </a>
          <a href="#testimonials" class="text-gray-700 hover:text-blue-600 px-3 py-2 text-sm font-medium" @click="closeMobileMenu">
            Referanslar
          </a>
          <a href="#contact" class="text-gray-700 hover:text-blue-600 px-3 py-2 text-sm font-medium" @click="closeMobileMenu">
            İletişim
          </a>
          <div class="pt-4 border-t border-gray-200">
            <p class="text-sm text-gray-600 mb-2">Hemen Arayın</p>
            <a href="tel:+31612345678" class="text-lg font-semibold text-blue-600 hover:text-blue-700">
              +31 6 1234 5678
            </a>
            <button class="w-full mt-4 bg-blue-600 text-white px-6 py-2 rounded-lg hover:bg-blue-700 transition-colors font-medium">
              Ücretsiz Danışmanlık
            </button>
          </div>
        </div>
      </div>
    </div>
  </header>
</template>

<script setup>
import { ref } from 'vue'

const mobileMenuOpen = ref(false)

const toggleMobileMenu = () => {
  mobileMenuOpen.value = !mobileMenuOpen.value
}

const closeMobileMenu = () => {
  mobileMenuOpen.value = false
}
</script>
