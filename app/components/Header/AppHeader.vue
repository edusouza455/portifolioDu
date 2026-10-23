<template>
  <header class="w-full flex flex-row items-center justify-between py-2 relative border-b border-zinc-700/70 pb-4">
    <div class="flex items-center gap-3">
      <NuxtImg 
        src="/logo.jpg"
        alt="Eduardo Souza Logo"
        width="56"
        height="56"
        class="rounded-full ring-2 ring-sky-400/30 transition-transform duration-200 hover:scale-105"
      />
      <div class="flex flex-col">
        <span class="font-bold text-white text-base md:text-lg leading-tight">Eduardo Souza</span>
        <span class="text-xs text-sky-300 font-medium">QA Automation Engineer / SDET • CTFL</span>
      </div>
    </div>

    <nav class="hidden md:flex flex-row space-x-6 items-center text-sm font-medium text-gray-200">
      <a href="#sobre" class="hover:text-sky-300 transition-colors">Sobre</a>
      <a href="#servicos" class="hover:text-sky-300 transition-colors">Meus Serviços</a>
      <a href="#skills" class="hover:text-sky-300 transition-colors">Skills</a>
      <a href="https://github.com/edusouza455" target="_blank" rel="noopener noreferrer" class="hover:text-sky-300 transition-colors">Projetos</a>
      <a
        href="https://wa.me/5595981153371?text=Ol%C3%A1%20Eduardo!%20Vi%20seu%20portf%C3%B3lio%20e%20gostaria%20de%20conversar."
        target="_blank"
        rel="noopener noreferrer"
        class="px-4 py-2 rounded-lg bg-sky-500/15 text-sky-300 border border-sky-400/30 hover:bg-sky-500/25 transition-all"
      >
        Entrar em Contato
      </a>
    </nav>

    <div class="md:hidden relative">
      <ButtonMenu />
    </div>
  </header>
</template>

<script setup>
</script>

<style scoped>
.fade-enter-active, .fade-leave-active {
  transition: opacity 0.2s;
}
.fade-enter-from, .fade-leave-to {
  opacity: 0;
}
</style>
