<script>
export default {
    data() {
        return {
            
        }
    }
}
</script>

<template>
    <footer class="w-full h-auto bg-primario mt-12 p-8 flex justify-around gap-8 rounded-t-4xl">
        <div class="flex flex-col gap-6">
            <h2 class="text-5xl font-bold text-secundario mb-2">Contacto</h2>

            <div class="flex items-center gap-4 text-secundario/90 hover:text-white transition-colors duration-300">
                <span class="icon-[mdi-light--email] text-3xl"></span>
                <span class="text-xl">sergiobenavides780@gmail.com</span>
            </div>

            <div class="flex items-center gap-4 text-secundario/90 hover:text-white transition-colors duration-300">
                <span class="icon-[mdi-light--phone] text-3xl"></span>
                <span class="text-xl">314 880 2292</span>
            </div>
        </div>

        <form action="" class="flex flex-col gap-4 w-1/3 bg-secundario/10 p-6 rounded-2xl backdrop-blur-sm">
            <h3 class="text-2xl font-bold text-secundario mb-2">Envíame un mensaje</h3>
            <input type="text" placeholder="Nombre"
                class="p-3 bg-secundario/20 border-2 border-transparent focus:border-secundario rounded-xl text-secundario placeholder-secundario/60 outline-none transition-all duration-300">
            <input type="email" placeholder="Email"
                class="p-3 bg-secundario/20 border-2 border-transparent focus:border-secundario rounded-xl text-secundario placeholder-secundario/60 outline-none transition-all duration-300">
            <textarea name="" id="" cols="30" rows="4" placeholder="Mensaje"
                class="p-3 bg-secundario/20 border-2 border-transparent focus:border-secundario rounded-xl text-secundario placeholder-secundario/60 outline-none transition-all duration-300 resize-none"></textarea>
            <button
                class="p-3 bg-secundario text-primario font-bold rounded-xl hover:bg-white transition-colors duration-300 shadow-lg">Enviar</button>
        </form>
    </footer>
</template>