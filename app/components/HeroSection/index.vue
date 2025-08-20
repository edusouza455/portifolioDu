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
        Desenvolvedor web formado em Análise e Desenvolvimento de Sistemas,
        especializado em front-end com
        <span class="text-sky-300 font-semibold">Vue.js</span>,
        <span class="text-sky-300 font-semibold">TypeScript</span> e
        <span class="text-sky-300 font-semibold">Tailwind CSS</span>.
        Possui experiência na construção de interfaces modernas, responsivas e focadas na experiência do usuário.<br>
        Além do front-end, tem conhecimentos em
        <span class="text-sky-300 font-semibold">Python/Django</span> e
        <span class="text-sky-300 font-semibold">Docker</span>,
        o que lhe permite colaborar em projetos full stack e ambientes de desenvolvimento escaláveis.
      </p>
      <div class="flex space-x-4 justify-center">
        <a href="https://github.com/seuusuario" target="_blank">
          <Icon name="pajamas:github" class="w-8 h-8 text-white transition-transform duration-200 hover:scale-110" />
        </a>
        <a href="https://linkedin.com/in/seuusuario" target="_blank">
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