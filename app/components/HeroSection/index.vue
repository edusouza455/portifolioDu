<template>
  <section class="w-full bg-zinc-700/50 border border-zinc-700 rounded-2xl p-6 md:p-10 shadow-xl">
    <div class="flex flex-col md:flex-row items-center gap-8 md:gap-12 justify-between text-white">
      <div class="relative shrink-0">
        <NuxtImg 
          src="/edu.jpg"
          alt="Eduardo Coutinho de Souza"
          width="190"
          height="190"
          class="rounded-2xl shadow-lg ring-2 ring-sky-400/30 transition-transform duration-200 hover:scale-105 object-cover"
        />
        <span
          class="absolute -bottom-3 left-1/2 -translate-x-1/2 whitespace-nowrap px-3 py-1 rounded-full bg-zinc-800 border border-sky-400/40 text-sky-300 text-xs font-semibold shadow-md"
        >
          ISTQB® CTFL Certified
        </span>
      </div>

      <div class="w-full flex flex-col items-center md:items-start text-center md:text-left">
        <div class="flex flex-wrap items-center justify-center md:justify-start gap-2 mb-2">
          <span class="px-3 py-0.5 text-xs font-medium rounded-full bg-sky-500/15 text-sky-300 border border-sky-400/30">
            QA Automation Engineer / SDET
          </span>
          <span class="px-3 py-0.5 text-xs font-medium rounded-full bg-zinc-800 text-gray-300 border border-zinc-600">
            Manaus, AM • Remoto / Híbrido
          </span>
        </div>

        <h1 class="text-2xl md:text-4xl font-bold mb-3 tracking-tight">
          Eduardo Coutinho de Souza
        </h1>

        <p class="text-sm md:text-base text-gray-200 mb-6 leading-relaxed max-w-3xl">
          Especialista em Qualidade de Software e Automação de Testes (<span class="text-sky-300 font-semibold">CTFL - ISTQB</span>), pós-graduado em Engenharia de Software com foco em Qualidade e Testes. Atuo em todo o ciclo de vida de testes (<span class="text-sky-300 font-semibold">STLC</span>), combinando automação em <span class="text-sky-300 font-semibold">Java (RestAssured)</span>, <span class="text-sky-300 font-semibold">Python (Pytest)</span>, <span class="text-sky-300 font-semibold">Playwright</span>, <span class="text-sky-300 font-semibold">Selenium</span> e <span class="text-sky-300 font-semibold">Appium</span> com <span class="text-sky-300 font-semibold">Inteligência Artificial aplicada a QA</span> e pipelines de <span class="text-sky-300 font-semibold">CI/CD</span> para entregas rápidas, seguras e livres de regressões.
        </p>

        <div class="flex flex-wrap items-center justify-center md:justify-start gap-3 w-full">
          <a
            href="https://wa.me/5595981153371?text=Ol%C3%A1%20Eduardo!%20Vi%20seu%20portf%C3%B3lio%20e%20gostaria%20de%20conversar%20sobre%20seus%20servi%C3%A7os%20de%20QA."
            target="_blank"
            rel="noopener noreferrer"
            class="inline-flex items-center gap-2 px-5 py-2.5 rounded-xl bg-sky-400 text-zinc-900 font-semibold text-sm hover:bg-sky-300 transition-all shadow-md"
          >
            <Icon name="codicon:comment-discussion" class="w-4 h-4" />
            Contratar / WhatsApp
          </a>

          <a
            href="mailto:eduardosouza12pw@gmail.com"
            class="inline-flex items-center gap-2 px-4 py-2.5 rounded-xl bg-zinc-800 hover:bg-zinc-700 border border-zinc-600 text-gray-200 text-sm font-medium transition-all"
          >
            <Icon name="codicon:mail" class="w-4 h-4 text-sky-300" />
            eduardosouza12pw@gmail.com
          </a>

          <div class="flex items-center gap-3 ml-0 md:ml-2">
            <a
              href="https://github.com/edusouza455"
              target="_blank"
              rel="noopener noreferrer"
              title="GitHub"
              class="p-2 rounded-xl bg-zinc-800 border border-zinc-600 hover:border-sky-400/50 transition-transform duration-200 hover:scale-110"
            >
              <Icon name="pajamas:github" class="w-6 h-6 text-white" />
            </a>
            <a
              href="https://www.linkedin.com/in/edu-souza-367289292/"
              target="_blank"
              rel="noopener noreferrer"
              title="LinkedIn"
              class="p-2 rounded-xl bg-zinc-800 border border-zinc-600 hover:border-sky-400/50 transition-transform duration-200 hover:scale-110"
            >
              <Icon name="skill-icons:linkedin" class="w-6 h-6" />
            </a>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
</script>

<style scoped>
</style>
