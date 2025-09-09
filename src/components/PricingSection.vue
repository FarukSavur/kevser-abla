<template>
  <section id="pricing"
    class="py-20 bg-gradient-to-br from-slate-900 via-blue-900 to-indigo-900 relative overflow-hidden">
    <!-- Background Elements -->
    <div class="absolute inset-0">
      <div class="absolute top-1/4 left-1/4 w-96 h-96 bg-orange-500/10 rounded-full blur-3xl animate-pulse"></div>
      <div
        class="absolute bottom-1/4 right-1/4 w-80 h-80 bg-blue-500/10 rounded-full blur-3xl animate-pulse delay-1000">
      </div>
      <div
        class="absolute top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2 w-64 h-64 bg-purple-500/10 rounded-full blur-3xl animate-pulse delay-500">
      </div>

      <!-- Floating Elements -->
      <div class="absolute top-20 left-20 w-4 h-4 bg-orange-400/30 rounded-full animate-bounce delay-300"></div>
      <div class="absolute top-40 right-32 w-6 h-6 bg-blue-400/40 rounded-full animate-bounce delay-700"></div>
      <div class="absolute bottom-32 left-1/3 w-3 h-3 bg-purple-300/50 rounded-full animate-bounce delay-1000"></div>
      <div class="absolute bottom-20 right-20 w-5 h-5 bg-orange-300/20 rounded-full animate-bounce delay-500"></div>
    </div>

    <div class="relative max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <!-- Section Header -->
      <div class="text-center mb-16">
        <div
          class="inline-flex items-center px-4 py-2 bg-white/10 backdrop-blur-sm border border-white/20 rounded-full text-sm font-medium text-white/90 mb-6">
          <svg class="w-4 h-4 mr-2 text-orange-400" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
              d="M12 8c-1.657 0-3 .895-3 2s1.343 2 3 2 3 .895 3 2-1.343 2-3 2m0-8c1.11 0 2.08.402 2.599 1M12 8V7m0 1v8m0 0v1m0-1c-1.11 0-2.08-.402-2.599-1" />
          </svg>
          Lespakketten
        </div>
        <h2 class="text-5xl md:text-6xl font-bold mb-6">
          <span class="bg-gradient-to-r from-white via-orange-200 to-orange-400 bg-clip-text text-transparent">
            Lespakketten
          </span>
        </h2>
        <p class="text-xl text-gray-300 max-w-3xl mx-auto leading-relaxed">
          Kies het lespakket dat bij jou past. Al onze pakketten worden gegeven door professionele instructeurs.
        </p>
      </div>

      <!-- Pricing Cards Swiper -->
      <div class="relative pt-8">
        <Swiper :modules="modules" :slides-per-view="1" :space-between="30" :autoplay="{
          delay: 5000,
          disableOnInteraction: false,
        }" :pagination="{
            clickable: true,
            dynamicBullets: true,
          }" :navigation="{
            nextEl: '.swiper-button-next-custom',
            prevEl: '.swiper-button-prev-custom',
          }" :breakpoints="{
            640: {
              slidesPerView: 1,
              spaceBetween: 20,
            },
            768: {
              slidesPerView: 2,
              spaceBetween: 30,
            },
            1024: {
              slidesPerView: 3,
              spaceBetween: 30,
            },
          }" class="pricing-swiper">
          <!-- Basic Package -->
          <SwiperSlide>
            <div
              class="relative bg-white/10 backdrop-blur-md rounded-3xl shadow-2xl p-8 h-full transform hover:scale-105 transition-all duration-300 hover:shadow-2xl border border-white/20 overflow-hidden group">
              <!-- Background Gradient -->
              <div class="absolute inset-0 bg-gradient-to-br from-blue-500/5 to-blue-600/5"></div>
              <div
                class="absolute top-0 right-0 w-32 h-32 bg-gradient-to-br from-blue-400/10 to-blue-600/10 rounded-full blur-2xl">
              </div>

              <div class="relative z-10 text-center">
                <div class="relative inline-block mb-6">
                  <div
                    class="absolute inset-0 bg-gradient-to-r from-blue-500 to-blue-600 rounded-2xl blur-lg opacity-50 group-hover:opacity-75 transition-opacity duration-300">
                  </div>
                  <div
                    class="relative bg-gradient-to-r from-blue-500 to-blue-600 p-4 rounded-2xl shadow-xl group-hover:scale-105 transition-transform duration-300">
                    <svg class="w-8 h-8 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                        d="M12 6.253v13m0-13C10.832 5.477 9.246 5 7.5 5S4.168 5.477 3 6.253v13C4.168 18.477 5.754 18 7.5 18s3.332.477 4.5 1.253m0-13C13.168 5.477 14.754 5 16.5 5c1.746 0 3.332.477 4.5 1.253v13C19.832 18.477 18.246 18 16.5 18c-1.746 0-3.332.477-4.5 1.253">
                      </path>
                    </svg>
                  </div>
                </div>
                <h3 class="text-2xl font-bold text-white mb-4">Basis Pakket</h3>
                <div class="mb-6">
                  <span
                    class="text-5xl font-bold bg-gradient-to-r from-blue-400 to-blue-600 bg-clip-text text-transparent">€45</span>
                  <span class="text-gray-300 ml-2">/les</span>
                </div>
                <p class="text-gray-300 mb-8">Ideaal voor beginners</p>
              </div>

              <ul class="space-y-4 mb-8">
                <li class="flex items-center p-2 rounded-lg hover:bg-white/5 transition-colors duration-200">
                  <div class="w-8 h-8 bg-green-100 rounded-full flex items-center justify-center mr-3">
                    <svg class="w-4 h-4 text-green-600" fill="currentColor" viewBox="0 0 20 20">
                      <path fill-rule="evenodd"
                        d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
                        clip-rule="evenodd"></path>
                    </svg>
                  </div>
                  <span class="text-gray-300 font-medium">60 minuten les</span>
                </li>
                <li class="flex items-center p-2 rounded-lg hover:bg-white/5 transition-colors duration-200">
                  <div class="w-8 h-8 bg-green-100 rounded-full flex items-center justify-center mr-3">
                    <svg class="w-4 h-4 text-green-600" fill="currentColor" viewBox="0 0 20 20">
                      <path fill-rule="evenodd"
                        d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
                        clip-rule="evenodd"></path>
                    </svg>
                  </div>
                  <span class="text-gray-300 font-medium">Basis verkeersregels</span>
                </li>
                <li class="flex items-center p-2 rounded-lg hover:bg-white/5 transition-colors duration-200">
                  <div class="w-8 h-8 bg-green-100 rounded-full flex items-center justify-center mr-3">
                    <svg class="w-4 h-4 text-green-600" fill="currentColor" viewBox="0 0 20 20">
                      <path fill-rule="evenodd"
                        d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
                        clip-rule="evenodd"></path>
                    </svg>
                  </div>
                  <span class="text-gray-300 font-medium">Voertuigbediening</span>
                </li>
                <li class="flex items-center p-2 rounded-lg hover:bg-white/5 transition-colors duration-200">
                  <div class="w-8 h-8 bg-green-100 rounded-full flex items-center justify-center mr-3">
                    <svg class="w-4 h-4 text-green-600" fill="currentColor" viewBox="0 0 20 20">
                      <path fill-rule="evenodd"
                        d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
                        clip-rule="evenodd"></path>
                    </svg>
                  </div>
                  <span class="text-gray-300 font-medium">Veilige rijtechnieken</span>
                </li>
              </ul>

              <button
                class="group relative w-full bg-gradient-to-r from-blue-600 to-blue-700 text-white py-3 px-6 rounded-2xl font-bold shadow-lg hover:shadow-xl transition-all duration-300 hover:scale-105 overflow-hidden">
                <span class="relative z-10 flex items-center justify-center">
                  Pakket Kiezen
                  <svg class="w-5 h-5 ml-2 group-hover:translate-x-1 transition-transform duration-300" fill="none"
                    viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                      d="M13 7l5 5m0 0l-5 5m5-5H6" />
                  </svg>
                </span>
                <div
                  class="absolute inset-0 bg-gradient-to-r from-blue-700 to-blue-800 opacity-0 group-hover:opacity-100 transition-opacity duration-300">
                </div>
              </button>
            </div>
          </SwiperSlide>

          <!-- Premium Package -->
          <SwiperSlide>
            <div
              class="relative bg-white/10 backdrop-blur-md rounded-3xl shadow-2xl p-8 h-full transform hover:scale-105 transition-all duration-300 hover:shadow-2xl border border-white/20  group">
              <!-- Popular Badge -->
              <div class="absolute -top-4 left-1/2 transform -translate-x-1/2 z-30">
                <span
                  class="bg-gradient-to-r from-orange-500 to-orange-600 text-white px-6 py-2 rounded-full text-sm font-bold shadow-lg animate-pulse">
                  Meest Populair
                </span>
              </div>

              <!-- Background Gradient -->
              <div class="absolute inset-0 bg-gradient-to-br from-orange-500/5 to-orange-600/5"></div>
              <div
                class="absolute top-0 right-0 w-32 h-32 bg-gradient-to-br from-orange-400/10 to-orange-600/10 rounded-full blur-2xl">
              </div>

              <div class="relative z-10 text-center">
                <div class="relative inline-block mb-6">
                  <div
                    class="absolute inset-0 bg-gradient-to-r from-orange-500 to-orange-600 rounded-2xl blur-lg opacity-50 group-hover:opacity-75 transition-opacity duration-300">
                  </div>
                  <div
                    class="relative bg-gradient-to-r from-orange-500 to-orange-600 p-4 rounded-2xl shadow-xl group-hover:scale-105 transition-transform duration-300">
                    <svg class="w-8 h-8 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                        d="M11.049 2.927c.3-.921 1.603-.921 1.902 0l1.519 4.674a1 1 0 00.95.69h4.915c.969 0 1.371 1.24.588 1.81l-3.976 2.888a1 1 0 00-.363 1.118l1.518 4.674c.3.922-.755 1.688-1.538 1.118l-3.976-2.888a1 1 0 00-1.176 0l-3.976 2.888c-.783.57-1.838-.197-1.538-1.118l1.518-4.674a1 1 0 00-.363-1.118l-3.976-2.888c-.784-.57-.38-1.81.588-1.81h4.914a1 1 0 00.951-.69l1.519-4.674z">
                      </path>
                    </svg>
                  </div>
                </div>
                <h3 class="text-2xl font-bold text-white mb-4">Premium Pakket</h3>
                <div class="mb-6">
                  <span
                    class="text-5xl font-bold bg-gradient-to-r from-orange-400 to-orange-600 bg-clip-text text-transparent">€40</span>
                  <span class="text-gray-300 ml-2">/les</span>
                  <!-- <div class="text-sm text-gray-400 line-through">€45</div> -->
                </div>
                <p class="text-gray-300 mb-8">Meest gekozen pakket</p>
              </div>

              <ul class="space-y-4 mb-8">
                <li class="flex items-center p-2 rounded-lg hover:bg-white/5 transition-colors duration-200">
                  <div class="w-8 h-8 bg-green-100 rounded-full flex items-center justify-center mr-3">
                    <svg class="w-4 h-4 text-green-600" fill="currentColor" viewBox="0 0 20 20">
                      <path fill-rule="evenodd"
                        d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
                        clip-rule="evenodd"></path>
                    </svg>
                  </div>
                  <span class="text-gray-300 font-medium">60 minuten les</span>
                </li>
                <li class="flex items-center p-2 rounded-lg hover:bg-white/5 transition-colors duration-200">
                  <div class="w-8 h-8 bg-green-100 rounded-full flex items-center justify-center mr-3">
                    <svg class="w-4 h-4 text-green-600" fill="currentColor" viewBox="0 0 20 20">
                      <path fill-rule="evenodd"
                        d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
                        clip-rule="evenodd"></path>
                    </svg>
                  </div>
                  <span class="text-gray-300 font-medium">10 lessen pakket</span>
                </li>
                <li class="flex items-center p-2 rounded-lg hover:bg-white/5 transition-colors duration-200">
                  <div class="w-8 h-8 bg-green-100 rounded-full flex items-center justify-center mr-3">
                    <svg class="w-4 h-4 text-green-600" fill="currentColor" viewBox="0 0 20 20">
                      <path fill-rule="evenodd"
                        d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
                        clip-rule="evenodd"></path>
                    </svg>
                  </div>
                  <span class="text-gray-300 font-medium">Theorie les ondersteuning</span>
                </li>
                <li class="flex items-center p-2 rounded-lg hover:bg-white/5 transition-colors duration-200">
                  <div class="w-8 h-8 bg-green-100 rounded-full flex items-center justify-center mr-3">
                    <svg class="w-4 h-4 text-green-600" fill="currentColor" viewBox="0 0 20 20">
                      <path fill-rule="evenodd"
                        d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
                        clip-rule="evenodd"></path>
                    </svg>
                  </div>
                  <span class="text-gray-300 font-medium">Examen voorbereiding</span>
                </li>
              </ul>

              <button
                class="group relative w-full bg-gradient-to-r from-orange-600 to-orange-700 text-white py-3 px-6 rounded-2xl font-bold shadow-lg hover:shadow-xl transition-all duration-300 hover:scale-105 overflow-hidden">
                <span class="relative z-10 flex items-center justify-center">
                  Pakket Kiezen
                  <svg class="w-5 h-5 ml-2 group-hover:translate-x-1 transition-transform duration-300" fill="none"
                    viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                      d="M13 7l5 5m0 0l-5 5m5-5H6" />
                  </svg>
                </span>
                <div
                  class="absolute inset-0 bg-gradient-to-r from-orange-700 to-orange-800 opacity-0 group-hover:opacity-100 transition-opacity duration-300">
                </div>
              </button>
            </div>
          </SwiperSlide>

          <!-- Intensive Package -->
          <SwiperSlide>
            <div
              class="relative bg-white/10 backdrop-blur-md rounded-3xl shadow-2xl p-8 h-full transform hover:scale-105 transition-all duration-300 hover:shadow-2xl border border-white/20 overflow-hidden group">
              <!-- Background Gradient -->
              <div class="absolute inset-0 bg-gradient-to-br from-green-500/5 to-green-600/5"></div>
              <div
                class="absolute top-0 right-0 w-32 h-32 bg-gradient-to-br from-green-400/10 to-green-600/10 rounded-full blur-2xl">
              </div>

              <div class="relative z-10 text-center">
                <div class="relative inline-block mb-6">
                  <div
                    class="absolute inset-0 bg-gradient-to-r from-green-500 to-green-600 rounded-2xl blur-lg opacity-50 group-hover:opacity-75 transition-opacity duration-300">
                  </div>
                  <div
                    class="relative bg-gradient-to-r from-green-500 to-green-600 p-4 rounded-2xl shadow-xl group-hover:scale-105 transition-transform duration-300">
                    <svg class="w-8 h-8 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                        d="M13 10V3L4 14h7v7l9-11h-7z"></path>
                    </svg>
                  </div>
                </div>
                <h3 class="text-2xl font-bold text-white mb-4">Intensief Pakket</h3>
                <div class="mb-6">
                  <span
                    class="text-5xl font-bold bg-gradient-to-r from-green-400 to-green-600 bg-clip-text text-transparent">€35</span>
                  <span class="text-gray-300 ml-2">/les</span>
                  <!-- <div class="text-sm text-gray-400 line-through">€45</div> -->
                </div>
                <p class="text-gray-300 mb-8">Ideaal voor snelle leerling</p>
              </div>

              <ul class="space-y-4 mb-8">
                <li class="flex items-center p-2 rounded-lg hover:bg-white/5 transition-colors duration-200">
                  <div class="w-8 h-8 bg-green-100 rounded-full flex items-center justify-center mr-3">
                    <svg class="w-4 h-4 text-green-600" fill="currentColor" viewBox="0 0 20 20">
                      <path fill-rule="evenodd"
                        d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
                        clip-rule="evenodd"></path>
                    </svg>
                  </div>
                  <span class="text-gray-300 font-medium">60 minuten les</span>
                </li>
                <li class="flex items-center p-2 rounded-lg hover:bg-white/5 transition-colors duration-200">
                  <div class="w-8 h-8 bg-green-100 rounded-full flex items-center justify-center mr-3">
                    <svg class="w-4 h-4 text-green-600" fill="currentColor" viewBox="0 0 20 20">
                      <path fill-rule="evenodd"
                        d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
                        clip-rule="evenodd"></path>
                    </svg>
                  </div>
                  <span class="text-gray-300 font-medium">20 lessen pakket</span>
                </li>
                <li class="flex items-center p-2 rounded-lg hover:bg-white/5 transition-colors duration-200">
                  <div class="w-8 h-8 bg-green-100 rounded-full flex items-center justify-center mr-3">
                    <svg class="w-4 h-4 text-green-600" fill="currentColor" viewBox="0 0 20 20">
                      <path fill-rule="evenodd"
                        d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
                        clip-rule="evenodd"></path>
                    </svg>
                  </div>
                  <span class="text-gray-300 font-medium">Dagelijkse lessen mogelijk</span>
                </li>
                <li class="flex items-center p-2 rounded-lg hover:bg-white/5 transition-colors duration-200">
                  <div class="w-8 h-8 bg-green-100 rounded-full flex items-center justify-center mr-3">
                    <svg class="w-4 h-4 text-green-600" fill="currentColor" viewBox="0 0 20 20">
                      <path fill-rule="evenodd"
                        d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
                        clip-rule="evenodd"></path>
                    </svg>
                  </div>
                  <span class="text-gray-300 font-medium">Persoonlijke instructeur</span>
                </li>
              </ul>

              <button
                class="group relative w-full bg-gradient-to-r from-green-600 to-green-700 text-white py-3 px-6 rounded-2xl font-bold shadow-lg hover:shadow-xl transition-all duration-300 hover:scale-105 overflow-hidden">
                <span class="relative z-10 flex items-center justify-center">
                  Pakket Kiezen
                  <svg class="w-5 h-5 ml-2 group-hover:translate-x-1 transition-transform duration-300" fill="none"
                    viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                      d="M13 7l5 5m0 0l-5 5m5-5H6" />
                  </svg>
                </span>
                <div
                  class="absolute inset-0 bg-gradient-to-r from-green-700 to-green-800 opacity-0 group-hover:opacity-100 transition-opacity duration-300">
                </div>
              </button>
            </div>
          </SwiperSlide>

          <!-- Exam Package -->
          <SwiperSlide>
            <div
              class="relative bg-white/10 backdrop-blur-md rounded-3xl shadow-2xl p-8 h-full transform hover:scale-105 transition-all duration-300 hover:shadow-2xl border border-white/20 overflow-hidden group">
              <!-- Background Gradient -->
              <div class="absolute inset-0 bg-gradient-to-br from-orange-500/5 to-orange-600/5"></div>
              <div
                class="absolute top-0 right-0 w-32 h-32 bg-gradient-to-br from-orange-400/10 to-orange-600/10 rounded-full blur-2xl">
              </div>

              <div class="relative z-10 text-center">
                <div class="relative inline-block mb-6">
                  <div
                    class="absolute inset-0 bg-gradient-to-r from-orange-500 to-orange-600 rounded-2xl blur-lg opacity-50 group-hover:opacity-75 transition-opacity duration-300">
                  </div>
                  <div
                    class="relative bg-gradient-to-r from-orange-500 to-orange-600 p-4 rounded-2xl shadow-xl group-hover:scale-105 transition-transform duration-300">
                    <svg class="w-8 h-8 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                        d="M9 12l2 2 4-4M7.835 4.697a3.42 3.42 0 001.946-.806 3.42 3.42 0 014.438 0 3.42 3.42 0 001.946.806 3.42 3.42 0 013.138 3.138 3.42 3.42 0 00.806 1.946 3.42 3.42 0 010 4.438 3.42 3.42 0 00-.806 1.946 3.42 3.42 0 01-3.138 3.138 3.42 3.42 0 00-1.946.806 3.42 3.42 0 01-4.438 0 3.42 3.42 0 00-1.946-.806 3.42 3.42 0 01-3.138-3.138 3.42 3.42 0 00-.806-1.946 3.42 3.42 0 010-4.438 3.42 3.42 0 00.806-1.946 3.42 3.42 0 013.138-3.138z">
                      </path>
                    </svg>
                  </div>
                </div>
                <h3 class="text-2xl font-bold text-white mb-4">Examen Pakket</h3>
                <div class="mb-6">
                  <span
                    class="text-5xl font-bold bg-gradient-to-r from-orange-400 to-orange-600 bg-clip-text text-transparent">€50</span>
                  <span class="text-gray-300 ml-2">/les</span>
                </div>
                <p class="text-gray-300 mb-8">Voorbereiding voor examen</p>
              </div>

              <ul class="space-y-4 mb-8">
                <li class="flex items-center p-2 rounded-lg hover:bg-white/5 transition-colors duration-200">
                  <div class="w-8 h-8 bg-green-100 rounded-full flex items-center justify-center mr-3">
                    <svg class="w-4 h-4 text-green-600" fill="currentColor" viewBox="0 0 20 20">
                      <path fill-rule="evenodd"
                        d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
                        clip-rule="evenodd"></path>
                    </svg>
                  </div>
                  <span class="text-gray-300 font-medium">90 minuten les</span>
                </li>
                <li class="flex items-center p-2 rounded-lg hover:bg-white/5 transition-colors duration-200">
                  <div class="w-8 h-8 bg-green-100 rounded-full flex items-center justify-center mr-3">
                    <svg class="w-4 h-4 text-green-600" fill="currentColor" viewBox="0 0 20 20">
                      <path fill-rule="evenodd"
                        d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
                        clip-rule="evenodd"></path>
                    </svg>
                  </div>
                  <span class="text-gray-300 font-medium">Examen simulatie</span>
                </li>
                <li class="flex items-center p-2 rounded-lg hover:bg-white/5 transition-colors duration-200">
                  <div class="w-8 h-8 bg-green-100 rounded-full flex items-center justify-center mr-3">
                    <svg class="w-4 h-4 text-green-600" fill="currentColor" viewBox="0 0 20 20">
                      <path fill-rule="evenodd"
                        d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
                        clip-rule="evenodd"></path>
                    </svg>
                  </div>
                  <span class="text-gray-300 font-medium">Praktijk examen</span>
                </li>
                <li class="flex items-center p-2 rounded-lg hover:bg-white/5 transition-colors duration-200">
                  <div class="w-8 h-8 bg-green-100 rounded-full flex items-center justify-center mr-3">
                    <svg class="w-4 h-4 text-green-600" fill="currentColor" viewBox="0 0 20 20">
                      <path fill-rule="evenodd"
                        d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
                        clip-rule="evenodd"></path>
                    </svg>
                  </div>
                  <span class="text-gray-300 font-medium">Examen dag ondersteuning</span>
                </li>
              </ul>

              <button
                class="group relative w-full bg-gradient-to-r from-orange-600 to-orange-700 text-white py-3 px-6 rounded-2xl font-bold shadow-lg hover:shadow-xl transition-all duration-300 hover:scale-105 overflow-hidden">
                <span class="relative z-10 flex items-center justify-center">
                  Pakket Kiezen
                  <svg class="w-5 h-5 ml-2 group-hover:translate-x-1 transition-transform duration-300" fill="none"
                    viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                      d="M13 7l5 5m0 0l-5 5m5-5H6" />
                  </svg>
                </span>
                <div
                  class="absolute inset-0 bg-gradient-to-r from-orange-700 to-orange-800 opacity-0 group-hover:opacity-100 transition-opacity duration-300">
                </div>
              </button>
            </div>
          </SwiperSlide>
        </Swiper>

        <!-- Custom Navigation Buttons -->
        <button
          class="swiper-button-prev-custom absolute left-0 top-1/2 transform -translate-y-1/2 -translate-x-4 z-10 bg-white rounded-full p-4 shadow-lg hover:shadow-xl transition-all duration-300 hover:scale-110 border-2 border-gray-100 hover:border-blue-300 group">
          <svg class="w-6 h-6 text-gray-600 group-hover:text-blue-600 transition-colors duration-300" fill="none"
            stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 19l-7-7 7-7"></path>
          </svg>
        </button>
        <button
          class="swiper-button-next-custom absolute right-0 top-1/2 transform -translate-y-1/2 translate-x-4 z-10 bg-white rounded-full p-4 shadow-lg hover:shadow-xl transition-all duration-300 hover:scale-110 border-2 border-gray-100 hover:border-blue-300 group">
          <svg class="w-6 h-6 text-gray-600 group-hover:text-blue-600 transition-colors duration-300" fill="none"
            stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7"></path>
          </svg>
        </button>
      </div>

      <!-- Additional Info -->
      <div class="mt-16 text-center">
        <div
          class="relative bg-white/10 backdrop-blur-md rounded-3xl shadow-2xl p-8 max-w-4xl mx-auto border border-white/20 overflow-hidden">
          <!-- Background Gradient -->
          <div class="absolute inset-0 bg-gradient-to-br from-white/5 to-white/10"></div>
          <div
            class="absolute top-0 right-0 w-32 h-32 bg-gradient-to-br from-orange-400/10 to-orange-600/10 rounded-full blur-2xl">
          </div>

          <div class="relative z-10">
            <h3 class="text-3xl font-bold text-white mb-8">Waarom Kevser Abla Rijschool?</h3>
            <div class="grid md:grid-cols-3 gap-8">
              <div class="text-center group">
                <div class="relative inline-block mb-4">
                  <div
                    class="absolute inset-0 bg-gradient-to-r from-blue-500 to-blue-600 rounded-2xl blur-lg opacity-50 group-hover:opacity-75 transition-opacity duration-300">
                  </div>
                  <div
                    class="relative bg-gradient-to-r from-blue-500 to-blue-600 p-3 rounded-2xl shadow-xl group-hover:scale-105 transition-transform duration-300">
                    <svg class="w-6 h-6 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                        d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z"></path>
                    </svg>
                  </div>
                </div>
                <h4 class="font-bold text-white mb-2">Flexibel Rooster</h4>
                <p class="text-gray-300 text-sm">Lessen op tijden die jou uitkomen</p>
              </div>
              <div class="text-center group">
                <div class="relative inline-block mb-4">
                  <div
                    class="absolute inset-0 bg-gradient-to-r from-green-500 to-green-600 rounded-2xl blur-lg opacity-50 group-hover:opacity-75 transition-opacity duration-300">
                  </div>
                  <div
                    class="relative bg-gradient-to-r from-green-500 to-green-600 p-3 rounded-2xl shadow-xl group-hover:scale-105 transition-transform duration-300">
                    <svg class="w-6 h-6 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                        d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z"></path>
                    </svg>
                  </div>
                </div>
                <h4 class="font-bold text-white mb-2">95% Slagingspercentage</h4>
                <p class="text-gray-300 text-sm">De meeste van onze leerlingen slagen in één keer</p>
              </div>
              <div class="text-center group">
                <div class="relative inline-block mb-4">
                  <div
                    class="absolute inset-0 bg-gradient-to-r from-purple-500 to-purple-600 rounded-2xl blur-lg opacity-50 group-hover:opacity-75 transition-opacity duration-300">
                  </div>
                  <div
                    class="relative bg-gradient-to-r from-purple-500 to-purple-600 p-3 rounded-2xl shadow-xl group-hover:scale-105 transition-transform duration-300">
                    <svg class="w-6 h-6 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                        d="M17 20h5v-2a3 3 0 00-5.356-1.857M17 20H7m10 0v-2c0-.656-.126-1.283-.356-1.857M7 20H2v-2a3 3 0 015.356-1.857M7 20v-2c0-.656.126-1.283.356-1.857m0 0a5.002 5.002 0 019.288 0M15 7a3 3 0 11-6 0 3 3 0 016 0zm6 3a2 2 0 11-4 0 2 2 0 014 0zM7 10a2 2 0 11-4 0 2 2 0 014 0z">
                      </path>
                    </svg>
                  </div>
                </div>
                <h4 class="font-bold text-white mb-2">Ervaren Instructeurs</h4>
                <p class="text-gray-300 text-sm">Professionele instructeurs met jarenlange ervaring</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { Swiper, SwiperSlide } from 'swiper/vue'
import { Autoplay, Pagination, Navigation } from 'swiper/modules'

// Import Swiper styles
import 'swiper/css'
import 'swiper/css/pagination'
import 'swiper/css/navigation'

const modules = [Autoplay, Pagination, Navigation]
</script>

<style scoped>
.pricing-swiper {
  padding: 20px 0 60px 0;
}

.pricing-swiper :deep(.swiper-pagination) {
  bottom: 20px;
}

/* Custom Navigation Buttons Styling */
.swiper-button-prev-custom,
.swiper-button-next-custom {
  width: 56px;
  height: 56px;
  display: flex;
  align-items: center;
  justify-content: center;
  background: white;
  border-radius: 50%;
  box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06);
  transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
  border: 2px solid #f3f4f6;
}


.swiper-button-prev-custom:active,
.swiper-button-next-custom:active {
  transform: scale(0.95);
}

.swiper-button-prev-custom svg,
.swiper-button-next-custom svg {
  transition: all 0.3s ease;
}


/* Responsive adjustments */
@media (max-width: 768px) {

  .swiper-button-prev-custom,
  .swiper-button-next-custom {
    width: 48px;
    height: 48px;
    padding: 12px;
  }

  .swiper-button-prev-custom {
    left: 8px;
  }

  .swiper-button-next-custom {
    right: 8px;
  }
}
</style>
