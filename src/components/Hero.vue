<script>
export default {
    name: 'Hero'
}
</script>

<template>
    <section class="relative w-full py-8 overflow- left-15">
        <div class="z-10 text-left max-w-2xl px-8">
            <p class="text-2xl text-primario/80 mb-2 font-light">Hola, Soy</p>
            <h1 class="text-6xl md:text-7xl font-bold text-primario mb-6 leading-tight">Sergio Naranjo</h1>
            <p class="text-lg text-primario/70 leading-relaxed max-w-xl mb-8">
                desarrollador web creativo y comprometido en transformar ideas en experiencias digitales impactantes.
                Estoy listo para llevar tu proyecto al siguiente nivel. ¡Hablemos!
            </p>

            <div class="flex gap-4 flex-wrap mt-10">
                <a href="#contacto"
                    class="px-8 py-3 bg-primario text-secundario font-semibold rounded-full hover:bg-primario/90 transition-all duration-300 hover:scale-105 shadow-lg hover:shadow-xl">
                    Contáctame
                </a>
                <a href="/cv.pdf" download
                    class="px-8 py-3 bg-transparent border-2 border-primario text-primario font-semibold rounded-full hover:bg-primario hover:text-secundario transition-all duration-300 hover:scale-105">
                    Descargar CV
                </a>
            </div>
        </div>
    </section>
</template>
