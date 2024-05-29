<script setup>
import { onMounted, ref } from "vue";

const navbar = ref('')
const showMenu = ref(false)

onMounted(() => {
  window.onscroll = () => {
  if(window.scrollY === 0) {
    navbar.value.classList.remove('bg-primary-200')
  } else {
    navbar.value.classList.add('bg-primary-200')
  }
}
})
</script>

<template>
  <nav ref="navbar" class="fixed top-0 left-0 w-full bg-primary-200 z-20 transition duration-200"> 
    <div class="container flex items-center justify-between h-20">
      <div class="relative z-30 flex items-center gap-2 mb-2 lg:mb-0">
        <h1 class="text-white font-bold text-lg lg:text-2xl">3D <span class="text-secondary">BACKGROUND</span></h1>
       
      </div>
      <div class="flex lg:hidden items-center gap-2">
        <button class="relative z-30 px-4 py-2 -mt-1.5 text-sm rounded-full text-white font-medium tracking-wider uppercase bg-secondary w-full lg:w-auto">Donate</button>
        <button @click="showMenu = !showMenu" class="relative z-30 text-white -mt-2 p-2">
          <svg width="18" height="12" viewBox="0 0 18 12" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M1 12H17C17.55 12 18 11.55 18 11C18 10.45 17.55 10 17 10H1C0.45 10 0 10.45 0 11C0 11.55 0.45 12 1 12ZM1 7H17C17.55 7 18 6.55 18 6C18 5.45 17.55 5 17 5H1C0.45 5 0 5.45 0 6C0 6.55 0.45 7 1 7ZM0 1C0 1.55 0.45 2 1 2H17C17.55 2 18 1.55 18 1C18 0.45 17.55 0 17 0H1C0.45 0 0 0.45 0 1Z" fill="white"/>
          </svg>
        </button>
      </div>
      <div
        class="
          absolute lg:static top-20 inset-x-0
          flex flex-col lg:flex-row items-center gap-5 lg:gap-10
          bg-primary-200 lg:bg-transparent pt-5 pb-10 px-5 lg:p-0
          transition duration-500 lg:duration-200 lg:-translate-y-0
        "
        :class="!showMenu ? 'translate-y-[-150%]' : '-translate-y-0'"
      >
        <a @click="showMenu = false" class="text-white font-medium" href="#home">Home</a>
        <a @click="showMenu = false" class="text-white font-medium" href="#category">Category</a>
        <a @click="showMenu = false" class="text-white font-medium" href="#about">About</a>
        <a @click="showMenu = false" class="text-white font-medium" href="#trick-or-treat">The pest</a>
        <button class="hidden md:block px-8 py-3 rounded-full text-white font-medium tracking-wider uppercase bg-secondary w-full lg:w-auto">Donate</button>
      </div>
    </div>
  </nav>
</template>