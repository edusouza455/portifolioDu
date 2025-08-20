<template>
  <div class="bg-zinc-800 text-white min-h-screen flex flex-col">
    <div class="flex-1">
      <div class="max-w-6xl mx-auto px-4 py-6 flex flex-col gap-8">
        <HeaderAppHeader/>
        <transition name="fade-up">
          <HeroSection v-if="show"/>
        </transition>
      </div>
      <transition name="fade-up">
        <div v-if="show" class="w-full bg-zinc-700 py-5 rounded-xl">
          <div class="max-w-6xl mx-auto w-full flex flex-col md:flex-row md:gap-20 p-5 justify-center items-center">
            <AboutSection/>
            <BoxSkills/>
          </div>
        </div>

      </transition>
    </div>
    <AppFooter/>
  </div>
</template>

<script  setup>
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