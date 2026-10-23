<template>
  <div id="skills" class="flex flex-col items-center w-full">
    <section class="bg-zinc-800/60 border border-zinc-600/50 rounded-2xl p-6 md:p-8 w-full flex flex-col items-center">
      <h2 class="text-xl md:text-2xl font-bold mb-2 text-center text-white">Hard Skills &amp; Ferramentas</h2>
      <p class="text-xs md:text-sm text-gray-400 mb-6 text-center">
        Stack técnica para automação, validação de APIs, mobile, performance e CI/CD
      </p>

      <div class="flex flex-wrap justify-center gap-3 md:gap-4 mb-6">
        <template v-for="name in icons" :key="name">
          <div
            v-if="isDevicon(name)"
            class="w-11 h-11 md:w-12 md:h-12 flex items-center justify-center rounded-lg bg-zinc-700 border border-zinc-600 transition-transform duration-200 hover:scale-110 hover:border-sky-400/50"
            :title="getTitle(name)"
            :aria-label="getTitle(name)"
          >
            <Icon :name="name" class="w-6 h-6 md:w-7 md:h-7 text-white" />
          </div>

          <Icon
            v-else
            :name="name"
            :class="iconClass"
            :title="getTitle(name)"
            :aria-label="getTitle(name)"
          />
        </template>
      </div>

      <div class="flex flex-wrap justify-center gap-2 pt-4 border-t border-zinc-700 w-full">
        <span
          v-for="tag in extraSkills"
          :key="tag"
          class="px-3 py-1 rounded-lg bg-zinc-700/80 border border-zinc-600 text-xs font-medium text-gray-200 hover:border-sky-400/50 hover:text-sky-300 transition-colors"
        >
          {{ tag }}
        </span>
      </div>
    </section>
  </div>
</template>

<script setup>
const icons = [
  'devicon:playwright',
  'devicon:pytest',
  'devicon:selenium',
  'skill-icons:java-dark',
  'skill-icons:python-dark',
  'skill-icons:javascript',
  'skill-icons:postman',
  'skill-icons:docker',
  'skill-icons:postgresql-dark',
  'skill-icons:githubactions-dark',
  'skill-icons:git',
  'skill-icons:linux-dark'
]

const extraSkills = [
  'RestAssured',
  'Appium (Android)',
  'JMeter',
  'Jira & Xray',
  'Azure DevOps',
  'Allure Reports',
  'Grafana',
  'SQL',
  'IA para QA',
  'STLC / ISTQB',
  'Scrum & Kanban'
]

const iconClass = 'w-11 h-11 md:w-12 md:h-12 text-black transition-transform duration-200 hover:scale-110'

function getTitle(name) {
  const parts = name.split(':')
  let title = parts.length > 1 ? parts[1] : parts[0]
  title = title.replace(/-dark|-light|-wordmark$/i, '')
  if (title.toLowerCase() === 'postgresql') title = 'PostgreSQL'
  if (title.toLowerCase() === 'javascript') title = 'JavaScript'
  if (title.toLowerCase() === 'githubactions') title = 'GitHub Actions (CI/CD)'
  return title.charAt(0).toUpperCase() + title.slice(1)
}

function isDevicon(name) {
  return name && name.split(':')[0].toLowerCase() === 'devicon'
}
</script>

<style scoped>
</style>
