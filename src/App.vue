<script setup>
import NavBar from './components/NavBar.vue'
import back from './assets/back.svg'
import dibujos from './assets/dibujos.svg'
import SobreMi from './components/SobreMi.vue'
</script>

<template>
  <div class="grid grid-cols-1">
    <header class="h-screen relative grid place-items-center overflow-hidden bg-terciario">
      <img :src="back" alt="Background" class="absolute inset-0 w-full h-full object-cover opacity-50">
      <NavBar class="bg-primario rounded-3xl p-2 w-1/2 z-10 absolute top-4" />

      <div class="z-10 text-center">
        <h1 class="text-4xl font-bold text-white mb-4">Bienvenido a mi Portafolio</h1>
        <p class="text-xl text-white">Descubre mis proyectos y habilidades</p>
      </div>
    </header>

    <main class="relative min-h-screen bg-secundario flex flex-col items-center justify-center overflow-hidden">
      <img :src="dibujos" alt="Background" class="absolute inset-0 w-full h-full object-cover opacity-50">
      <div class="relative z-10 p-8 text-center flex flex-col justify-center items-center -top-50 gap-10">
        <SobreMi />
      </div>
    </main>
    <footer class="p-8 bg-gray-800 text-white">
      <h1>Footer</h1>
    </footer>

  </div>

</template>
