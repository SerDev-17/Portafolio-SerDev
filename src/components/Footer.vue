<script>
import emailjs from '@emailjs/browser'

export default {
    data() {
        return {
            socialLinks: [
                {
                    name: 'Linkedin',
                    url: 'https://www.linkedin.com/in/sergio-benavides-780/',
                    icon: 'icon-[fa-brands--linkedin]'
                },
                {
                    name: 'Github',
                    url: 'https://github.com/SerDev-17',
                    icon: 'icon-[fa-brands--github]'
                },
                {
                    name: 'Instagram',
                    url: 'https://www.instagram.com/sergio_benavides_780/',
                    icon: 'icon-[fa-brands--instagram]'
                },
                {
                    name: 'Facebook',
                    url: 'https://www.facebook.com/sergio.benavides.780',
                    icon: 'icon-[fa-brands--facebook]'
                },
                {
                    name: 'Twitter',
                    url: 'https://twitter.com/SergioBenavides780',
                    icon: 'icon-[fa-brands--twitter]'
                }
            ],
            formData: {
                nombre: '',
                email: '',
                mensaje: ''
            },
            isSubmitting: false,
            submitMessage: '',
            submitStatus: '' // 'success' or 'error'
        }
    },
    methods: {
        async sendEmail(e) {
            e.preventDefault()

            // Validación básica
            if (!this.formData.nombre || !this.formData.email || !this.formData.mensaje) {
                this.submitMessage = 'Por favor completa todos los campos'
                this.submitStatus = 'error'
                setTimeout(() => {
                    this.submitMessage = ''
                    this.submitStatus = ''
                }, 3000)
                return
            }

            this.isSubmitting = true
            this.submitMessage = ''

            try {
                // IMPORTANTE: Reemplaza estos valores con tus credenciales de EmailJS
                const serviceID = 'service_5x3v80t' // Obtén esto de emailjs.com
                const templateID = 'template_5l1puyg' // Obtén esto de emailjs.com
                const publicKey = 'Y6IJOrWXNBiwnrZJz' // Obtén esto de emailjs.com

                const templateParams = {
                    from_name: this.formData.nombre,
                    from_email: this.formData.email,
                    message: this.formData.mensaje,
                    to_name: 'Gmail' // Tu nombre
                }

                await emailjs.send(serviceID, templateID, templateParams, publicKey)

                this.submitMessage = '¡Mensaje enviado correctamente!'
                this.submitStatus = 'success'

                // Limpiar formulario
                this.formData.nombre = ''
                this.formData.email = ''
                this.formData.mensaje = ''

            } catch (error) {
                console.error('Error al enviar el correo:', error)
                this.submitMessage = 'Error al enviar el mensaje. Intenta de nuevo.'
                this.submitStatus = 'error'
            } finally {
                this.isSubmitting = false

                // Limpiar mensaje después de 5 segundos
                setTimeout(() => {
                    this.submitMessage = ''
                    this.submitStatus = ''
                }, 5000)
            }
        }
    }
}
</script>

<template>
    <footer class="w-full h-auto bg-primario mt-12 p-8 flex justify-around gap-8 rounded-t-4xl" data-aos="zoom-in" data-aos-duration="1500">
        <div class="flex flex-col gap-6">
            <h2 class="text-5xl font-bold text-secundario mb-2">Contacto</h2>

            <div class="flex items-center gap-4 text-secundario/90 hover:text-white transition-colors duration-300">
                <span class="icon-[mdi-light--email] text-3xl"></span>
                <span class="text-xl">sergiobenavides780@gmail.com</span>
            </div>

            <div class="flex items-center gap-4 text-secundario/90 hover:text-white transition-colors duration-300">
                <span class="icon-[mdi-light--phone] text-3xl"></span>
                <span class="text-xl">+57 314 880 2292</span>
            </div>

            <div class="flex gap-4 mt-4">
                <a v-for="link in socialLinks" :key="link.name" :href="link.url" target="_blank"
                    class="group p-3 flex justify-center items-center rounded-full bg-secundario/10 hover:bg-secundario transition-all duration-300 hover:scale-110 shadow-md">
                    <span :class="link.icon"
                        class="text-2xl text-secundario group-hover:text-primario transition-colors duration-300"></span>
                </a>
            </div>
        </div>

        <form @submit="sendEmail"
            class="flex flex-col gap-4 w-1/3 bg-secundario/10 p-6 rounded-2xl backdrop-blur-sm relative">
            <h3 class="text-2xl font-bold text-secundario mb-2">Envíame un mensaje</h3>

            <input type="text" v-model="formData.nombre" placeholder="Nombre" :disabled="isSubmitting"
                class="p-3 bg-secundario/20 border-2 border-transparent focus:border-secundario rounded-xl text-secundario placeholder-secundario/60 outline-none transition-all duration-300 disabled:opacity-50">

            <input type="email" v-model="formData.email" placeholder="Email" :disabled="isSubmitting"
                class="p-3 bg-secundario/20 border-2 border-transparent focus:border-secundario rounded-xl text-secundario placeholder-secundario/60 outline-none transition-all duration-300 disabled:opacity-50">

            <textarea v-model="formData.mensaje" cols="30" rows="4" placeholder="Mensaje" :disabled="isSubmitting"
                class="p-3 bg-secundario/20 border-2 border-transparent focus:border-secundario rounded-xl text-secundario placeholder-secundario/60 outline-none transition-all duration-300 resize-none disabled:opacity-50"></textarea>

            <button type="submit" :disabled="isSubmitting"
                class="p-3 bg-secundario text-primario font-bold rounded-xl hover:bg-white transition-colors duration-300 shadow-lg disabled:opacity-50 disabled:cursor-not-allowed">
                {{ isSubmitting ? 'Enviando...' : 'Enviar' }}
            </button>

            <!-- Mensaje de feedback -->
            <div v-if="submitMessage"
                :class="['text-center p-2 rounded-lg transition-all duration-300',
                    submitStatus === 'success' ? 'bg-green-500/20 text-green-300' : 'bg-red-500/20 text-red-300']">
                {{ submitMessage }}
            </div>
        </form>
    </footer>
</template>