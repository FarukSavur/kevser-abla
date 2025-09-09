<template>
  <section id="services" class="py-20 bg-gradient-to-br from-slate-50 via-blue-50 to-indigo-50 relative overflow-hidden">
    <!-- Background Elements -->
    <div class="absolute inset-0">
      <div class="absolute top-1/4 left-1/4 w-96 h-96 bg-blue-500/5 rounded-full blur-3xl animate-pulse"></div>
      <div class="absolute bottom-1/4 right-1/4 w-80 h-80 bg-orange-500/5 rounded-full blur-3xl animate-pulse delay-1000"></div>
      <div class="absolute top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2 w-64 h-64 bg-purple-500/5 rounded-full blur-3xl animate-pulse delay-500"></div>
      
      <!-- Floating Elements -->
      <div class="absolute top-20 left-20 w-4 h-4 bg-blue-400/30 rounded-full animate-bounce delay-300"></div>
      <div class="absolute top-40 right-32 w-3 h-3 bg-orange-400/40 rounded-full animate-bounce delay-700"></div>
      <div class="absolute bottom-32 left-40 w-5 h-5 bg-purple-400/30 rounded-full animate-bounce delay-1000"></div>
      <div class="absolute bottom-20 right-20 w-4 h-4 bg-indigo-400/30 rounded-full animate-bounce delay-500"></div>
    </div>

    <div class="relative max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <!-- Section Header -->
      <div class="text-center mb-16">
        <div class="inline-flex items-center px-4 py-2 bg-white/80 backdrop-blur-sm border border-blue-200/50 rounded-full text-sm font-medium text-blue-700 mb-6">
          <svg class="w-4 h-4 mr-2 text-blue-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 21V5a2 2 0 00-2-2H7a2 2 0 00-2 2v16m14 0h2m-2 0h-5m-9 0H3m2 0h5M9 7h1m-1 4h1m4-4h1m-1 4h1m-5 10v-5a1 1 0 011-1h2a1 1 0 011 1v5m-4 0h4" />
          </svg>
          Onze Diensten
        </div>
        <h2 class="text-5xl md:text-6xl font-bold mb-6">
          <span class="bg-gradient-to-r from-slate-900 via-blue-900 to-indigo-900 bg-clip-text text-transparent">
            Onze Diensten
          </span>
        </h2>
        <p class="text-xl text-gray-600 max-w-3xl mx-auto leading-relaxed">
          Voor het behalen van je autorijbewijs en motorrijbewijs in Nederland bieden wij
          alle diensten aan met onze professionele instructeurs.
        </p>
      </div>

      <!-- Services Swiper -->
      <div class="relative pt-8">
        <swiper
          :modules="modules"
          :autoplay="{
            delay: 4000,
            disableOnInteraction: false,
          }"
          :loop="true"
          :slides-per-view="1"
          :space-between="30"
          :grab-cursor="true"
          :pagination="{ clickable: true }"
          :navigation="true"
          :breakpoints="{
            640: {
              slidesPerView: 2,
              spaceBetween: 20,
            },
            1024: {
              slidesPerView: 3,
              spaceBetween: 30,
            },
          }"
          class="services-swiper"
        >
          <!-- B Rijbewijs -->
          <swiper-slide>
            <div class="relative bg-white/80 backdrop-blur-md rounded-3xl shadow-xl hover:shadow-2xl transition-all duration-300 p-8 group h-full border border-white/20 overflow-hidden">
              <!-- Background Gradient -->
              <div class="absolute inset-0 bg-gradient-to-br from-blue-500/5 to-blue-600/5"></div>
              <div class="absolute top-0 right-0 w-32 h-32 bg-gradient-to-br from-blue-400/10 to-blue-600/10 rounded-full blur-2xl"></div>
              
              <div class="relative z-10 text-center">
                <div class="relative inline-block mb-6">
                  <div class="absolute inset-0 bg-gradient-to-r from-blue-500 to-blue-600 rounded-2xl blur-lg opacity-50 group-hover:opacity-75 transition-opacity duration-300"></div>
                  <div class="relative bg-gradient-to-r from-blue-500 to-blue-600 p-6 rounded-2xl shadow-xl group-hover:scale-105 transition-transform duration-300">
                    <svg class="h-12 w-12 text-white" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                        d="M8 7h12m0 0l-4-4m4 4l-4 4m0 6H4m0 0l4 4m-4-4l4-4" />
                    </svg>
                  </div>
                </div>
                <h3 class="text-3xl font-bold text-gray-900 mb-4">B Rijbewijs</h3>
                <p class="text-gray-600 mb-6 leading-relaxed text-lg">
                  Krijg alle benodigde theoretische en praktische training voor autorijden.
                  Word een veilige bestuurder met onze ervaren instructeurs.
                </p>
                <ul class="text-left space-y-3 mb-8">
                  <li class="flex items-center text-gray-700 p-2 rounded-lg hover:bg-blue-50 transition-colors duration-200">
                    <div class="w-8 h-8 bg-green-100 rounded-full flex items-center justify-center mr-3">
                      <svg class="h-4 w-4 text-green-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                      </svg>
                    </div>
                    <span class="text-lg font-medium">Theorielessen</span>
                  </li>
                  <li class="flex items-center text-gray-700 p-2 rounded-lg hover:bg-blue-50 transition-colors duration-200">
                    <div class="w-8 h-8 bg-green-100 rounded-full flex items-center justify-center mr-3">
                      <svg class="h-4 w-4 text-green-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                      </svg>
                    </div>
                    <span class="text-lg font-medium">Praktijklessen</span>
                  </li>
                  <li class="flex items-center text-gray-700 p-2 rounded-lg hover:bg-blue-50 transition-colors duration-200">
                    <div class="w-8 h-8 bg-green-100 rounded-full flex items-center justify-center mr-3">
                      <svg class="h-4 w-4 text-green-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                      </svg>
                    </div>
                    <span class="text-lg font-medium">Examen Voorbereiding</span>
                  </li>
                  <li class="flex items-center text-gray-700 p-2 rounded-lg hover:bg-blue-50 transition-colors duration-200">
                    <div class="w-8 h-8 bg-green-100 rounded-full flex items-center justify-center mr-3">
                      <svg class="h-4 w-4 text-green-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                      </svg>
                    </div>
                    <span class="text-lg font-medium">Flexibele Tijden</span>
                  </li>
                </ul>
                <button class="group relative w-full bg-gradient-to-r from-blue-600 to-blue-700 text-white py-4 rounded-2xl font-bold text-lg shadow-lg hover:shadow-xl transition-all duration-300 hover:scale-105 overflow-hidden">
                  <span class="relative z-10 flex items-center justify-center">
                    Bekijk Details
                    <svg class="w-5 h-5 ml-2 group-hover:translate-x-1 transition-transform duration-300" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 7l5 5m0 0l-5 5m5-5H6" />
                    </svg>
                  </span>
                  <div class="absolute inset-0 bg-gradient-to-r from-blue-700 to-blue-800 opacity-0 group-hover:opacity-100 transition-opacity duration-300"></div>
                </button>
              </div>
            </div>
          </swiper-slide>

          <!-- A Rijbewijs -->
          <swiper-slide>
            <div class="relative bg-white/80 backdrop-blur-md rounded-3xl shadow-xl hover:shadow-2xl transition-all duration-300 p-8 group h-full border border-white/20 overflow-hidden">
              <!-- Background Gradient -->
              <div class="absolute inset-0 bg-gradient-to-br from-red-500/5 to-red-600/5"></div>
              <div class="absolute top-0 right-0 w-32 h-32 bg-gradient-to-br from-red-400/10 to-red-600/10 rounded-full blur-2xl"></div>
              
              <div class="relative z-10 text-center">
                <div class="relative inline-block mb-6">
                  <div class="absolute inset-0 bg-gradient-to-r from-red-500 to-red-600 rounded-2xl blur-lg opacity-50 group-hover:opacity-75 transition-opacity duration-300"></div>
                  <div class="relative bg-gradient-to-r from-red-500 to-red-600 p-6 rounded-2xl shadow-xl group-hover:scale-105 transition-transform duration-300">
                    <svg class="h-12 w-12 text-white" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                        d="M13 10V3L4 14h7v7l9-11h-7z" />
                    </svg>
                  </div>
                </div>
                <h3 class="text-3xl font-bold text-gray-900 mb-4">A Rijbewijs</h3>
                <p class="text-gray-600 mb-6 leading-relaxed text-lg">
                  Ons speciale opleidingsprogramma voor motorrijden.
                  Krijg professionele ondersteuning om een veilige motorrijder te worden.
                </p>
                <ul class="text-left space-y-3 mb-8">
                  <li class="flex items-center text-gray-700 p-2 rounded-lg hover:bg-red-50 transition-colors duration-200">
                    <div class="w-8 h-8 bg-green-100 rounded-full flex items-center justify-center mr-3">
                      <svg class="h-4 w-4 text-green-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                      </svg>
                    </div>
                    <span class="text-lg font-medium">Motor Theorie</span>
                  </li>
                  <li class="flex items-center text-gray-700 p-2 rounded-lg hover:bg-red-50 transition-colors duration-200">
                    <div class="w-8 h-8 bg-green-100 rounded-full flex items-center justify-center mr-3">
                      <svg class="h-4 w-4 text-green-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                      </svg>
                    </div>
                    <span class="text-lg font-medium">Praktijk Training</span>
                  </li>
                  <li class="flex items-center text-gray-700 p-2 rounded-lg hover:bg-red-50 transition-colors duration-200">
                    <div class="w-8 h-8 bg-green-100 rounded-full flex items-center justify-center mr-3">
                      <svg class="h-4 w-4 text-green-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                      </svg>
                    </div>
                    <span class="text-lg font-medium">Veiligheidstraining</span>
                  </li>
                  <li class="flex items-center text-gray-700 p-2 rounded-lg hover:bg-red-50 transition-colors duration-200">
                    <div class="w-8 h-8 bg-green-100 rounded-full flex items-center justify-center mr-3">
                      <svg class="h-4 w-4 text-green-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                      </svg>
                    </div>
                    <span class="text-lg font-medium">Moderne Motoren</span>
                  </li>
                </ul>
                <button class="group relative w-full bg-gradient-to-r from-red-600 to-red-700 text-white py-4 rounded-2xl font-bold text-lg shadow-lg hover:shadow-xl transition-all duration-300 hover:scale-105 overflow-hidden">
                  <span class="relative z-10 flex items-center justify-center">
                    Bekijk Details
                    <svg class="w-5 h-5 ml-2 group-hover:translate-x-1 transition-transform duration-300" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 7l5 5m0 0l-5 5m5-5H6" />
                    </svg>
                  </span>
                  <div class="absolute inset-0 bg-gradient-to-r from-red-700 to-red-800 opacity-0 group-hover:opacity-100 transition-opacity duration-300"></div>
                </button>
              </div>
            </div>
          </swiper-slide>

          <!-- Theorielessen -->
          <swiper-slide>
            <div class="relative bg-white/80 backdrop-blur-md rounded-3xl shadow-xl hover:shadow-2xl transition-all duration-300 p-8 group h-full border border-white/20 overflow-hidden">
              <!-- Background Gradient -->
              <div class="absolute inset-0 bg-gradient-to-br from-green-500/5 to-green-600/5"></div>
              <div class="absolute top-0 right-0 w-32 h-32 bg-gradient-to-br from-green-400/10 to-green-600/10 rounded-full blur-2xl"></div>
              
              <div class="relative z-10 text-center">
                <div class="relative inline-block mb-6">
                  <div class="absolute inset-0 bg-gradient-to-r from-green-500 to-green-600 rounded-2xl blur-lg opacity-50 group-hover:opacity-75 transition-opacity duration-300"></div>
                  <div class="relative bg-gradient-to-r from-green-500 to-green-600 p-6 rounded-2xl shadow-xl group-hover:scale-105 transition-transform duration-300">
                    <svg class="h-12 w-12 text-white" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                        d="M12 6.253v13m0-13C10.832 5.477 9.246 5 7.5 5S4.168 5.477 3 6.253v13C4.168 18.477 5.754 18 7.5 18s3.332.477 4.5 1.253m0-13C13.168 5.477 14.754 5 16.5 5c1.746 0 3.332.477 4.5 1.253v13C19.832 18.477 18.246 18 16.5 18c-1.746 0-3.332.477-4.5 1.253" />
                    </svg>
                  </div>
                </div>
                <h3 class="text-3xl font-bold text-gray-900 mb-4">Theorielessen</h3>
                <p class="text-gray-600 mb-6 leading-relaxed text-lg">
                  Krijg uitgebreide theoretische training over verkeersregels,
                  veiligheidsmaatregelen en bestuurdersgedrag.
                </p>
                <ul class="text-left space-y-3 mb-8">
                  <li class="flex items-center text-gray-700 p-2 rounded-lg hover:bg-green-50 transition-colors duration-200">
                    <div class="w-8 h-8 bg-green-100 rounded-full flex items-center justify-center mr-3">
                      <svg class="h-4 w-4 text-green-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                      </svg>
                    </div>
                    <span class="text-lg font-medium">Verkeersregels</span>
                  </li>
                  <li class="flex items-center text-gray-700 p-2 rounded-lg hover:bg-green-50 transition-colors duration-200">
                    <div class="w-8 h-8 bg-green-100 rounded-full flex items-center justify-center mr-3">
                      <svg class="h-4 w-4 text-green-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                      </svg>
                    </div>
                    <span class="text-lg font-medium">Veiligheidstraining</span>
                  </li>
                  <li class="flex items-center text-gray-700 p-2 rounded-lg hover:bg-green-50 transition-colors duration-200">
                    <div class="w-8 h-8 bg-green-100 rounded-full flex items-center justify-center mr-3">
                      <svg class="h-4 w-4 text-green-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                      </svg>
                    </div>
                    <span class="text-lg font-medium">Eerste Hulp</span>
                  </li>
                  <li class="flex items-center text-gray-700 p-2 rounded-lg hover:bg-green-50 transition-colors duration-200">
                    <div class="w-8 h-8 bg-green-100 rounded-full flex items-center justify-center mr-3">
                      <svg class="h-4 w-4 text-green-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                      </svg>
                    </div>
                    <span class="text-lg font-medium">Online Lessen</span>
                  </li>
                </ul>
                <button class="group relative w-full bg-gradient-to-r from-green-600 to-green-700 text-white py-4 rounded-2xl font-bold text-lg shadow-lg hover:shadow-xl transition-all duration-300 hover:scale-105 overflow-hidden">
                  <span class="relative z-10 flex items-center justify-center">
                    Bekijk Details
                    <svg class="w-5 h-5 ml-2 group-hover:translate-x-1 transition-transform duration-300" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 7l5 5m0 0l-5 5m5-5H6" />
                    </svg>
                  </span>
                  <div class="absolute inset-0 bg-gradient-to-r from-green-700 to-green-800 opacity-0 group-hover:opacity-100 transition-opacity duration-300"></div>
                </button>
              </div>
            </div>
          </swiper-slide>

          <!-- Praktijklessen -->
          <swiper-slide>
            <div class="relative bg-white/80 backdrop-blur-md rounded-3xl shadow-xl hover:shadow-2xl transition-all duration-300 p-8 group h-full border border-white/20 overflow-hidden">
              <!-- Background Gradient -->
              <div class="absolute inset-0 bg-gradient-to-br from-purple-500/5 to-purple-600/5"></div>
              <div class="absolute top-0 right-0 w-32 h-32 bg-gradient-to-br from-purple-400/10 to-purple-600/10 rounded-full blur-2xl"></div>
              
              <div class="relative z-10 text-center">
                <div class="relative inline-block mb-6">
                  <div class="absolute inset-0 bg-gradient-to-r from-purple-500 to-purple-600 rounded-2xl blur-lg opacity-50 group-hover:opacity-75 transition-opacity duration-300"></div>
                  <div class="relative bg-gradient-to-r from-purple-500 to-purple-600 p-6 rounded-2xl shadow-xl group-hover:scale-105 transition-transform duration-300">
                    <svg class="h-12 w-12 text-white" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                        d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z" />
                    </svg>
                  </div>
                </div>
                <h3 class="text-3xl font-bold text-gray-900 mb-4">Praktijklessen</h3>
                <p class="text-gray-600 mb-6 leading-relaxed text-lg">
                  Oefen in echte verkeersomstandigheden.
                  Leer veilige rijtechnieken met onze ervaren instructeurs.
                </p>
                <ul class="text-left space-y-3 mb-8">
                  <li class="flex items-center text-gray-700 p-2 rounded-lg hover:bg-purple-50 transition-colors duration-200">
                    <div class="w-8 h-8 bg-green-100 rounded-full flex items-center justify-center mr-3">
                      <svg class="h-4 w-4 text-green-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                      </svg>
                    </div>
                    <span class="text-lg font-medium">Individuele Training</span>
                  </li>
                  <li class="flex items-center text-gray-700 p-2 rounded-lg hover:bg-purple-50 transition-colors duration-200">
                    <div class="w-8 h-8 bg-green-100 rounded-full flex items-center justify-center mr-3">
                      <svg class="h-4 w-4 text-green-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                      </svg>
                    </div>
                    <span class="text-lg font-medium">Moderne Voertuigen</span>
                  </li>
                  <li class="flex items-center text-gray-700 p-2 rounded-lg hover:bg-purple-50 transition-colors duration-200">
                    <div class="w-8 h-8 bg-green-100 rounded-full flex items-center justify-center mr-3">
                      <svg class="h-4 w-4 text-green-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                      </svg>
                    </div>
                    <span class="text-lg font-medium">Verkeerstraining</span>
                  </li>
                  <li class="flex items-center text-gray-700 p-2 rounded-lg hover:bg-purple-50 transition-colors duration-200">
                    <div class="w-8 h-8 bg-green-100 rounded-full flex items-center justify-center mr-3">
                      <svg class="h-4 w-4 text-green-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                      </svg>
                    </div>
                    <span class="text-lg font-medium">Flexibel Programma</span>
                  </li>
                </ul>
                <button class="group relative w-full bg-gradient-to-r from-purple-600 to-purple-700 text-white py-4 rounded-2xl font-bold text-lg shadow-lg hover:shadow-xl transition-all duration-300 hover:scale-105 overflow-hidden">
                  <span class="relative z-10 flex items-center justify-center">
                    Bekijk Details
                    <svg class="w-5 h-5 ml-2 group-hover:translate-x-1 transition-transform duration-300" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 7l5 5m0 0l-5 5m5-5H6" />
                    </svg>
                  </span>
                  <div class="absolute inset-0 bg-gradient-to-r from-purple-700 to-purple-800 opacity-0 group-hover:opacity-100 transition-opacity duration-300"></div>
                </button>
              </div>
            </div>
          </swiper-slide>

          <!-- Examen Voorbereiding -->
          <swiper-slide>
            <div class="relative bg-white/80 backdrop-blur-md rounded-3xl shadow-xl hover:shadow-2xl transition-all duration-300 p-8 group h-full border border-white/20 overflow-hidden">
              <!-- Background Gradient -->
              <div class="absolute inset-0 bg-gradient-to-br from-yellow-500/5 to-yellow-600/5"></div>
              <div class="absolute top-0 right-0 w-32 h-32 bg-gradient-to-br from-yellow-400/10 to-yellow-600/10 rounded-full blur-2xl"></div>
              
              <div class="relative z-10 text-center">
                <div class="relative inline-block mb-6">
                  <div class="absolute inset-0 bg-gradient-to-r from-yellow-500 to-yellow-600 rounded-2xl blur-lg opacity-50 group-hover:opacity-75 transition-opacity duration-300"></div>
                  <div class="relative bg-gradient-to-r from-yellow-500 to-yellow-600 p-6 rounded-2xl shadow-xl group-hover:scale-105 transition-transform duration-300">
                    <svg class="h-12 w-12 text-white" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                        d="M9 5H7a2 2 0 00-2 2v10a2 2 0 002 2h8a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2" />
                    </svg>
                  </div>
                </div>
                <h3 class="text-3xl font-bold text-gray-900 mb-4">Examen Voorbereiding</h3>
                <p class="text-gray-600 mb-6 leading-relaxed text-lg">
                  Onze speciale programma's voor examenvoorbereiding.
                  Bereid je voor op examens met een hoog slagingspercentage.
                </p>
                <ul class="text-left space-y-3 mb-8">
                  <li class="flex items-center text-gray-700 p-2 rounded-lg hover:bg-yellow-50 transition-colors duration-200">
                    <div class="w-8 h-8 bg-green-100 rounded-full flex items-center justify-center mr-3">
                      <svg class="h-4 w-4 text-green-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                      </svg>
                    </div>
                    <span class="text-lg font-medium">Proefexamens</span>
                  </li>
                  <li class="flex items-center text-gray-700 p-2 rounded-lg hover:bg-yellow-50 transition-colors duration-200">
                    <div class="w-8 h-8 bg-green-100 rounded-full flex items-center justify-center mr-3">
                      <svg class="h-4 w-4 text-green-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                      </svg>
                    </div>
                    <span class="text-lg font-medium">Individuele Coaching</span>
                  </li>
                  <li class="flex items-center text-gray-700 p-2 rounded-lg hover:bg-yellow-50 transition-colors duration-200">
                    <div class="w-8 h-8 bg-green-100 rounded-full flex items-center justify-center mr-3">
                      <svg class="h-4 w-4 text-green-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                      </svg>
                    </div>
                    <span class="text-lg font-medium">Strategie Training</span>
                  </li>
                  <li class="flex items-center text-gray-700 p-2 rounded-lg hover:bg-yellow-50 transition-colors duration-200">
                    <div class="w-8 h-8 bg-green-100 rounded-full flex items-center justify-center mr-3">
                      <svg class="h-4 w-4 text-green-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                      </svg>
                    </div>
                    <span class="text-lg font-medium">95% Slagingspercentage</span>
                  </li>
                </ul>
                <button class="group relative w-full bg-gradient-to-r from-yellow-600 to-yellow-700 text-white py-4 rounded-2xl font-bold text-lg shadow-lg hover:shadow-xl transition-all duration-300 hover:scale-105 overflow-hidden">
                  <span class="relative z-10 flex items-center justify-center">
                    Bekijk Details
                    <svg class="w-5 h-5 ml-2 group-hover:translate-x-1 transition-transform duration-300" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 7l5 5m0 0l-5 5m5-5H6" />
                    </svg>
                  </span>
                  <div class="absolute inset-0 bg-gradient-to-r from-yellow-700 to-yellow-800 opacity-0 group-hover:opacity-100 transition-opacity duration-300"></div>
                </button>
              </div>
            </div>
          </swiper-slide>

          <!-- Privélessen -->
          <swiper-slide>
            <div class="relative bg-white/80 backdrop-blur-md rounded-3xl shadow-xl hover:shadow-2xl transition-all duration-300 p-8 group h-full border border-white/20 overflow-hidden">
              <!-- Background Gradient -->
              <div class="absolute inset-0 bg-gradient-to-br from-indigo-500/5 to-indigo-600/5"></div>
              <div class="absolute top-0 right-0 w-32 h-32 bg-gradient-to-br from-indigo-400/10 to-indigo-600/10 rounded-full blur-2xl"></div>
              
              <div class="relative z-10 text-center">
                <div class="relative inline-block mb-6">
                  <div class="absolute inset-0 bg-gradient-to-r from-indigo-500 to-indigo-600 rounded-2xl blur-lg opacity-50 group-hover:opacity-75 transition-opacity duration-300"></div>
                  <div class="relative bg-gradient-to-r from-indigo-500 to-indigo-600 p-6 rounded-2xl shadow-xl group-hover:scale-105 transition-transform duration-300">
                    <svg class="h-12 w-12 text-white" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                        d="M12 4.354a4 4 0 110 5.292M15 21H3v-1a6 6 0 0112 0v1zm0 0h6v-1a6 6 0 00-9-5.197m13.5-9a2.5 2.5 0 11-5 0 2.5 2.5 0 015 0z" />
                    </svg>
                  </div>
                </div>
                <h3 class="text-3xl font-bold text-gray-900 mb-4">Privélessen</h3>
                <p class="text-gray-600 mb-6 leading-relaxed text-lg">
                  Aangepaste lesprogramma's volgens uw persoonlijke behoeften.
                  Ervaar een leertraject dat past bij uw tempo.
                </p>
                <ul class="text-left space-y-3 mb-8">
                  <li class="flex items-center text-gray-700 p-2 rounded-lg hover:bg-indigo-50 transition-colors duration-200">
                    <div class="w-8 h-8 bg-green-100 rounded-full flex items-center justify-center mr-3">
                      <svg class="h-4 w-4 text-green-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                      </svg>
                    </div>
                    <span class="text-lg font-medium">Persoonlijk Programma</span>
                  </li>
                  <li class="flex items-center text-gray-700 p-2 rounded-lg hover:bg-indigo-50 transition-colors duration-200">
                    <div class="w-8 h-8 bg-green-100 rounded-full flex items-center justify-center mr-3">
                      <svg class="h-4 w-4 text-green-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                      </svg>
                    </div>
                    <span class="text-lg font-medium">Flexibele Tijden</span>
                  </li>
                  <li class="flex items-center text-gray-700 p-2 rounded-lg hover:bg-indigo-50 transition-colors duration-200">
                    <div class="w-8 h-8 bg-green-100 rounded-full flex items-center justify-center mr-3">
                      <svg class="h-4 w-4 text-green-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                      </svg>
                    </div>
                    <span class="text-lg font-medium">Individuele Training</span>
                  </li>
                  <li class="flex items-center text-gray-700 p-2 rounded-lg hover:bg-indigo-50 transition-colors duration-200">
                    <div class="w-8 h-8 bg-green-100 rounded-full flex items-center justify-center mr-3">
                      <svg class="h-4 w-4 text-green-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                      </svg>
                    </div>
                    <span class="text-lg font-medium">Snelle Voortgang</span>
                  </li>
                </ul>
                <button class="group relative w-full bg-gradient-to-r from-indigo-600 to-indigo-700 text-white py-4 rounded-2xl font-bold text-lg shadow-lg hover:shadow-xl transition-all duration-300 hover:scale-105 overflow-hidden">
                  <span class="relative z-10 flex items-center justify-center">
                    Bekijk Details
                    <svg class="w-5 h-5 ml-2 group-hover:translate-x-1 transition-transform duration-300" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 7l5 5m0 0l-5 5m5-5H6" />
                    </svg>
                  </span>
                  <div class="absolute inset-0 bg-gradient-to-r from-indigo-700 to-indigo-800 opacity-0 group-hover:opacity-100 transition-opacity duration-300"></div>
                </button>
              </div>
            </div>
          </swiper-slide>
        </swiper>
      </div>
    </div>
  </section>
</template>

<script setup>
import { Swiper, SwiperSlide } from 'swiper/vue'
import { Navigation, Pagination, Autoplay } from 'swiper/modules'
import 'swiper/css'
import 'swiper/css/navigation'
import 'swiper/css/pagination'
import 'swiper/css/autoplay'

const modules = [Navigation, Pagination, Autoplay]
</script>

<style scoped>
.services-swiper {
  padding-bottom: 50px;
}

:deep(.swiper-pagination-bullet) {
  background-color: #3B82F6;
}

:deep(.swiper-pagination-bullet-active) {
  background-color: #1D4ED8;
}

:deep(.swiper-button-next),
:deep(.swiper-button-prev) {
  color: #3B82F6;
}

:deep(.swiper-button-next:after),
:deep(.swiper-button-prev:after) {
  font-size: 24px;
}
</style>