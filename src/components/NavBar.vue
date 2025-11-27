<script>
export default {
    data() {
        return {
            "Links": [
                {
                    "href": "#",
                    "text": "Inicio"
                },
                {
                    "href": "#",
                    "text": "Sobre mí"
                },
                {
                    "href": "#",
                    "text": "Servicios"
                },
                {
                    "href": "#",
                    "text": "Proyectos"
                },
                {
                    "href": "#",
                    "text": "Contacto"
                }
            ]
        }
    }
}
</script>

<template>
    <nav class="bg-primario">
        <ul class="flex justify-around text-terciario">
            <li v-for="link in Links" :key="link.href">
                <a :href="link.href" class="relative group transition-colors duration-300 hover:text-white">
                    {{ link.text }}
                    <span
                        class="absolute left-0 bottom-0 w-0 h-0.5 bg-white transition-all duration-300 group-hover:w-full"></span>
                </a>
            </li>
        </ul>
    </nav>
</template>