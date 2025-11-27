<script setup>
import NavBar from './components/NavBar.vue'
import back from './assets/back.svg'
import SobreMi from './components/SobreMi.vue'
import Servicios from './components/Servicios.vue'
import Footer from './components/Footer.vue'
</script>

<template>
  <div class="grid grid-cols-1 bg-secundario">
    <header class="h-screen relative grid place-items-center overflow-hidden bg-terciario rounded-b-3xl">
      <img :src="back" alt="Background" class="absolute inset-0 w-full h-full object-cover opacity-50">
      <NavBar class="bg-primario rounded-3xl p-2 w-1/2 z-10 absolute top-4" />

      <div class="z-10 text-center">
        <h1 class="text-4xl font-bold text-white mb-4">Bienvenido a mi Portafolio</h1>
        <p class="text-xl text-white">Descubre mis proyectos y habilidades</p>
      </div>
    </header>

    <main class="relative min-h-screen bg-secundario flex flex-col items-center justify-center overflow-hidden">
      
        <SobreMi />
        <Servicios />
    </main>
    <Footer />

  </div>

</template>
