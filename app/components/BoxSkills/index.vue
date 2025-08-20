<template>
  <div class="flex flex-col items-center w-full">
    <h2 class="text-xl md:text-2xl font-semibold mb-4 text-center">Hard Skills</h2>

    <section class="flex flex-wrap justify-center gap-4 md:gap-6">
      <Icon v-for="icon in icons" :name= "icon.Icon"
      class="w-10 h-10 md:w-12 md:h-12 text-black transition-transform duration-200 hover:scale-110" />
    </section>
   
  </div>
</template>

<script setup>
import { ref } from 'vue'

  const icons = ref([
    {Icon:'skill-icons:vuejs-dark'},
    {Icon:'skill-icons:javascript'},
    {Icon:'skill-icons:python-dark'},
    {Icon:'skill-icons:tailwindcss-dark'},
    {Icon:'skill-icons:postgresql-dark'},
    {Icon:'skill-icons:docker'},
    {Icon:'skill-icons:linux-dark'},
    
  ])


  
</script>

<style>

</style>