<script>
export default {
    data() {
        return {
            services: [
                {
                    title: 'UI/UX Design',
                    description: 'Diseño de interfaces intuitivas y atractivas que mejoran la experiencia del usuario.',
                    icon: 'icon-[mdi--palette-outline]'
                },
                {
                    title: 'Web Design',
                    description: 'Desarrollo de sitios web modernos, responsivos y optimizados para todos los dispositivos.',
                    icon: 'icon-[mdi--web]'
                },
                {
                    title: 'Landing Page',
                    description: 'Páginas de aterrizaje diseñadas para convertir visitantes en clientes potenciales.',
                    icon: 'icon-[mdi--rocket-launch-outline]'
                },
                {
                    title: 'Desarrollo Frontend',
                    description: 'Implementación de aplicaciones web con las últimas tecnologías y mejores prácticas.',
                    icon: 'icon-[mdi--code-tags]'
                },
                {
                    title: 'Desarrollo Backend',
                    description: 'Desarrollo de aplicaciones web con las últimas tecnologías y mejores prácticas.',
                    icon: 'icon-[mdi--code]'
                },
                {
                    title: 'Optimización Web',
                    description: 'Mejora del rendimiento y velocidad de carga de sitios web existentes.',
                    icon: 'icon-[mdi--speedometer]'
                }
            ]
        }
    }
}
</script>

<template>
    <section class="relative min-h-screen w-full bg-secundario p-8 flex flex-col items-center justify-center" data-aos="zoom-in" data-aos-duration="1500">
        <h2 class="text-5xl font-bold text-primario mb-12">Mis Servicios</h2>

        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8 max-w-7xl w-full">
            <div v-for="service in services" :key="service.title"
                class="group bg-primario/90 backdrop-blur-sm rounded-3xl p-8 hover:bg-primario transition-all duration-300 hover:scale-105 hover:shadow-2xl cursor-pointer">

                <!-- Icon -->
                <div class="mb-6 flex justify-between items-start">
                    <div
                        class="p-4 bg-secundario/20 rounded-2xl group-hover:bg-secundario/30 transition-all duration-300">
                        <span :class="service.icon" class="text-5xl text-secundario"></span>
                    </div>
                    
                </div>

                <!-- Content -->
                <h3 class="text-2xl font-bold text-secundario mb-4">{{ service.title }}</h3>
                <p class="text-secundario/80 text-base leading-relaxed">{{ service.description }}</p>
            </div>
        </div>
    </section>
</template>