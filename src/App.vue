<script setup>
import Header from './components/Header.vue'
import HeroSection from './components/HeroSection.vue'
import ServicesSection from './components/ServicesSection.vue'
import InstructorsSection from './components/InstructorsSection.vue'
import TestimonialsSection from './components/TestimonialsSection.vue'
import ContactSection from './components/ContactSection.vue'
import Footer from './components/Footer.vue'
</script>

<template>
  <div id="app">
    <Header />
    <main>
      <HeroSection />
      <ServicesSection />
      <InstructorsSection />
      <TestimonialsSection />
      <ContactSection />
    </main>
    <Footer />
  </div>
</template>
