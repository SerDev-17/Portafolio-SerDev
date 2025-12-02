<script>
export default {
    data() {
        return {
            skills: [
                'UX Design',
                'App Design',
                'Dashboard',
                'Wireframe',
                'User Research',
                'HTML',
                'CSS',
                'JavaScript',
                'Vue.js',
                'PHP',
                'Python',
                'MySQL',
                'Tailwind CSS',
                'Responsive Design',
                'UI/UX',
                'Frontend Development',
                'Backend Development',
                'Web Design',
                'Landing Pages'
            ]
        }
    }
}
</script>

<template>
    <section class="relative w-full bg-primario py-8 overflow-hidden rotate-359 rounded-xl">
        <div class="relative flex">
            <div class="flex items-center gap-8 animate-scroll whitespace-nowrap">
                <template v-for="(skill, index) in skills" :key="`skill-1-${index}`">
                    <span class="text-2xl font-bold text-secundario/90">{{ skill }}</span>
                    <span class="text-3xl text-secundario/40">✦</span>
                </template>
            </div>

            <div class="flex items-center gap-8 animate-scroll whitespace-nowrap" aria-hidden="true">
                <template v-for="(skill, index) in skills" :key="`skill-2-${index}`">
                    <span class="text-2xl font-bold text-secundario/90">{{ skill }}</span>
                    <span class="text-3xl text-secundario/40">✦</span>
                </template>
            </div>
        </div>
    </section>
</template>

<style scoped>
@keyframes scroll {
    0% {
        transform: translateX(0);
    }

    100% {
        transform: translateX(-100%);
    }
}

.animate-scroll {
    animation: scroll 40s linear infinite;
}

section:hover .animate-scroll {
    animation-play-state: paused;
}
</style>
