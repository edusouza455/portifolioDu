<template>
  <div class="w-full flex flex-col items-center">
  <section class="bg-zinc-700 rounded-xl p-6 w-full">
    <h2 class="text-xl md:text-2xl font-bold mb-3 text-center">{{ $t('about.title') }}</h2>
    <p class="text-base md:text-lg text-gray-200 text-justify leading-relaxed">
      {{ $t('about.p1_start') }} <span class="font-semibold text-blue-300">{{ $t('about.role_company') }}</span>, {{ $t('about.p1_end') }}<br>
      {{ $t('about.p2_start') }} <span class="font-semibold text-blue-300">Django</span> {{ $t('about.p2_mid') }} <span class="font-semibold text-blue-300">VUE.js</span> {{ $t('hero.and') }} <span class="font-semibold text-blue-300">TypeScript</span>. {{ $t('about.p2_end') }}<br>
      {{ $t('about.p3_start') }} <span class="font-semibold text-blue-300">Docker</span> {{ $t('about.p3_end') }}
    </p>
  </section>
</div>
</template>

<script>
</script>

<style scoped>

</style>
