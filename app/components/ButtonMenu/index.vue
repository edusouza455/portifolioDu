<template>
  <div>
      <button @click="menuOpen = !menuOpen" class="focus:outline-none">
        <Icon name="meteor-icons:bars" 
          class="w-8 h-8 md:w-12 md:h-12 text-white transition-transform duration-200 hover:scale-110" />
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
</template>

<script setup>
import { ref } from 'vue'

  const menuOpen = ref(false)

</script>

<style lang="scss" scoped>

</style>