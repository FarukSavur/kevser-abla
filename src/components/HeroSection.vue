<template>
  <section id="home" class="relative min-h-screen flex items-center bg-gradient-to-br from-slate-900 via-blue-900 to-indigo-900 text-white overflow-hidden pt-20">
    <!-- Animated Background -->
    <div class="absolute inset-0">
      <!-- Gradient Orbs -->
      <div class="absolute top-1/4 left-1/4 w-96 h-96 bg-blue-500/20 rounded-full blur-3xl animate-pulse"></div>
      <div class="absolute bottom-1/4 right-1/4 w-80 h-80 bg-orange-500/20 rounded-full blur-3xl animate-pulse delay-1000"></div>
      <div class="absolute top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2 w-64 h-64 bg-purple-500/20 rounded-full blur-3xl animate-pulse delay-500"></div>
      
      <!-- Floating Elements -->
      <div class="absolute top-20 left-20 w-4 h-4 bg-white/30 rounded-full animate-bounce delay-300"></div>
      <div class="absolute top-40 right-32 w-6 h-6 bg-orange-400/40 rounded-full animate-bounce delay-700"></div>
      <div class="absolute bottom-32 left-1/3 w-3 h-3 bg-blue-300/50 rounded-full animate-bounce delay-1000"></div>
      <div class="absolute bottom-20 right-20 w-5 h-5 bg-white/20 rounded-full animate-bounce delay-500"></div>
      
      <!-- Grid Pattern -->
      <div class="absolute inset-0 opacity-30">
        <div class="w-full h-full bg-dot-pattern"></div>
      </div>
    </div>

    <div class="relative max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-20 lg:py-32">
      <div class="grid grid-cols-1 lg:grid-cols-2 gap-16 items-center">
        <!-- Content -->
        <div class="text-center lg:text-left space-y-8">
          <!-- Badge -->
          <div class="inline-flex items-center px-4 py-2 bg-white/10 backdrop-blur-sm border border-white/20 rounded-full text-sm font-medium text-white/90">
            <svg class="w-4 h-4 mr-2 text-orange-400" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z" />
            </svg>
            #1 Rijschool in Nederland
          </div>

          <h1 class="text-5xl md:text-6xl lg:text-7xl font-bold leading-tight">
            Word een
            <span class="bg-gradient-to-r from-orange-400 via-orange-500 to-yellow-400 bg-clip-text text-transparent animate-pulse">
              Veilige Bestuurder
            </span>
            in Nederland
          </h1>
          
          <p class="text-xl md:text-2xl text-gray-300 leading-relaxed max-w-2xl">
            Met <span class="text-orange-400 font-bold">15 jaar ervaring</span> geven wij autorijlessen en motorrijlessen. 
            Ons slagingspercentage is meer dan <span class="text-orange-400 font-bold">95%</span>!
          </p>
          
          <!-- Features -->
          <div class="grid grid-cols-1 sm:grid-cols-3 gap-6">
            <div class="flex flex-col items-center lg:items-start space-y-2 p-4 bg-white/5 backdrop-blur-sm rounded-2xl border border-white/10">
              <div class="w-12 h-12 bg-gradient-to-r from-orange-500 to-orange-600 rounded-xl flex items-center justify-center">
                <svg class="h-6 w-6 text-white" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z" />
                </svg>
              </div>
              <span class="text-white font-semibold">95% Slagingspercentage</span>
            </div>
            <div class="flex flex-col items-center lg:items-start space-y-2 p-4 bg-white/5 backdrop-blur-sm rounded-2xl border border-white/10">
              <div class="w-12 h-12 bg-gradient-to-r from-blue-500 to-blue-600 rounded-xl flex items-center justify-center">
                <svg class="h-6 w-6 text-white" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z" />
                </svg>
              </div>
              <span class="text-white font-semibold">15 Jaar Ervaring</span>
            </div>
            <div class="flex flex-col items-center lg:items-start space-y-2 p-4 bg-white/5 backdrop-blur-sm rounded-2xl border border-white/10">
              <div class="w-12 h-12 bg-gradient-to-r from-green-500 to-green-600 rounded-xl flex items-center justify-center">
                <svg class="h-6 w-6 text-white" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z" />
                </svg>
              </div>
              <span class="text-white font-semibold">Flexibele Tijden</span>
            </div>
          </div>

          <!-- CTA Buttons -->
          <div class="flex flex-col sm:flex-row gap-4 justify-center lg:justify-start">
            <button class="group relative bg-gradient-to-r from-orange-500 to-orange-600 text-white px-8 py-4 rounded-2xl font-bold text-lg shadow-2xl hover:shadow-orange-500/25 transition-all duration-300 hover:scale-105 overflow-hidden">
              <span class="relative z-10 flex items-center justify-center">
                Gratis Advies
                <svg class="w-5 h-5 ml-2 group-hover:translate-x-1 transition-transform duration-300" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 7l5 5m0 0l-5 5m5-5H6" />
                </svg>
              </span>
              <div class="absolute inset-0 bg-gradient-to-r from-orange-600 to-orange-700 opacity-0 group-hover:opacity-100 transition-opacity duration-300"></div>
            </button>
            <button class="group border-2 border-white/30 text-white px-8 py-4 rounded-2xl font-bold text-lg hover:bg-white/10 hover:border-white/50 transition-all duration-300 hover:scale-105 backdrop-blur-sm">
              <span class="flex items-center justify-center">
                Bekijk Onze Diensten
                <svg class="w-5 h-5 ml-2 group-hover:translate-x-1 transition-transform duration-300" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 7l5 5m0 0l-5 5m5-5H6" />
                </svg>
              </span>
            </button>
          </div>
        </div>

        <!-- Image/Visual -->
        <div class="relative">
          <!-- Main Card -->
          <div class="relative bg-white/10 backdrop-blur-md rounded-3xl p-8 shadow-2xl border border-white/20 overflow-hidden">
            <!-- Background Pattern -->
            <div class="absolute inset-0 bg-gradient-to-br from-blue-500/10 to-orange-500/10"></div>
            <div class="absolute top-0 right-0 w-32 h-32 bg-gradient-to-br from-orange-400/20 to-orange-600/20 rounded-full blur-2xl"></div>
            <div class="absolute bottom-0 left-0 w-24 h-24 bg-gradient-to-tr from-blue-400/20 to-blue-600/20 rounded-full blur-2xl"></div>
            
            <div class="relative z-10">
              <!-- Car Section -->
              <div class="text-center mb-8 group">
                <div class="relative inline-block">
                  <div class="absolute inset-0 bg-gradient-to-r from-orange-500 to-orange-600 rounded-2xl blur-lg opacity-50 group-hover:opacity-75 transition-opacity duration-300"></div>
                  <div class="relative bg-gradient-to-r from-orange-500 to-orange-600 p-6 rounded-2xl shadow-xl group-hover:scale-105 transition-transform duration-300">
                    <svg class="h-16 w-16 text-white mx-auto" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 7h12m0 0l-4-4m4 4l-4 4m0 6H4m0 0l4 4m-4-4l4-4" />
                    </svg>
                  </div>
                </div>
                <h3 class="text-2xl font-bold text-white mt-6 mb-2">Autorijlessen</h3>
                <p class="text-gray-300 text-lg">B Rijbewijs</p>
                <div class="mt-4 inline-flex items-center px-4 py-2 bg-white/10 rounded-full text-sm text-white/90">
                  <svg class="w-4 h-4 mr-2 text-orange-400" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z" />
                  </svg>
                  Vanaf €45/les
                </div>
              </div>

              <!-- Divider -->
              <div class="w-full h-px bg-gradient-to-r from-transparent via-white/30 to-transparent mb-8"></div>

              <!-- Motor Section -->
              <div class="text-center group">
                <div class="relative inline-block">
                  <div class="absolute inset-0 bg-gradient-to-r from-blue-500 to-blue-600 rounded-2xl blur-lg opacity-50 group-hover:opacity-75 transition-opacity duration-300"></div>
                  <div class="relative bg-gradient-to-r from-blue-500 to-blue-600 p-6 rounded-2xl shadow-xl group-hover:scale-105 transition-transform duration-300">
                    <svg class="h-16 w-16 text-white mx-auto" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z" />
                    </svg>
                  </div>
                </div>
                <h3 class="text-2xl font-bold text-white mt-6 mb-2">Motorrijlessen</h3>
                <p class="text-gray-300 text-lg">A Rijbewijs</p>
                <div class="mt-4 inline-flex items-center px-4 py-2 bg-white/10 rounded-full text-sm text-white/90">
                  <svg class="w-4 h-4 mr-2 text-blue-400" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z" />
                  </svg>
                  Vanaf €50/les
                </div>
              </div>
            </div>
          </div>

          <!-- Floating Elements -->
          <div class="absolute -top-8 -right-8 w-24 h-24 bg-gradient-to-r from-orange-400 to-orange-500 rounded-full opacity-60 animate-pulse shadow-lg"></div>
          <div class="absolute -bottom-8 -left-8 w-20 h-20 bg-gradient-to-r from-blue-400 to-blue-500 rounded-full opacity-60 animate-bounce shadow-lg"></div>
          <div class="absolute top-1/2 -left-6 w-12 h-12 bg-gradient-to-r from-purple-400 to-purple-500 rounded-full opacity-50 animate-ping shadow-lg"></div>
          <div class="absolute top-1/4 -right-4 w-8 h-8 bg-gradient-to-r from-green-400 to-green-500 rounded-full opacity-40 animate-bounce delay-1000 shadow-lg"></div>
        </div>
      </div>
    </div>

    <!-- Scroll Indicator -->
    <div class="absolute bottom-8 left-1/2 transform -translate-x-1/2 animate-bounce">
      <div class="flex flex-col items-center space-y-2">
        <span class="text-white/60 text-sm font-medium">Scroll om meer te ontdekken</span>
        <div class="w-6 h-10 border-2 border-white/30 rounded-full flex justify-center">
          <div class="w-1 h-3 bg-white/60 rounded-full mt-2 animate-bounce"></div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
// Hero section logic can be added here if needed
</script>
