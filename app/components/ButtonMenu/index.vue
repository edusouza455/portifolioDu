<template>
  <div>
    <button @click="menuOpen = !menuOpen" class="focus:outline-none" aria-label="Abrir menu">
      <Icon
        name="meteor-icons:bars"
        class="w-7 h-7 text-white transition-transform duration-200 hover:scale-110"
      />
    </button>

    <transition name="fade">
      <nav
        v-if="menuOpen"
        class="fixed inset-0 bg-black/60 backdrop-blur-xs flex items-center justify-center z-50"
        @click.self="menuOpen = false"
      >
        <div class="bg-zinc-800 border border-zinc-700 rounded-2xl shadow-2xl py-8 px-8 flex flex-col items-center gap-5 w-4/5 max-w-xs text-white">
          <a @click="menuOpen = false" href="#sobre" class="text-base font-medium hover:text-sky-300 transition">Sobre</a>
          <a @click="menuOpen = false" href="#servicos" class="text-base font-medium hover:text-sky-300 transition">Meus Serviços</a>
          <a @click="menuOpen = false" href="#skills" class="text-base font-medium hover:text-sky-300 transition">Skills</a>
          <a href="https://github.com/edusouza455" target="_blank" rel="noopener noreferrer" class="text-base font-medium hover:text-sky-300 transition">Projetos</a>
          <a
            href="https://wa.me/5595981153371?text=Ol%C3%A1%20Eduardo!%20Vi%20seu%20portf%C3%B3lio%20e%20gostaria%20de%20conversar."
            target="_blank"
            rel="noopener noreferrer"
            class="w-full text-center py-2.5 px-4 rounded-lg bg-sky-500/20 text-sky-300 border border-sky-400/30 font-semibold hover:bg-sky-500/30 transition"
          >
            Falar no WhatsApp
          </a>
          <button @click="menuOpen = false" class="mt-2 text-xs text-gray-400 hover:text-white">Fechar</button>
        </div>
      </nav>
    </transition>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const menuOpen = ref(false)
</script>

<style scoped>
</style>
