<template>
  <section id="home" class="relative bg-gradient-to-br from-blue-600 via-blue-700 to-blue-800 text-white overflow-hidden">
    <!-- Background Pattern -->
    <div class="absolute inset-0 bg-black opacity-20"></div>
    <div class="absolute inset-0">
      <div class="absolute top-10 left-10 w-20 h-20 border border-white opacity-10 rounded-full"></div>
      <div class="absolute top-32 right-20 w-16 h-16 border border-white opacity-10 rounded-full"></div>
      <div class="absolute bottom-20 left-1/4 w-12 h-12 border border-white opacity-10 rounded-full"></div>
      <div class="absolute bottom-32 right-1/3 w-8 h-8 border border-white opacity-10 rounded-full"></div>
    </div>

    <div class="relative max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-20 lg:py-32">
      <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
        <!-- Content -->
        <div class="text-center lg:text-left">
          <h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-6">
            Hollanda'da
            <span class="text-yellow-400">Güvenli Sürücü</span>
            Olun
          </h1>
          <p class="text-xl md:text-2xl text-blue-100 mb-8 leading-relaxed">
            15 yıllık deneyimimizle araba ve motor direksiyon dersleri veriyoruz. 
            Başarı oranımız %95'in üzerinde!
          </p>
          
          <!-- Features -->
          <div class="grid grid-cols-1 sm:grid-cols-3 gap-4 mb-8">
            <div class="flex items-center justify-center lg:justify-start">
              <svg class="h-6 w-6 text-yellow-400 mr-2" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
              </svg>
              <span class="text-blue-100">%95 Başarı Oranı</span>
            </div>
            <div class="flex items-center justify-center lg:justify-start">
              <svg class="h-6 w-6 text-yellow-400 mr-2" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
              </svg>
              <span class="text-blue-100">15 Yıl Deneyim</span>
            </div>
            <div class="flex items-center justify-center lg:justify-start">
              <svg class="h-6 w-6 text-yellow-400 mr-2" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
              </svg>
              <span class="text-blue-100">Esnek Saatler</span>
            </div>
          </div>

          <!-- CTA Buttons -->
          <div class="flex flex-col sm:flex-row gap-4 justify-center lg:justify-start">
            <button class="bg-yellow-400 text-blue-900 px-8 py-4 rounded-lg font-bold text-lg hover:bg-yellow-300 transition-colors shadow-lg">
              Ücretsiz Danışmanlık Al
            </button>
            <button class="border-2 border-white text-white px-8 py-4 rounded-lg font-bold text-lg hover:bg-white hover:text-blue-900 transition-colors">
              Hizmetlerimizi İncele
            </button>
          </div>
        </div>

        <!-- Image/Visual -->
        <div class="relative">
          <div class="bg-white bg-opacity-10 backdrop-blur-sm rounded-2xl p-8 shadow-2xl">
            <!-- Car Icon -->
            <div class="text-center mb-6">
              <div class="inline-flex items-center justify-center w-24 h-24 bg-yellow-400 rounded-full mb-4">
                <svg class="h-12 w-12 text-blue-900" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 7h12m0 0l-4-4m4 4l-4 4m0 6H4m0 0l4 4m-4-4l4-4" />
                </svg>
              </div>
              <h3 class="text-2xl font-bold text-white mb-2">Araba Dersleri</h3>
              <p class="text-blue-100">B Sınıfı Ehliyet</p>
            </div>

            <!-- Motor Icon -->
            <div class="text-center">
              <div class="inline-flex items-center justify-center w-24 h-24 bg-yellow-400 rounded-full mb-4">
                <svg class="h-12 w-12 text-blue-900" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z" />
                </svg>
              </div>
              <h3 class="text-2xl font-bold text-white mb-2">Motor Dersleri</h3>
              <p class="text-blue-100">A Sınıfı Ehliyet</p>
            </div>
          </div>

          <!-- Floating Elements -->
          <div class="absolute -top-4 -right-4 w-16 h-16 bg-yellow-400 rounded-full opacity-80 animate-pulse"></div>
          <div class="absolute -bottom-4 -left-4 w-12 h-12 bg-white rounded-full opacity-60 animate-bounce"></div>
        </div>
      </div>
    </div>

    <!-- Scroll Indicator -->
    <div class="absolute bottom-8 left-1/2 transform -translate-x-1/2 animate-bounce">
      <svg class="h-6 w-6 text-white" fill="none" viewBox="0 0 24 24" stroke="currentColor">
        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 14l-7 7m0 0l-7-7m7 7V3" />
      </svg>
    </div>
  </section>
</template>

<script setup>
// Hero section logic can be added here if needed
</script>
