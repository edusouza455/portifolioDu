<template>
  <section class="w-full flex flex-col md:flex-row items-center gap-8 md:gap-20 justify-center text-white">
    <NuxtImg 
      src="/edu.jpg"
      alt="era pra ter um edu aqui"
      width="180"
      height="180"
      class="rounded-xl shadow-lg mb-4 md:mb-0 transition-transform duration-200 hover:scale-110'"
    />
  <div class="p-4 md:p-10 w-full md:w-auto flex flex-col items-center">
      <h1 class="text-2xl md:text-3xl font-bold mb-2">Eduardo Souza</h1>
      <p class="text-base md:text-lg text-white mb-4 text-justify">
        Engenheiro de QA formado em ADS, especializado em automação de testes utilizando 
        <span class="text-sky-300 font-semibold">Playwright</span>, 
        <span class="text-sky-300 font-semibold">Python (Pytest)</span> e 
        <span class="text-sky-300 font-semibold">TypeScript</span>. 
        Com background em desenvolvimento, aplico uma visão técnica profunda para garantir a qualidade e a performance de interfaces modernas.<br>
        Além da automação, possuo domínio em 
        <span class="text-sky-300 font-semibold">CI/CD</span> e 
        <span class="text-sky-300 font-semibold">Docker</span>, 
        o que me permite integrar testes contínuos em pipelines escaláveis e garantir entregas de software robustas e confiáveis.
      </p>
      <div class="flex space-x-4 justify-center">
        <a href="https://github.com/edusouza455" target="_blank">
          <Icon name="pajamas:github" class="w-8 h-8 text-white transition-transform duration-200 hover:scale-110" />
        </a>
        <a href="https://www.linkedin.com/in/edu-souza-367289292/" target="_blank">
          <Icon name="skill-icons:linkedin" class="w-8 h-8 transition-transform duration-200 hover:scale-110" />
        </a>
      </div>
    </div>
  </section>
</template>

<script>
</script>

<style scoped>

</style>