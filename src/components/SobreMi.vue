<script>
import iconoHtml from "../assets/Tecnologias/icono-html.svg"
import iconoCss from "../assets/Tecnologias/icono-css.svg"
import iconoJs from "../assets/Tecnologias/icono-js.svg"
import iconoVue from "../assets/Tecnologias/icono-vue.svg"
import iconoBaseDatos from "../assets/Tecnologias/icono-base-datos.svg"
import iconoPhp from "../assets/Tecnologias/icono-php.svg"
import iconoPython from "../assets/Tecnologias/icono-python.svg"
import iconoTailwind from "../assets/Tecnologias/icono-tailwind.svg"
export default {
    data() {
        return {
            "ImagenesTecnologias": [
                {
                    "src": iconoHtml,
                    "alt": "HTML"
                },
                {
                    "src": iconoCss,
                    "alt": "CSS"
                },
                {
                    "src": iconoJs,
                    "alt": "JS"
                },
                {
                    "src": iconoVue,
                    "alt": "Vue"
                },
                {
                    "src": iconoBaseDatos,
                    "alt": "Bases de datos"
                },
                {
                    "src": iconoPhp,
                    "alt": "PHP"
                },
                {
                    "src": iconoPython,
                    "alt": "Python"
                },
                {
                    "src": iconoTailwind,
                    "alt": "Tailwind"
                }
            ]
        }
    }
}
</script>

<template>
    <div class="relative min-h-screen" data-aos="zoom-in" data-aos-duration="1500">
        
        <div class="relative z-10 p-8 text-center flex flex-col justify-center items-center gap-10 min-h-screen">
            <h1 class="text-5xl font-bold text-primario mb-4">Sobre mí</h1>
            <p class="text-primario text-center text-lg w-3/4">Soy Sergio Naranjo, un desarrollador web apasionado por
                el
                diseño y la tecnología. Me especializo en crear sitios y aplicaciones que combinan funcionalidad,
                creatividad
                y una excelente experiencia de usuario. Disfruto cada reto y me comprometo a ofrecer soluciones
                digitales
                que
                aporten valor real a cada proyecto en el que participo.</p>
            <h1 class="text-5xl font-bold text-primario mb-4">Tecnologias</h1>
            <div class="flex flex-wrap gap-8 justify-center">
                <div v-for="imagen in ImagenesTecnologias" :key="imagen.alt"
                    class="group flex flex-col items-center cursor-pointer transition-all duration-300 hover:scale-110">
                    <div
                        class="p-4 rounded-2xl group-hover:bg-primario/20 transition-all duration-300 group-hover:shadow-lg">
                        <img :src="imagen.src" :alt="imagen.alt"
                            class="size-12 object-contain transition-all duration-300 group-hover:rotate-12 group-hover:scale-110">
                    </div>
                    <p
                        class="text-center text-lg font-semibold text-primario mt-2 group-hover:text-primario/80 transition-colors duration-300">
                        {{ imagen.alt }}
                    </p>
                </div>
            </div>
        </div>
    </div>
</template>