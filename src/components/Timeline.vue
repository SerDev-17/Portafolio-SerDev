<script>
export default {
    data() {
        return {
            timelineItems: [
                {
                    year: '2024',
                    title: 'Desarrollador Full Stack',
                    company: 'Freelance',
                    description: 'Desarrollo de aplicaciones web modernas con Vue.js, PHP y bases de datos. Enfoque en diseño UI/UX y experiencia de usuario.',
                    type: 'work'
                },
                {
                    year: '2023',
                    title: 'Certificación en Desarrollo Web',
                    company: 'Institución Educativa',
                    description: 'Formación intensiva en tecnologías frontend y backend, incluyendo JavaScript, Vue.js, PHP y Python.',
                    type: 'education'
                },
                {
                    year: '2022',
                    title: 'Desarrollador Frontend',
                    company: 'Proyecto Personal',
                    description: 'Creación de sitios web responsivos y landing pages con HTML, CSS, JavaScript y Tailwind CSS.',
                    type: 'work'
                },
                {
                    year: '2021',
                    title: 'Inicio en Programación',
                    company: 'Autodidacta',
                    description: 'Primeros pasos en el mundo del desarrollo web, aprendiendo fundamentos de HTML, CSS y JavaScript.',
                    type: 'education'
                }
            ]
        }
    }
}
</script>

<template>
    <section class="relative min-h-screen w-full bg-secundario p-8 flex flex-col items-center justify-center" data-aos="zoom-in" data-aos-duration="1500">
        <h2 class="text-5xl font-bold text-primario mb-16">Mi Trayectoria</h2>

        <div class="relative max-w-5xl w-full">
            <!-- Línea vertical central -->
            <div class="absolute left-1/2 transform -translate-x-1/2 h-full w-1 bg-terciario/30"></div>

            <!-- Items del timeline -->
            <div v-for="(item, index) in timelineItems" :key="index" class="relative mb-12 flex items-center"
                :class="index % 2 === 0 ? 'justify-start' : 'justify-end'">

                <!-- Contenedor del item -->
                <div class="w-5/12 group">
                    <div
                        class="bg-primario/90 backdrop-blur-sm rounded-3xl p-6 hover:bg-primario transition-all duration-300 hover:scale-105 hover:shadow-2xl cursor-pointer">
                        <!-- Año -->
                        <div class="flex items-center gap-3 mb-3">
                            <span class="text-3xl font-bold text-secundario">{{ item.year }}</span>
                            <span v-if="item.type === 'work'"
                                class="icon-[mdi--briefcase-outline] text-2xl text-secundario"></span>
                            <span v-else class="icon-[mdi--school-outline] text-2xl text-secundario"></span>
                        </div>

                        <!-- Título y empresa -->
                        <h3 class="text-xl font-bold text-secundario mb-2">{{ item.title }}</h3>
                        <p class="text-secundario/80 font-semibold mb-3">{{ item.company }}</p>

                        <!-- Descripción -->
                        <p class="text-secundario/70 text-sm leading-relaxed">{{ item.description }}</p>
                    </div>
                </div>

                <!-- Punto central en la línea -->
                <div
                    class="absolute left-1/2 transform -translate-x-1/2 w-6 h-6 bg-primario rounded-full border-4 p-3 border-terciario group-hover:scale-125 transition-transform duration-300 z-10">
                </div>
            </div>
        </div>
    </section>
</template>
