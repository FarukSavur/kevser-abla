<template>
  <section id="services"
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
              d="M19 21V5a2 2 0 00-2-2H7a2 2 0 00-2 2v16m14 0h2m-2 0h-5m-9 0H3m2 0h5M9 7h1m-1 4h1m4-4h1m-1 4h1m-5 10v-5a1 1 0 011-1h2a1 1 0 011 1v5m-4 0h4" />
          </svg>
          Onze Diensten
        </div>
        <h2 class="text-5xl md:text-6xl font-bold mb-6">
          <span class="bg-gradient-to-r from-white via-orange-200 to-orange-400 bg-clip-text text-transparent">
            Onze Diensten
          </span>
        </h2>
        <p class="text-xl text-gray-300 max-w-3xl mx-auto leading-relaxed">
          Voor het behalen van je autorijbewijs en motorrijbewijs in Nederland bieden wij
          alle diensten aan met onze professionele instructeurs.
        </p>
      </div>

      <!-- Services Swiper -->
      <div class="relative pt-8">
        <swiper :modules="modules" :autoplay="{
          delay: 4000,
          disableOnInteraction: false,
        }" :loop="true" :slides-per-view="1" :space-between="30" :grab-cursor="true"
          :pagination="{ clickable: true }" :navigation="true" :breakpoints="{
            640: {
              slidesPerView: 2,
              spaceBetween: 20,
            },
            1024: {
              slidesPerView: 3,
              spaceBetween: 30,
            },
          }" class="services-swiper">
          <!-- Services Loop -->
          <swiper-slide v-for="service in services" :key="service.id">
            <div
              class="relative bg-white/10 backdrop-blur-md rounded-3xl shadow-2xl hover:shadow-2xl transition-all duration-300 p-8 group h-full border border-white/20 overflow-hidden">
              <!-- Background Gradient -->
              <div class="absolute inset-0 bg-gradient-to-br from-slate-500/5 to-slate-600/5"></div>
              <div
                class="absolute top-0 right-0 w-32 h-32 bg-gradient-to-br from-slate-400/10 to-slate-600/10 rounded-full blur-2xl">
              </div>

              <div class="relative z-10 text-center">
                <div class="relative inline-block mb-6">
                  <div
                    class="absolute inset-0 rounded-2xl blur-lg opacity-50 group-hover:opacity-75 transition-opacity duration-300"
                    :class="`bg-gradient-to-r ${service.gradient}`"></div>
                  <div
                    class="relative p-6 rounded-2xl shadow-xl group-hover:scale-105 transition-transform duration-300"
                    :class="`bg-gradient-to-r ${service.gradient}`">
                    <svg class="h-12 w-12 text-white" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" :d="service.icon" />
                    </svg>
                  </div>
                </div>
                <h3 class="text-3xl font-bold text-white mb-4">{{ service.title }}</h3>
                <p class="text-gray-300 mb-6 leading-relaxed text-lg">
                  {{ service.description }}
                </p>
                <ul class="text-left space-y-3 mb-8">
                  <li v-for="feature in service.features" :key="feature"
                    class="flex items-center text-gray-300 p-2 rounded-lg hover:bg-white/5 transition-colors duration-200">
                    <div class="w-8 h-8 bg-green-500/20 rounded-full flex items-center justify-center mr-3">
                      <svg class="h-4 w-4 text-green-400" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                      </svg>
                    </div>
                    <span class="text-lg font-medium">{{ feature }}</span>
                  </li>
                </ul>
                <button
                  class="group relative w-full text-white py-4 rounded-2xl font-bold text-lg shadow-lg hover:shadow-xl transition-all duration-300 hover:scale-105 overflow-hidden"
                  :class="`bg-gradient-to-r ${service.gradient}`">
                  <span class="relative z-10 flex items-center justify-center">
                    Bekijk Details
                    <svg class="w-5 h-5 ml-2 group-hover:translate-x-1 transition-transform duration-300" fill="none"
                      viewBox="0 0 24 24" stroke="currentColor">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                        d="M13 7l5 5m0 0l-5 5m5-5H6" />
                    </svg>
                  </span>
                  <div class="absolute inset-0 opacity-0 group-hover:opacity-100 transition-opacity duration-300"
                    :class="`bg-gradient-to-r from-${service.color}-700 to-${service.color}-800`"></div>
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

// Services verileri
const services = [
  {
    id: 1,
    title: "B Rijbewijs",
    description: "Krijg alle benodigde theoretische en praktische training voor autorijden. Word een veilige bestuurder met onze ervaren instructeurs.",
    color: "blue",
    gradient: "from-blue-500 to-blue-600",
    icon: "M8 7h12m0 0l-4-4m4 4l-4 4m0 6H4m0 0l4 4m-4-4l4-4",
    features: [
      "Theorielessen",
      "Praktijklessen",
      "Examen Voorbereiding",
      "Flexibele Tijden"
    ]
  },
  {
    id: 2,
    title: "A Rijbewijs",
    description: "Ons speciale opleidingsprogramma voor motorrijden. Krijg professionele ondersteuning om een veilige motorrijder te worden.",
    color: "red",
    gradient: "from-red-500 to-red-600",
    icon: "M13 10V3L4 14h7v7l9-11h-7z",
    features: [
      "Motor Theorie",
      "Praktijk Training",
      "Veiligheidstraining",
      "Moderne Motoren"
    ]
  },
  {
    id: 3,
    title: "Theorielessen",
    description: "Krijg uitgebreide theoretische training over verkeersregels, veiligheidsmaatregelen en bestuurdersgedrag.",
    color: "green",
    gradient: "from-green-500 to-green-600",
    icon: "M12 6.253v13m0-13C10.832 5.477 9.246 5 7.5 5S4.168 5.477 3 6.253v13C4.168 18.477 5.754 18 7.5 18s3.332.477 4.5 1.253m0-13C13.168 5.477 14.754 5 16.5 5c1.746 0 3.332.477 4.5 1.253v13C19.832 18.477 18.246 18 16.5 18c-1.746 0-3.332.477-4.5 1.253",
    features: [
      "Verkeersregels",
      "Veiligheidstraining",
      "Eerste Hulp",
      "Online Lessen"
    ]
  },
  {
    id: 4,
    title: "Praktijklessen",
    description: "Oefen in echte verkeersomstandigheden. Leer veilige rijtechnieken met onze ervaren instructeurs.",
    color: "purple",
    gradient: "from-purple-500 to-purple-600",
    icon: "M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z",
    features: [
      "Individuele Training",
      "Moderne Voertuigen",
      "Verkeerstraining",
      "Flexibel Programma"
    ]
  },
  {
    id: 5,
    title: "Examen",
    description: "Onze speciale programma's voor. Bereid speciale je voor op examens met een hoog je voor op slagingspercentage.",
    color: "yellow",
    gradient: "from-yellow-500 to-yellow-600",
    icon: "M9 5H7a2 2 0 00-2 2v10a2 2 0 002 2h8a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2",
    features: [
      "Proefexamens",
      "Individuele Coaching",
      "Strategie Training",
      "95% Slagingspercentage"
    ]
  },
  {
    id: 6,
    title: "Privélessen",
    description: "Aangepaste lesprogramma's volgens uw persoonlijke behoeften. Ervaar een volgens leertraject dat past bij uw tempo.",
    color: "indigo",
    gradient: "from-indigo-500 to-indigo-600",
    icon: "M12 4.354a4 4 0 110 5.292M15 21H3v-1a6 6 0 0112 0v1zm0 0h6v-1a6 6 0 00-9-5.197m13.5-9a2.5 2.5 0 11-5 0 2.5 2.5 0 015 0z",
    features: [
      "Persoonlijk Programma",
      "Flexibele Tijden",
      "Individuele Training",
      "Snelle Voortgang"
    ]
  }
]
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
  width: 40px;
  height: 40px;
  background: rgba(255, 255, 255, 0.2);
  backdrop-filter: blur(8px);
  border-radius: 50%;
  color: rgba(255, 255, 255, 0.8);
  transition: all 0.3s ease;
  border: none;
  opacity: 0.8;
}

:deep(.swiper-button-next:hover),
:deep(.swiper-button-prev:hover) {
  background: rgba(255, 255, 255, 0.3);
  color: white;
  opacity: 1;
  transform: scale(1.05);
}

:deep(.swiper-button-next:after),
:deep(.swiper-button-prev:after) {
  font-size: 16px;
  font-weight: bold;
}

/* Responsive adjustments */
@media (max-width: 768px) {

  :deep(.swiper-button-next),
  :deep(.swiper-button-prev) {
    width: 36px;
    height: 36px;
  }

  :deep(.swiper-button-next:after),
  :deep(.swiper-button-prev:after) {
    font-size: 14px;
  }
}
</style>