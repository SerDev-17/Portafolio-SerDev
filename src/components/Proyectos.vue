<script>
export default {
    data() {
        return {
            projects: [
                {
                    title: 'E-Commerce Moderno',
                    description: 'Plataforma de comercio electrónico completa con carrito de compras, pasarela de pagos y panel de administración.',
                    technologies: ['Vue.js', 'PHP', 'MySQL', 'Tailwind'],
                    image: 'https://images.unsplash.com/photo-1557821552-17105176677c?w=800&h=600&fit=crop',
                    link: '#',
                    category: 'Web App'
                },
                {
                    title: 'Dashboard Analytics',
                    description: 'Panel de control interactivo con gráficos en tiempo real y visualización de datos empresariales.',
                    technologies: ['Vue.js', 'Python', 'Chart.js'],
                    image: 'https://images.unsplash.com/photo-1551288049-bebda4e38f71?w=800&h=600&fit=crop',
                    link: '#',
                    category: 'Dashboard'
                },
                {
                    title: 'Landing Page Corporativa',
                    description: 'Sitio web corporativo con diseño elegante, animaciones suaves y optimización SEO.',
                    technologies: ['HTML', 'CSS', 'JavaScript'],
                    image: 'https://images.unsplash.com/photo-1460925895917-afdab827c52f?w=800&h=600&fit=crop',
                    link: '#',
                    category: 'Landing'
                },
                {
                    title: 'App de Gestión de Tareas',
                    description: 'Aplicación web para gestión de proyectos con sistema de tareas, colaboración en equipo y notificaciones.',
                    technologies: ['Vue.js', 'PHP', 'MySQL'],
                    image: 'https://images.unsplash.com/photo-1454165804606-c3d57bc86b40?w=800&h=600&fit=crop',
                    link: '#',
                    category: 'Web App'
                },
                {
                    title: 'Portfolio Creativo',
                    description: 'Portafolio personal con diseño único, galería de proyectos y formulario de contacto integrado.',
                    technologies: ['Vue.js', 'Tailwind', 'EmailJS'],
                    image: 'https://images.unsplash.com/photo-1467232004584-a241de8bcf5d?w=800&h=600&fit=crop',
                    link: '#',
                    category: 'Portfolio'
                },
                {
                    title: 'Sistema de Reservas',
                    description: 'Plataforma de reservas online con calendario interactivo, gestión de disponibilidad y confirmaciones automáticas.',
                    technologies: ['Vue.js', 'PHP', 'MySQL'],
                    image: 'https://images.unsplash.com/photo-1506784983877-45594efa4cbe?w=800&h=600&fit=crop',
                    link: '#',
                    category: 'Web App'
                }
            ]
        }
    }
}
</script>

<template>
    <section class="relative min-h-screen w-full bg-secundario p-8 flex flex-col items-center justify-center">
        <h2 class="text-5xl font-bold text-primario mb-4">Mis Proyectos</h2>
        <p class="text-primario/70 text-lg mb-12 text-center max-w-2xl">
            Una selección de proyectos que demuestran mis habilidades en desarrollo web y diseño
        </p>

        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8 max-w-7xl w-full">
            <div v-for="project in projects" :key="project.title"
                class="group relative bg-terciario rounded-3xl overflow-hidden hover:shadow-2xl transition-all duration-300 hover:scale-105 cursor-pointer">

                <!-- Imagen del proyecto -->
                <div class="relative h-56 overflow-hidden">
                    <img :src="project.image" :alt="project.title"
                        class="w-full h-full object-cover transition-transform duration-500 group-hover:scale-110">

                    <!-- Overlay con categoría -->
                    <div class="absolute top-4 right-4 bg-primario/90 backdrop-blur-sm px-4 py-2 rounded-full">
                        <span class="text-secundario font-semibold text-sm">{{ project.category }}</span>
                    </div>
                </div>

                <!-- Contenido -->
                <div class="p-6">
                    <h3 class="text-2xl font-bold text-primario mb-3 group-hover:text-primario/80 transition-colors">
                        {{ project.title }}
                    </h3>

                    <p class="text-primario/70 text-sm leading-relaxed mb-4">
                        {{ project.description }}
                    </p>

                    <!-- Tecnologías -->
                    <div class="flex flex-wrap gap-2 mb-4">
                        <span v-for="tech in project.technologies" :key="tech"
                            class="px-3 py-1 bg-primario/20 rounded-full text-primario text-xs font-semibold">
                            {{ tech }}
                        </span>
                    </div>

                    <!-- Botón de ver proyecto -->
                    <a :href="project.link"
                        class="inline-flex items-center gap-2 text-primario font-semibold hover:gap-4 transition-all duration-300">
                        Ver proyecto
                        <span class="icon-[mdi--arrow-right] text-xl"></span>
                    </a>
                </div>
            </div>
        </div>
    </section>
</template>
