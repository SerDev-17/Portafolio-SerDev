<script setup>
import NavBar from './components/NavBar.vue'
import back from './assets/back.svg'
import SobreMi from './components/SobreMi.vue'
import Servicios from './components/Servicios.vue'
import CategoriasProyectos from './components/CategoriasProyectos.vue'
import Timeline from './components/Timeline.vue'
import Proyectos from './components/Proyectos.vue'
import Footer from './components/Footer.vue'
import Hero from './components/Hero.vue'
</script>

<template>
  <div class="grid grid-cols-1 bg-secundario">
    <header id="inicio" class="h-screen relative grid place-items-center overflow-hidden bg-terciario rounded-b-3xl">
      <img :src="back" alt="Background" class="absolute inset-0 w-full h-full object-cover opacity-50">
      <NavBar class="bg-primario rounded-3xl p-2 w-1/2 z-10 absolute top-4" />

      <Hero />
    </header>

    <main class="relative min-h-screen bg-secundario flex flex-col items-center justify-center overflow-hidden">

      <SobreMi id="sobre-mi" />
      <Servicios id="servicios" />
      <CategoriasProyectos />
      <Proyectos id="proyectos" />
      <Timeline />
    </main>
    <Footer id="contacto" />

  </div>

</template>
