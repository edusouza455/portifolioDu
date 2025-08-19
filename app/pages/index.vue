<template>
  <div class="bg-zinc-800 text-white min-h-screen flex flex-col">
    <div class="flex-1">
      <div class="max-w-6xl mx-auto px-4 py-6 flex flex-col gap-8">
        <HeaderAppHeader/>
        <HeroSection/>
      </div>
      <div class="w-full bg-zinc-700 py-5 rounded-xl">
        <div class="max-w-6xl mx-auto w-full flex flex-col md:flex-row md:gap-20 p-5 justify-center items-center">
          <AboutSection/>
          <BoxSkills/>
        </div>
      </div>
    </div>
    <AppFooter/>
  </div>
</template>

<script lang="ts">
export default {
  // ...
}

</script>

<style scoped>

</style>

<!--teste de conta-->