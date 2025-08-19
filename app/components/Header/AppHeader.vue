<template>
  <header class="w-full flex flex-col md:flex-row items-center justify-between gap-4 md:gap-0 relative">
    <h1 class="text-2xl md:text-3xl font-bold mb-2 md:mb-0">Eduardo Souza</h1>
    <nav class="hidden md:flex flex-row space-x-6 items-center">
      <a href="https://github.com/edusouza455" class="hover:underline transition-transform duration-200 hover:scale-110">Projetos</a>
      <a href="https://www.linkedin.com/in/edu-souza-367289292/" class="hover:underline transition-transform duration-200 hover:scale-110">Contato</a>
    </nav>
  <div class="md:hidden relative">
      <button @click="menuOpen = !menuOpen" class="focus:outline-none">
        <svg class="w-8 h-8 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"></path>
        </svg>
      </button>
      <transition name="fade">
        <nav v-if="menuOpen" class="fixed inset-0 bg-black bg-opacity-40 flex items-center justify-center z-50">
          <div class="bg-white rounded-xl shadow-2xl py-8 px-10 flex flex-col items-center gap-6 w-4/5 max-w-xs">
            <a href="https://github.com/edusouza455" class="text-zinc-800 text-lg font-semibold hover:text-blue-600 transition mb-2">Projetos</a>
            <a href="https://www.linkedin.com/in/edu-souza-367289292/" class="text-zinc-800 text-lg font-semibold hover:text-blue-600 transition">Contato</a>
            <button @click="menuOpen = false" class="mt-4 text-sm text-blue-500 hover:underline">Fechar</button>
          </div>
        </nav>
      </transition>
    </div>
  </header>
</template>

<script lang="ts">
import { ref } from 'vue';
export default {
  setup() {
    const menuOpen = ref(false);
    return { menuOpen };
  }
}
</script>

<style scoped>
.fade-enter-active, .fade-leave-active {
  transition: opacity 0.2s;
}
.fade-enter-from, .fade-leave-to {
  opacity: 0;
}
</style>