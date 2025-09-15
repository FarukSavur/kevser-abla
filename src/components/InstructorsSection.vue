<template>
  <section id="instructors" class="py-20 bg-gradient-to-br from-slate-900 via-blue-900 to-indigo-900 relative overflow-hidden">
    <!-- Background Elements -->
    <div class="absolute inset-0">
      <div class="absolute top-1/4 left-1/4 w-96 h-96 bg-orange-500/10 rounded-full blur-3xl animate-pulse"></div>
      <div class="absolute bottom-1/4 right-1/4 w-80 h-80 bg-blue-500/10 rounded-full blur-3xl animate-pulse delay-1000"></div>
      <div class="absolute top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2 w-64 h-64 bg-purple-500/10 rounded-full blur-3xl animate-pulse delay-500"></div>
      
      <!-- Floating Elements -->
      <div class="absolute top-20 left-20 w-4 h-4 bg-orange-400/30 rounded-full animate-bounce delay-300"></div>
      <div class="absolute top-40 right-32 w-6 h-6 bg-blue-400/40 rounded-full animate-bounce delay-700"></div>
      <div class="absolute bottom-32 left-1/3 w-3 h-3 bg-purple-300/50 rounded-full animate-bounce delay-1000"></div>
      <div class="absolute bottom-20 right-20 w-5 h-5 bg-orange-300/20 rounded-full animate-bounce delay-500"></div>
    </div>

    <div class="relative max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <!-- Section Header -->
      <div class="text-center mb-16">
        <div class="inline-flex items-center px-4 py-2 bg-white/10 backdrop-blur-sm border border-white/20 rounded-full text-sm font-medium text-white/90 mb-6">
          <svg class="w-4 h-4 mr-2 text-orange-400" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 4.354a4 4 0 110 5.292M15 21H3v-1a6 6 0 0112 0v1zm0 0h6v-1a6 6 0 00-9-5.197m13.5-9a2.5 2.5 0 11-5 0 2.5 2.5 0 015 0z" />
          </svg>
          Onze Instructeurs
        </div>
        <h2 class="text-5xl md:text-6xl font-bold mb-6">
          <span class="bg-gradient-to-r from-white via-orange-200 to-orange-400 bg-clip-text text-transparent">
            Onze Instructeurs
          </span>
        </h2>
        <p class="text-xl text-gray-300 max-w-3xl mx-auto leading-relaxed">
          Word een veilige bestuurder met onze ervaren en deskundige instructeurs.
          Maak kennis met onze instructeurs die elk expert zijn in hun vakgebied.
        </p>
      </div>

      <!-- Instructors Swiper -->
      <div class="relative">
        <swiper :modules="modules" :slides-per-view="1" :space-between="30" :pagination="{ clickable: true }"
        :loop="true"
          :navigation="true" :breakpoints="{
            640: {
              slidesPerView: 2,
              spaceBetween: 20,
            },
            1024: {
              slidesPerView: 3,
              spaceBetween: 30,
            },
          }" class="instructors-swiper">
          <!-- Instructors Loop -->
          <swiper-slide v-for="instructor in instructors" :key="instructor.id">
            <div class="relative bg-white/10 backdrop-blur-md rounded-3xl shadow-2xl hover:shadow-2xl transition-all duration-300 overflow-hidden border border-white/20 group">
              <!-- Background Gradient -->
              <div class="absolute inset-0 bg-gradient-to-br from-slate-500/5 to-slate-600/5"></div>
              <div class="absolute top-0 right-0 w-32 h-32 bg-gradient-to-br from-slate-400/10 to-slate-600/10 rounded-full blur-2xl"></div>
              
              <div class="relative">
                <div class="h-64 flex items-center justify-center relative overflow-hidden" :class="`bg-gradient-to-br ${instructor.gradient}`">
                  <div class="absolute inset-0 bg-gradient-to-br from-black/20 to-black/40"></div>
                  <div class="relative w-32 h-32 bg-white/90 backdrop-blur-sm rounded-full flex items-center justify-center shadow-2xl group-hover:scale-105 transition-transform duration-300">
                    <svg class="h-16 w-16" :class="`text-${instructor.color}-600`" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                        d="M16 7a4 4 0 11-8 0 4 4 0 018 0zM12 14a7 7 0 00-7 7h14a7 7 0 00-7-7z" />
                    </svg>
                  </div>
                  <!-- Floating Elements -->
                  <div class="absolute top-4 left-4 w-3 h-3 bg-white/30 rounded-full animate-bounce delay-300"></div>
                  <div class="absolute bottom-4 right-4 w-2 h-2 bg-white/40 rounded-full animate-bounce delay-700"></div>
                </div>
                <div class="absolute top-4 right-4 bg-gradient-to-r from-orange-500 to-orange-600 text-white px-4 py-2 rounded-full text-sm font-bold shadow-lg">
                  {{ instructor.experience }}
                </div>
              </div>
              <div class="relative z-10 p-6">
                <h3 class="text-2xl font-bold text-white mb-2">{{ instructor.name }}</h3>
                <p class="font-semibold mb-4" :class="`text-${instructor.color}-400`">{{ instructor.title }}</p>
                <p class="text-gray-300 mb-4 leading-relaxed">
                  {{ instructor.description }}
                </p>
                <div class="flex items-center justify-between">
                  <div class="flex items-center">
                    <div class="flex text-yellow-400">
                      <svg v-for="i in 5" :key="i" class="h-5 w-5" fill="currentColor" viewBox="0 0 20 20">
                        <path
                          d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z" />
                      </svg>
                    </div>
                    <span class="ml-2 text-gray-300 font-semibold">{{ instructor.rating }}/5</span>
                  </div>
                  <span class="text-sm text-gray-400 font-medium">{{ instructor.students }}</span>
                </div>
              </div>
            </div>
          </swiper-slide>
        </swiper>
      </div>

      <!-- Stats Section -->
      <div class="mt-16 relative bg-gradient-to-br from-slate-900 via-blue-900 to-indigo-900 rounded-3xl p-8 shadow-2xl overflow-hidden">
        <!-- Background Elements -->
        <div class="absolute inset-0">
          <div class="absolute top-1/4 left-1/4 w-96 h-96 bg-orange-500/10 rounded-full blur-3xl animate-pulse"></div>
          <div class="absolute bottom-1/4 right-1/4 w-80 h-80 bg-blue-500/10 rounded-full blur-3xl animate-pulse delay-1000"></div>
        </div>
        
        <div class="relative z-10 grid grid-cols-1 md:grid-cols-4 gap-8">
          <div class="text-center bg-white/10 backdrop-blur-md rounded-2xl p-6 hover:bg-white/20 transition-all duration-300 border border-white/20 group">
            <div class="text-5xl font-bold bg-gradient-to-r from-orange-400 to-orange-600 bg-clip-text text-transparent mb-3 group-hover:scale-110 transition-transform duration-300">15+</div>
            <div class="text-white text-lg font-medium">Jaar Ervaring</div>
            <div class="w-12 h-1 bg-gradient-to-r from-orange-400 to-orange-600 mx-auto mt-3 rounded-full"></div>
          </div>
          <div class="text-center bg-white/10 backdrop-blur-md rounded-2xl p-6 hover:bg-white/20 transition-all duration-300 border border-white/20 group">
            <div class="text-5xl font-bold bg-gradient-to-r from-blue-400 to-blue-600 bg-clip-text text-transparent mb-3 group-hover:scale-110 transition-transform duration-300">2000+</div>
            <div class="text-white text-lg font-medium">Geslaagde Leerlingen</div>
            <div class="w-12 h-1 bg-gradient-to-r from-blue-400 to-blue-600 mx-auto mt-3 rounded-full"></div>
          </div>
          <div class="text-center bg-white/10 backdrop-blur-md rounded-2xl p-6 hover:bg-white/20 transition-all duration-300 border border-white/20 group">
            <div class="text-5xl font-bold bg-gradient-to-r from-green-400 to-green-600 bg-clip-text text-transparent mb-3 group-hover:scale-110 transition-transform duration-300">95%</div>
            <div class="text-white text-lg font-medium">Slagingspercentage</div>
            <div class="w-12 h-1 bg-gradient-to-r from-green-400 to-green-600 mx-auto mt-3 rounded-full"></div>
          </div>
          <div class="text-center bg-white/10 backdrop-blur-md rounded-2xl p-6 hover:bg-white/20 transition-all duration-300 border border-white/20 group">
            <div class="text-5xl font-bold bg-gradient-to-r from-purple-400 to-purple-600 bg-clip-text text-transparent mb-3 group-hover:scale-110 transition-transform duration-300">4.8</div>
            <div class="text-white text-lg font-medium">Gemiddelde Score</div>
            <div class="w-12 h-1 bg-gradient-to-r from-purple-400 to-purple-600 mx-auto mt-3 rounded-full"></div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { Swiper, SwiperSlide } from 'swiper/vue'
import { Navigation, Pagination } from 'swiper/modules'
import 'swiper/css'
import 'swiper/css/navigation'
import 'swiper/css/pagination'

const modules = [Navigation, Pagination]

// Instructors verileri
const instructors = [
  {
    id: 1,
    name: "Kevser",
    title: "Hoofdinstructeur",
    description: "Onze hoofdinstructeur met 15 jaar ervaring in Nederland. Expert in B-rijbewijs.",
    experience: "15 Jaar Ervaring",
    rating: 4.9,
    students: "500+ Leerlingen",
    color: "blue",
    gradient: "from-blue-500 to-blue-600"
  },
  {
    id: 2,
    name: "Ahmet",
    title: "Motor Instructeur",
    description: "Onze expert instructeur voor A-rijbewijs. Ervaren in motorveiligheid en -technieken.",
    experience: "12 Jaar Ervaring",
    rating: 4.8,
    students: "300+ Leerlingen",
    color: "red",
    gradient: "from-red-500 to-red-600"
  },
  {
    id: 3,
    name: "Fatma",
    title: "Theorie Instructeur",
    description: "Expert in verkeersregels en veiligheid. Ervaren instructeur die geduldig is met leerlingen.",
    experience: "10 Jaar Ervaring",
    rating: 4.9,
    students: "400+ Leerlingen",
    color: "green",
    gradient: "from-green-500 to-green-600"
  },
  {
    id: 4,
    name: "Mehmet",
    title: "Praktijk Instructeur",
    description: "Expert in praktische rijtechnieken. Bekend om zijn vertrouwenwekkende benadering van leerlingen.",
    experience: "8 Jaar Ervaring",
    rating: 4.7,
    students: "250+ Leerlingen",
    color: "purple",
    gradient: "from-purple-500 to-purple-600"
  }
]
</script>

<style scoped>
.instructors-swiper {
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
