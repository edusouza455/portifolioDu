<template>
  <header class="w-full flex flex-row md:flex-row items-center justify-between gap-4 md:gap-0 relative">
    <NuxtImg 
    src="/logo.jpg"
    alt="era pra ter um edu aqui"
    width="80"
    height="80"
    class="text-2xl md:text-3xl font-bold mb-2 md:mb-0 rounded-full transition-transform duration-200 hover:scale-110"/>
    <nav class="hidden md:flex flex-row space-x-6 items-center">
      <a href="https://github.com/edusouza455" class="hover:underline transition-transform duration-200 hover:scale-110">Projetos</a>
      <a href="https://www.linkedin.com/in/edu-souza-367289292/" class="hover:underline transition-transform duration-200 hover:scale-110">Contato</a>
    </nav>
  <div class="md:hidden relative">
      <ButtonMenu/>      
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