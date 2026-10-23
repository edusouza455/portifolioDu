<template>
  <div class="bg-zinc-800 text-white min-h-screen flex flex-col">
    <div class="flex-1">
      <div class="max-w-6xl mx-auto px-4 py-6 flex flex-col gap-10">
        <HeaderAppHeader />

        <transition name="fade-up">
          <div v-if="show" class="flex flex-col gap-10">
            <!-- Cartão de Visitas Principal (Hero) -->
            <HeroSection />

            <!-- Seção Meus Serviços e Tipos de Testes -->
            <ServicesSection />

            <!-- Seção Sobre & Hard Skills -->
            <div class="w-full bg-zinc-700/60 border border-zinc-700 py-8 px-5 md:px-8 rounded-2xl shadow-lg">
              <div class="max-w-6xl mx-auto w-full grid grid-cols-1 lg:grid-cols-2 gap-8 items-stretch">
                <AboutSection />
                <BoxSkills />
              </div>
            </div>

            <!-- Cartão de Contato Rápido (CTA) -->
            <section class="w-full bg-zinc-700/50 border border-sky-400/30 rounded-2xl p-6 md:p-8 flex flex-col md:flex-row items-center justify-between gap-6">
              <div class="text-center md:text-left">
                <h2 class="text-xl md:text-2xl font-bold text-white mb-1">
                  Precisa garantir a qualidade do seu software?
                </h2>
                <p class="text-sm md:text-base text-gray-300">
                  Vamos conversar sobre como estruturar testes automatizados, validar APIs ou elevar a confiabilidade das suas entregas.
                </p>
              </div>
              <div class="flex flex-wrap items-center justify-center gap-3 shrink-0">
                <a
                  href="https://wa.me/5595981153371?text=Ol%C3%A1%20Eduardo!%20Vi%20seu%20portf%C3%B3lio%20e%20gostaria%20de%20conversar."
                  target="_blank"
                  rel="noopener noreferrer"
                  class="inline-flex items-center gap-2 px-5 py-3 rounded-xl bg-sky-400 text-zinc-900 font-semibold text-sm hover:bg-sky-300 transition-all shadow-md"
                >
                  <Icon name="codicon:comment-discussion" class="w-4 h-4" />
                  Chamar no WhatsApp
                </a>
                <a
                  href="https://www.linkedin.com/in/edu-souza-367289292/"
                  target="_blank"
                  rel="noopener noreferrer"
                  class="inline-flex items-center gap-2 px-5 py-3 rounded-xl bg-zinc-800 border border-zinc-600 hover:border-sky-400/50 text-white font-medium text-sm transition-all"
                >
                  <Icon name="skill-icons:linkedin" class="w-4 h-4" />
                  Conectar no LinkedIn
                </a>
              </div>
            </section>
          </div>
        </transition>
      </div>
    </div>

    <AppFooter />
  </div>
</template>

<script setup>
import { ref, onMounted } from 'vue'

const show = ref(false)

onMounted(() => {
  show.value = true
})
</script>

<style scoped>
.fade-up-enter-active {
  transition: opacity 0.7s cubic-bezier(.4,0,.2,1), transform 0.7s cubic-bezier(.4,0,.2,1);
}
.fade-up-enter-from {
  opacity: 0;
  transform: translateY(40px);
}
.fade-up-enter-to {
  opacity: 1;
  transform: translateY(0);
}
</style>
