<template>
  <section id="instructors" class="py-20 bg-white">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <!-- Section Header -->
      <div class="text-center mb-16">
        <h2 class="text-4xl md:text-5xl font-bold text-gray-900 mb-6">
          Eğitmenlerimiz
        </h2>
        <p class="text-xl text-gray-600 max-w-3xl mx-auto">
          Deneyimli ve uzman eğitmenlerimizle güvenli sürücü olun. 
          Her biri kendi alanında uzman olan eğitmenlerimizle tanışın.
        </p>
      </div>

      <!-- Instructors Swiper -->
      <div class="relative">
        <swiper
          :modules="modules"
          :slides-per-view="1"
          :space-between="30"
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
          class="instructors-swiper"
        >
          <!-- Instructor 1 -->
          <swiper-slide>
            <div class="bg-white rounded-2xl shadow-lg hover:shadow-xl transition-shadow duration-300 overflow-hidden">
              <div class="relative">
                <div class="h-64 bg-gradient-to-br from-blue-500 to-blue-600 flex items-center justify-center">
                  <div class="w-32 h-32 bg-white rounded-full flex items-center justify-center">
                    <svg class="h-16 w-16 text-blue-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M16 7a4 4 0 11-8 0 4 4 0 018 0zM12 14a7 7 0 00-7 7h14a7 7 0 00-7-7z" />
                    </svg>
                  </div>
                </div>
                <div class="absolute top-4 right-4 bg-yellow-400 text-yellow-900 px-3 py-1 rounded-full text-sm font-semibold">
                  15 Yıl Deneyim
                </div>
              </div>
              <div class="p-6">
                <h3 class="text-2xl font-bold text-gray-900 mb-2">Kevser Hanım</h3>
                <p class="text-blue-600 font-semibold mb-4">Baş Eğitmen</p>
                <p class="text-gray-600 mb-4 leading-relaxed">
                  Hollanda'da 15 yıllık deneyime sahip baş eğitmenimiz. 
                  B sınıfı ehliyet konusunda uzman.
                </p>
                <div class="flex items-center justify-between">
                  <div class="flex items-center">
                    <div class="flex text-yellow-400">
                      <svg v-for="i in 5" :key="i" class="h-5 w-5" fill="currentColor" viewBox="0 0 20 20">
                        <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z" />
                      </svg>
                    </div>
                    <span class="ml-2 text-gray-600">4.9/5</span>
                  </div>
                  <span class="text-sm text-gray-500">500+ Öğrenci</span>
                </div>
              </div>
            </div>
          </swiper-slide>

          <!-- Instructor 2 -->
          <swiper-slide>
            <div class="bg-white rounded-2xl shadow-lg hover:shadow-xl transition-shadow duration-300 overflow-hidden">
              <div class="relative">
                <div class="h-64 bg-gradient-to-br from-red-500 to-red-600 flex items-center justify-center">
                  <div class="w-32 h-32 bg-white rounded-full flex items-center justify-center">
                    <svg class="h-16 w-16 text-red-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M16 7a4 4 0 11-8 0 4 4 0 018 0zM12 14a7 7 0 00-7 7h14a7 7 0 00-7-7z" />
                    </svg>
                  </div>
                </div>
                <div class="absolute top-4 right-4 bg-yellow-400 text-yellow-900 px-3 py-1 rounded-full text-sm font-semibold">
                  12 Yıl Deneyim
                </div>
              </div>
              <div class="p-6">
                <h3 class="text-2xl font-bold text-gray-900 mb-2">Ahmet Bey</h3>
                <p class="text-red-600 font-semibold mb-4">Motor Eğitmeni</p>
                <p class="text-gray-600 mb-4 leading-relaxed">
                  A sınıfı ehliyet konusunda uzman eğitmenimiz. 
                  Motosiklet güvenliği ve teknikleri konusunda deneyimli.
                </p>
                <div class="flex items-center justify-between">
                  <div class="flex items-center">
                    <div class="flex text-yellow-400">
                      <svg v-for="i in 5" :key="i" class="h-5 w-5" fill="currentColor" viewBox="0 0 20 20">
                        <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z" />
                      </svg>
                    </div>
                    <span class="ml-2 text-gray-600">4.8/5</span>
                  </div>
                  <span class="text-sm text-gray-500">300+ Öğrenci</span>
                </div>
              </div>
            </div>
          </swiper-slide>

          <!-- Instructor 3 -->
          <swiper-slide>
            <div class="bg-white rounded-2xl shadow-lg hover:shadow-xl transition-shadow duration-300 overflow-hidden">
              <div class="relative">
                <div class="h-64 bg-gradient-to-br from-green-500 to-green-600 flex items-center justify-center">
                  <div class="w-32 h-32 bg-white rounded-full flex items-center justify-center">
                    <svg class="h-16 w-16 text-green-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M16 7a4 4 0 11-8 0 4 4 0 018 0zM12 14a7 7 0 00-7 7h14a7 7 0 00-7-7z" />
                    </svg>
                  </div>
                </div>
                <div class="absolute top-4 right-4 bg-yellow-400 text-yellow-900 px-3 py-1 rounded-full text-sm font-semibold">
                  10 Yıl Deneyim
                </div>
              </div>
              <div class="p-6">
                <h3 class="text-2xl font-bold text-gray-900 mb-2">Fatma Hanım</h3>
                <p class="text-green-600 font-semibold mb-4">Teorik Eğitmen</p>
                <p class="text-gray-600 mb-4 leading-relaxed">
                  Trafik kuralları ve güvenlik konularında uzman. 
                  Öğrencilerine sabırla yaklaşan deneyimli eğitmen.
                </p>
                <div class="flex items-center justify-between">
                  <div class="flex items-center">
                    <div class="flex text-yellow-400">
                      <svg v-for="i in 5" :key="i" class="h-5 w-5" fill="currentColor" viewBox="0 0 20 20">
                        <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z" />
                      </svg>
                    </div>
                    <span class="ml-2 text-gray-600">4.9/5</span>
                  </div>
                  <span class="text-sm text-gray-500">400+ Öğrenci</span>
                </div>
              </div>
            </div>
          </swiper-slide>

          <!-- Instructor 4 -->
          <swiper-slide>
            <div class="bg-white rounded-2xl shadow-lg hover:shadow-xl transition-shadow duration-300 overflow-hidden">
              <div class="relative">
                <div class="h-64 bg-gradient-to-br from-purple-500 to-purple-600 flex items-center justify-center">
                  <div class="w-32 h-32 bg-white rounded-full flex items-center justify-center">
                    <svg class="h-16 w-16 text-purple-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M16 7a4 4 0 11-8 0 4 4 0 018 0zM12 14a7 7 0 00-7 7h14a7 7 0 00-7-7z" />
                    </svg>
                  </div>
                </div>
                <div class="absolute top-4 right-4 bg-yellow-400 text-yellow-900 px-3 py-1 rounded-full text-sm font-semibold">
                  8 Yıl Deneyim
                </div>
              </div>
              <div class="p-6">
                <h3 class="text-2xl font-bold text-gray-900 mb-2">Mehmet Bey</h3>
                <p class="text-purple-600 font-semibold mb-4">Pratik Eğitmen</p>
                <p class="text-gray-600 mb-4 leading-relaxed">
                  Pratik sürüş teknikleri konusunda uzman. 
                  Öğrencilerine güven veren yaklaşımıyla tanınır.
                </p>
                <div class="flex items-center justify-between">
                  <div class="flex items-center">
                    <div class="flex text-yellow-400">
                      <svg v-for="i in 5" :key="i" class="h-5 w-5" fill="currentColor" viewBox="0 0 20 20">
                        <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z" />
                      </svg>
                    </div>
                    <span class="ml-2 text-gray-600">4.7/5</span>
                  </div>
                  <span class="text-sm text-gray-500">250+ Öğrenci</span>
                </div>
              </div>
            </div>
          </swiper-slide>
        </swiper>
      </div>

      <!-- Stats Section -->
      <div class="mt-16 grid grid-cols-1 md:grid-cols-4 gap-8">
        <div class="text-center">
          <div class="text-4xl font-bold text-blue-600 mb-2">15+</div>
          <div class="text-gray-600">Yıl Deneyim</div>
        </div>
        <div class="text-center">
          <div class="text-4xl font-bold text-blue-600 mb-2">2000+</div>
          <div class="text-gray-600">Başarılı Öğrenci</div>
        </div>
        <div class="text-center">
          <div class="text-4xl font-bold text-blue-600 mb-2">%95</div>
          <div class="text-gray-600">Başarı Oranı</div>
        </div>
        <div class="text-center">
          <div class="text-4xl font-bold text-blue-600 mb-2">4.8</div>
          <div class="text-gray-600">Ortalama Puan</div>
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
  color: #3B82F6;
}
</style>
