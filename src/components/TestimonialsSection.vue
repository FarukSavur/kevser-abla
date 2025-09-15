<template>
  <section id="testimonials" class="py-20 bg-gradient-to-br from-slate-900 via-blue-900 to-indigo-900 relative overflow-hidden">
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
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 12h.01M12 12h.01M16 12h.01M21 12c0 4.418-4.03 8-9 8a9.863 9.863 0 01-4.255-.949L3 20l1.395-3.72C3.512 15.042 3 13.574 3 12c0-4.418 4.03-8 9-8s9 3.582 9 8z" />
          </svg>
          Leerling Beoordelingen
        </div>
        <h2 class="text-5xl md:text-6xl font-bold mb-6">
          <span class="bg-gradient-to-r from-white via-orange-200 to-orange-400 bg-clip-text text-transparent">
            Leerling Beoordelingen
          </span>
        </h2>
        <p class="text-xl text-gray-300 max-w-3xl mx-auto leading-relaxed">
          Lees de ervaringen van onze succesvolle leerlingen. 
          Hun verhalen zijn een voorbode van jouw succes.
        </p>
      </div>

      <!-- Testimonials Swiper with Coverflow Effect -->
      <div class="relative">
        <swiper
          :modules="modules"
          :autoplay="{
            delay: 2500,
            disableOnInteraction: false,
          }"
          :mousewheel="true"
          :loop="true"
          :slides-per-view="1"
          :space-between="30"
          :effect="'coverflow'"
          :grab-cursor="true"
          :centered-slides="true"
          :coverflow-effect="{
            rotate: 30,
            stretch: 0,
            depth: 100,
            modifier: 1,
            slideShadows: false,
          }"
          :pagination="{ clickable: true }"
          :navigation="true"
          :breakpoints="{
            640: {
              slidesPerView: 2,
            },
            1024: {
              slidesPerView: 3,
            },
          }"
          class="testimonials-swiper"
        >
          <!-- Testimonials Loop -->
          <swiper-slide v-for="testimonial in testimonials" :key="testimonial.id">
            <div class="relative bg-white/10 backdrop-blur-md rounded-3xl shadow-2xl p-8 hover:shadow-2xl transition-all duration-300 h-full border border-white/20 overflow-hidden group">
              <!-- Background Gradient -->
              <div class="absolute inset-0 bg-gradient-to-br from-slate-500/5 to-slate-600/5"></div>
              <div class="absolute top-0 right-0 w-32 h-32 bg-gradient-to-br from-slate-400/10 to-slate-600/10 rounded-full blur-2xl"></div>
              
              <div class="relative z-10">
                <div class="flex items-center mb-6">
                  <div class="relative">
                    <div class="absolute inset-0 bg-gradient-to-r rounded-full blur-lg opacity-50 group-hover:opacity-75 transition-opacity duration-300" :class="`from-${testimonial.color}-500 to-${testimonial.color}-600`"></div>
                    <div class="relative w-16 h-16 rounded-full flex items-center justify-center shadow-xl group-hover:scale-105 transition-transform duration-300" :class="`bg-gradient-to-r from-${testimonial.color}-500 to-${testimonial.color}-600`">
                      <svg class="h-8 w-8 text-white" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M16 7a4 4 0 11-8 0 4 4 0 018 0zM12 14a7 7 0 00-7 7h14a7 7 0 00-7-7z" />
                      </svg>
                    </div>
                  </div>
                  <div class="ml-4">
                    <h4 class="text-lg font-bold text-white">{{ testimonial.name }}</h4>
                    <p class="text-gray-300">{{ testimonial.license }}</p>
                  </div>
                </div>
                <div class="flex text-yellow-400 mb-4">
                  <svg v-for="i in 5" :key="i" class="h-5 w-5" fill="currentColor" viewBox="0 0 20 20">
                    <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z" />
                  </svg>
                </div>
                <p class="text-gray-300 leading-relaxed">
                  "{{ testimonial.comment }}"
                </p>
              </div>
            </div>
          </swiper-slide>
        </swiper>
      </div>

      <!-- CTA Section -->
      <div class="mt-16 text-center">
        <div class="bg-blue-600 rounded-2xl p-8 text-white">
          <h3 class="text-3xl font-bold mb-4">Word ook een van onze Succesvolle Leerlingen!</h3>
          <p class="text-xl text-blue-100 mb-6">
            Krijg direct gratis advies en ontdek het programma dat bij jou past.
          </p>
          <button class="bg-yellow-400 text-blue-900 px-8 py-4 rounded-lg font-bold text-lg hover:bg-yellow-300 transition-colors">
            Gratis Advies
          </button>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { Swiper, SwiperSlide } from 'swiper/vue'
import { Navigation, Pagination, EffectCoverflow, Autoplay } from 'swiper/modules'
import 'swiper/css'
import 'swiper/css/navigation'
import 'swiper/css/pagination'
import 'swiper/css/effect-coverflow'
import 'swiper/css/autoplay'

const modules = [Navigation, Pagination, EffectCoverflow, Autoplay]

// Testimonial verileri
const testimonials = [
  {
    id: 1,
    name: "Ayşe Yılmaz",
    license: "B Rijbewijs",
    comment: "Werken met Kevser Abla was een geweldige ervaring. Dankzij haar geduldige en begripvolle aanpak heb ik mijn angsten overwonnen en succesvol mijn rijbewijs gehaald. Ik raad het iedereen aan!",
    color: "blue",
    gradient: "from-blue-500 to-blue-600"
  },
  {
    id: 2,
    name: "Mehmet Kaya",
    license: "A Rijbewijs",
    comment: "Ik wilde mijn A-rijbewijs halen maar was erg bang. Dankzij de professionele aanpak van Ahmet heb ik veilig leren motorrijden. Bedankt!",
    color: "red",
    gradient: "from-red-500 to-red-600"
  },
  {
    id: 3,
    name: "Fatma Demir",
    license: "B Rijbewijs",
    comment: "Dankzij flexibele tijden en individuele training kon ik mijn rijlessen gemakkelijk combineren met mijn werk. Ik ben erg tevreden, ik raad het iedereen aan.",
    color: "green",
    gradient: "from-green-500 to-green-600"
  },
  {
    id: 4,
    name: "Ali Özkan",
    license: "A Rijbewijs",
    comment: "Training met moderne motoren maakt echt het verschil. De instructeurs zijn zeer professioneel en leren veilige rijtechnieken heel goed aan.",
    color: "purple",
    gradient: "from-purple-500 to-purple-600"
  },
  {
    id: 5,
    name: "Zeynep Arslan",
    license: "B Rijbewijs",
    comment: "Ze hebben veel geholpen met examenvoorbereiding. Dankzij proefexamens en individuele coaching ben ik in de eerste keer geslaagd. Heel erg bedankt!",
    color: "yellow",
    gradient: "from-yellow-500 to-yellow-600"
  },
  {
    id: 6,
    name: "Can Yıldız",
    license: "A Rijbewijs",
    comment: "Ik dacht dat het halen van een rijbewijs in Nederland moeilijk was, maar met de juiste instructeur is het heel makkelijk. Dankzij Kevser Abla's cursus ben ik geslaagd voor zowel theorie als praktijk.",
    color: "indigo",
    gradient: "from-indigo-500 to-indigo-600"
  }
]
</script>

<style scoped>
.testimonials-swiper {
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

:deep(.swiper-slide-shadow-coverflow) {
  background: linear-gradient(45deg, rgba(0, 0, 0, 0.1), rgba(0, 0, 0, 0.2));
}
</style>