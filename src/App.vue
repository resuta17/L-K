<script setup>
import { onMounted, ref } from 'vue'


  const nav = ref(false)
  
  function clickedNav(){
      nav.value = !nav.value
      console.log(nav.value)
  }
  
  onMounted(() => {
    setTimeout(() => {
      nav.value = true
    }, 500)
  })
    
  
  
</script>

<template>
  <div class="shadow-md rounded-b-lg h-98 bg-[url('https://scontent.flgp1-1.fna.fbcdn.net/v/t39.30808-6/474745743_1313418899682440_5239560385679872531_n.jpg?_nc_cat=107&ccb=1-7&_nc_sid=833d8c&_nc_eui2=AeGvi9hDP8k21iBNnhyf200RT5BH2s63y5NPkEfazrfLkwNQ7iMX_25_PocPRjt3J8AHBLUvLnHkabCosil_cWh6&_nc_ohc=pxB3yYymN1YQ7kNvwFN9k5X&_nc_oc=Adl_yyQyVhuXTaa2xKG54FsQ4gVdAR1ZEdwDSuMrXgjeRXPcipcdFSrjpGZVgeQAsRE&_nc_zt=23&_nc_ht=scontent.flgp1-1.fna&_nc_gid=eXa1SbtLWdbf9u4O8F55WA&oh=00_AfNfyJpVQzF9XFEUYzUQkb4Rbd_ZmE6IReIW19Q2n4uZNA&oe=685599C4')] bg-cover bg-center" alt="Store front of LK’s Minimart" >
    <div class="sticky top-0 z-50 opacity-80 text-white">
      <header class="max-width bg-yellow-600 h-24 flex items-center justify-between px-6" :class="{ 'rounded-b-lg': !nav }">
        <div class="flex items-center">
          <img :src="'https://cdn-icons-png.flaticon.com/128/10461/10461387.png'" class="w-14"/>
          <p class="text-white font-bold text-3xl ml-4">
            LK's Minimart
          </p>
        </div>

        <button @click="clickedNav" id="hamburger-button" class="text-white hover:text-gray-200 focus:outline-none focus:text-gray-200 border rounded-sm">
          <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"></path>
          </svg>
        </button>
      </header>
      <nav v-show="nav" class="flex flex-col items-center justify-center bg-yellow-600 opacity-80 rounded-b-lg border-t-2 border-white">
          <a class="py-2 text-white border-b border-white w-[90%] text-center">About</a>
          <a class="py-2 text-white border-b border-white w-[90%] text-center">Product</a>
          <a class="py-2 text-white w-[90%] text-center">Contact</a>
      </nav>  
    </div> 
    
  </div>
  <div class="flex items-center justify-center space-x-2 mt-4">
      <div>
        <img :src="'https://cdn-icons-png.flaticon.com/128/684/684908.png'" class="w-6 h-6"/>
      </div>
      <div>
        <a target="_blank" href="https://www.google.com/maps/place/Leanne+and+Kirby+Balloons+Party/@12.8451868,123.990664,20.11z/data=!4m6!3m5!1s0x33a0c2c4190c3415:0xdc997e7a68e532fc!8m2!3d12.8450916!4d123.9905773!16s%2Fg%2F11f15pz34y?entry=ttu&g_ep=EgoyMDI1MDYxMC4xIKXMDSoASAFQAw%3D%3D">
           Purok 4, South Poblacion, Juban, Sorsogon
        </a>

      </div>
  </div>
  <body class="m-10">
    <section class=" flex items-start justify-center mt-20">
      <div class="flex-col">
        <p class="font-bold text-2xl text-center mb-2 text-[#1068C0]">
          STORE PROFILE
        </p>
        <p>
          LK’s Minimart is your friendly neighborhood one-stop shop for everyday essentials and celebration needs. 
        </p>   
      </div>
    </section>
    <section class="mt-20 border border-gray-200 p-4">
      <h1 class="mt-10 flex justify-center font-bold text-2xl text-[#1068C0] mb-10">
        WE OFFER
      </h1>
      
      <div class="space-y-20">        
        <div class="flex items-center space-x-6">
          <div class="w-1/2 h-62  shadow-xl rounded-r-lg flex items-center justify-center border border-gray-300 bg-white">
            <p class=" text-center text-4xl">
              Flower Bouquet
            </p>
          </div>
          <img src="https://scontent.flgp1-1.fna.fbcdn.net/v/t39.30808-6/474748503_1313407933016870_3065581096343235001_n.jpg?_nc_cat=109&ccb=1-7&_nc_sid=833d8c&_nc_eui2=AeHEOlS62U9ooWQggs-BOAAUYbheL6l6dihhuF4vqXp2KPi-Qevg9v2SJVo8DdA6oqvufUVMF2S_NyTJOX0u7Ve3&_nc_ohc=WslmM-4UhiQQ7kNvwGCT3OR&_nc_oc=AdmQc9EtwmBgQvaLChDJhJQuHoIbzbibxX1o3K3uLiCQsMLVLGoVkcjjpSdbYSqVpZ0&_nc_zt=23&_nc_ht=scontent.flgp1-1.fna&_nc_gid=19v8Lguqli04E165yVYscQ&oh=00_AfM_SpJpbhCMB7LWvhzLgKeyC6Wjy2mBwpV1-OjoyGbzLg&oe=68558E6F" 
          class="w-[45%] h-62 object-cover border border-gray-600 shadow-xl rounded-lg" />
        </div>

        <div class="flex items-center justify-end space-x-6">
          <div class="w-1/2 h-62  shadow-xl rounded-l-lg flex-col items-center justify-center border border-gray-300">
            <p class="text-center text-4xl mt-5">
              Cake
            </p>
            <p  class="text-center">
              Lorem ipsum
            </p>
          </div>
        </div>

        <div class="flex items-center space-x-6">
          <div class="w-1/2 h-62  shadow-xl rounded-r-lg flex items-center justify-center border border-gray-300 bg-white">
            <p class="text-center text-4xl">
              Party Shop
            </p>
          </div>
          <img src="https://scontent.flgp1-1.fna.fbcdn.net/v/t39.30808-6/474793346_1313407923016871_3433423636582494605_n.jpg?_nc_cat=103&ccb=1-7&_nc_sid=833d8c&_nc_eui2=AeFYMded8wDGEDFlV3vuNfRhRpiRwJtMaYVGmJHAm0xphStUHzuqgn16I5ti9xH4MgJK3PX3JeJRBEQqmhx0N9yC&_nc_ohc=nS7wnqegkwoQ7kNvwEEitec&_nc_oc=AdnPga8clFSZjF0Za268o8rxKGN8ds5RDFvKtPtoAnuGnYZg9L25MSjGNqBjM6mqUBY&_nc_zt=23&_nc_ht=scontent.flgp1-1.fna&_nc_gid=yxQ6vgjKdVsMgSARZltTTw&oh=00_AfMg8ffTD8T7Vgr3-Gnl6S9j6GLT35z_Od6Wnxk85kRZDA&oe=685588F0" 
          class="w-[45%] h-62 object-cover border border-gray-600 shadow-xl rounded-lg" />
        </div>
        
        <div class="flex items-center justify-end space-x-6">
          <img src="https://scontent.flgp1-1.fna.fbcdn.net/v/t39.30808-6/474745175_1313407919683538_4754889622248912206_n.jpg?_nc_cat=110&ccb=1-7&_nc_sid=833d8c&_nc_eui2=AeHD8dq95sD840pY5U0QChqpo0OjjEPcQYKjQ6OMQ9xBguS-HqlBAFu3pdyiakSVVxgEX5oXcfeFEQqHjcIsOevk&_nc_ohc=5VuYtLzjWQ8Q7kNvwFQu3QV&_nc_oc=AdlumRpJ4HfMwWeDH0QsgTcWInLneoBf4qaQBhTe7GW4xxAqlpXdDfdJ4e2yyHQN8k0&_nc_zt=23&_nc_ht=scontent.flgp1-1.fna&_nc_gid=n5z2soSn2giNhs4ApBsYzQ&oh=00_AfPIhCxalBcGKfZwwoC4K7dH1DDR4tw9zqoLHlNMVdDv0Q&oe=6855A67F" 
            class="w-[45%] h-62 object-cover border border-gray-600 shadow-xl rounded-lg" />
          <div class="w-1/2 h-62  shadow-xl rounded-l-lg flex items-center justify-center border border-gray-300 bg-white">
            <p class="text-center text-4xl">
              Grocery
            </p>
          </div>
        </div>
      </div>
    </section>
    <footer class="bg-yellow-600 mt-10">
        <p>
          Contact Us!
        </p>
    </footer>
  </body>
  
</template>

<style scoped>

  
</style>
