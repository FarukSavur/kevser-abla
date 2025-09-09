<template>
  <section id="testimonials" class="py-20 bg-gray-50">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <!-- Section Header -->
      <div class="text-center mb-16">
        <h2 class="text-4xl md:text-5xl font-bold text-gray-900 mb-6">
          Öğrenci Yorumları
        </h2>
        <p class="text-xl text-gray-600 max-w-3xl mx-auto">
          Başarılı öğrencilerimizin deneyimlerini okuyun. 
          Onların hikayeleri sizin de başarınızın habercisi.
        </p>
      </div>

      <!-- Testimonials Grid -->
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
        <!-- Testimonial 1 -->
        <div class="bg-white rounded-2xl shadow-lg p-8 hover:shadow-xl transition-shadow duration-300">
          <div class="flex items-center mb-6">
            <div class="w-16 h-16 bg-blue-100 rounded-full flex items-center justify-center mr-4">
              <svg class="h-8 w-8 text-blue-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M16 7a4 4 0 11-8 0 4 4 0 018 0zM12 14a7 7 0 00-7 7h14a7 7 0 00-7-7z" />
              </svg>
            </div>
            <div>
              <h4 class="text-lg font-semibold text-gray-900">Ayşe Yılmaz</h4>
              <p class="text-gray-600">B Sınıfı Ehliyet</p>
            </div>
          </div>
          <div class="flex text-yellow-400 mb-4">
            <svg v-for="i in 5" :key="i" class="h-5 w-5" fill="currentColor" viewBox="0 0 20 20">
              <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z" />
            </svg>
          </div>
          <p class="text-gray-700 leading-relaxed">
            "Kevser Abla ile çalışmak harika bir deneyimdi. Sabırlı ve anlayışlı yaklaşımı sayesinde 
            korkularımı yendim ve başarıyla ehliyetimi aldım. Herkese tavsiye ederim!"
          </p>
        </div>

        <!-- Testimonial 2 -->
        <div class="bg-white rounded-2xl shadow-lg p-8 hover:shadow-xl transition-shadow duration-300">
          <div class="flex items-center mb-6">
            <div class="w-16 h-16 bg-red-100 rounded-full flex items-center justify-center mr-4">
              <svg class="h-8 w-8 text-red-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M16 7a4 4 0 11-8 0 4 4 0 018 0zM12 14a7 7 0 00-7 7h14a7 7 0 00-7-7z" />
              </svg>
            </div>
            <div>
              <h4 class="text-lg font-semibold text-gray-900">Mehmet Kaya</h4>
              <p class="text-gray-600">A Sınıfı Ehliyet</p>
            </div>
          </div>
          <div class="flex text-yellow-400 mb-4">
            <svg v-for="i in 5" :key="i" class="h-5 w-5" fill="currentColor" viewBox="0 0 20 20">
              <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z" />
            </svg>
          </div>
          <p class="text-gray-700 leading-relaxed">
            "Motor ehliyeti almak istiyordum ama çok korkuyordum. Ahmet Bey'in profesyonel 
            yaklaşımı sayesinde güvenli bir şekilde motor kullanmayı öğrendim. Teşekkürler!"
          </p>
        </div>

        <!-- Testimonial 3 -->
        <div class="bg-white rounded-2xl shadow-lg p-8 hover:shadow-xl transition-shadow duration-300">
          <div class="flex items-center mb-6">
            <div class="w-16 h-16 bg-green-100 rounded-full flex items-center justify-center mr-4">
              <svg class="h-8 w-8 text-green-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M16 7a4 4 0 11-8 0 4 4 0 018 0zM12 14a7 7 0 00-7 7h14a7 7 0 00-7-7z" />
              </svg>
            </div>
            <div>
              <h4 class="text-lg font-semibold text-gray-900">Fatma Demir</h4>
              <p class="text-gray-600">B Sınıfı Ehliyet</p>
            </div>
          </div>
          <div class="flex text-yellow-400 mb-4">
            <svg v-for="i in 5" :key="i" class="h-5 w-5" fill="currentColor" viewBox="0 0 20 20">
              <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z" />
            </svg>
          </div>
          <p class="text-gray-700 leading-relaxed">
            "Esnek saatler ve birebir eğitim sayesinde iş hayatımla birlikte ehliyet derslerimi 
            rahatlıkla alabildim. Çok memnun kaldım, herkese tavsiye ederim."
          </p>
        </div>

        <!-- Testimonial 4 -->
        <div class="bg-white rounded-2xl shadow-lg p-8 hover:shadow-xl transition-shadow duration-300">
          <div class="flex items-center mb-6">
            <div class="w-16 h-16 bg-purple-100 rounded-full flex items-center justify-center mr-4">
              <svg class="h-8 w-8 text-purple-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M16 7a4 4 0 11-8 0 4 4 0 018 0zM12 14a7 7 0 00-7 7h14a7 7 0 00-7-7z" />
              </svg>
            </div>
            <div>
              <h4 class="text-lg font-semibold text-gray-900">Ali Özkan</h4>
              <p class="text-gray-600">A Sınıfı Ehliyet</p>
            </div>
          </div>
          <div class="flex text-yellow-400 mb-4">
            <svg v-for="i in 5" :key="i" class="h-5 w-5" fill="currentColor" viewBox="0 0 20 20">
              <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z" />
            </svg>
          </div>
          <p class="text-gray-700 leading-relaxed">
            "Modern motosikletlerle eğitim almak gerçekten fark yaratıyor. Eğitmenler çok 
            profesyonel ve güvenli sürüş tekniklerini çok iyi öğretiyorlar."
          </p>
        </div>

        <!-- Testimonial 5 -->
        <div class="bg-white rounded-2xl shadow-lg p-8 hover:shadow-xl transition-shadow duration-300">
          <div class="flex items-center mb-6">
            <div class="w-16 h-16 bg-yellow-100 rounded-full flex items-center justify-center mr-4">
              <svg class="h-8 w-8 text-yellow-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M16 7a4 4 0 11-8 0 4 4 0 018 0zM12 14a7 7 0 00-7 7h14a7 7 0 00-7-7z" />
              </svg>
            </div>
            <div>
              <h4 class="text-lg font-semibold text-gray-900">Zeynep Arslan</h4>
              <p class="text-gray-600">B Sınıfı Ehliyet</p>
            </div>
          </div>
          <div class="flex text-yellow-400 mb-4">
            <svg v-for="i in 5" :key="i" class="h-5 w-5" fill="currentColor" viewBox="0 0 20 20">
              <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z" />
            </svg>
          </div>
          <p class="text-gray-700 leading-relaxed">
            "Sınav hazırlığı konusunda çok yardımcı oldular. Deneme sınavları ve birebir 
            koçluk sayesinde ilk denemede başarılı oldum. Çok teşekkürler!"
          </p>
        </div>

        <!-- Testimonial 6 -->
        <div class="bg-white rounded-2xl shadow-lg p-8 hover:shadow-xl transition-shadow duration-300">
          <div class="flex items-center mb-6">
            <div class="w-16 h-16 bg-indigo-100 rounded-full flex items-center justify-center mr-4">
              <svg class="h-8 w-8 text-indigo-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M16 7a4 4 0 11-8 0 4 4 0 018 0zM12 14a7 7 0 00-7 7h14a7 7 0 00-7-7z" />
              </svg>
            </div>
            <div>
              <h4 class="text-lg font-semibold text-gray-900">Can Yıldız</h4>
              <p class="text-gray-600">A Sınıfı Ehliyet</p>
            </div>
          </div>
          <div class="flex text-yellow-400 mb-4">
            <svg v-for="i in 5" :key="i" class="h-5 w-5" fill="currentColor" viewBox="0 0 20 20">
              <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z" />
            </svg>
          </div>
          <p class="text-gray-700 leading-relaxed">
            "Hollanda'da ehliyet almak zor sanıyordum ama doğru eğitmenle çok kolaymış. 
            Kevser Abla'nın kursu sayesinde hem teorik hem pratik sınavları geçtim."
          </p>
        </div>
      </div>

      <!-- CTA Section -->
      <div class="mt-16 text-center">
        <div class="bg-blue-600 rounded-2xl p-8 text-white">
          <h3 class="text-3xl font-bold mb-4">Siz de Başarılı Öğrencilerimizden Biri Olun!</h3>
          <p class="text-xl text-blue-100 mb-6">
            Hemen ücretsiz danışmanlık alın ve size uygun programı keşfedin.
          </p>
          <button class="bg-yellow-400 text-blue-900 px-8 py-4 rounded-lg font-bold text-lg hover:bg-yellow-300 transition-colors">
            Ücretsiz Danışmanlık Al
          </button>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
// Testimonials section logic can be added here if needed
</script>
