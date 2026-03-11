<template>
  <div class="flex flex-col items-center w-full">
    <h2 class="text-xl md:text-2xl font-semibold mb-4 text-center">Hard Skills</h2>
    <section class="flex flex-wrap justify-center gap-4 md:gap-6">
      <template v-for="name in icons" :key="name">
        <!-- devicon items get a rounded bg to match other icons -->
        <div
          v-if="isDevicon(name)"
          class="w-10 h-10 md:w-12 md:h-12 flex items-center justify-center rounded-md bg-gray-100 dark:bg-gray-800 transition-transform duration-200 hover:scale-110"
          :title="getTitle(name)"
          :aria-label="getTitle(name)"
        >
          <Icon :name="name" class="w-6 h-6 md:w-8 md:h-8 text-black dark:text-white" />
        </div>

        <!-- normal icons keep the existing rendering -->
        <Icon
          v-else
          :name="name"
          :class="iconClass"
          :title="getTitle(name)"
          :aria-label="getTitle(name)"
        />
      </template>
    </section>
  </div>
</template>

<script setup>
const icons = [
  'devicon:playwright',
  'devicon:pytest',
  'skill-icons:javascript',
  'skill-icons:python-dark',
  'skill-icons:postgresql-dark',
  'skill-icons:docker',
  'skill-icons:postman',
  'skill-icons:linux-dark',
  'skill-icons:githubactions-dark',
  
]

const iconClass = 'w-10 h-10 md:w-12 md:h-12 text-black transition-transform duration-200 hover:scale-110'

function getTitle(name) {
  // retorna apenas o texto após ':' e remove sufixos como -dark
  const parts = name.split(':')
  let title = parts.length > 1 ? parts[1] : parts[0]
  title = title.replace(/-dark|-light|-wordmark$/i, '')
  // ajustar nomes conhecidos
  if (title.toLowerCase() === 'postgresql') title = 'PostgreSQL'
  if (title.toLowerCase() === 'javascript') title = 'JavaScript'
  if (title.toLowerCase() === 'vuejs') title = 'Vue.js'
  return title.charAt(0).toUpperCase() + title.slice(1)
}

function isDevicon(name) {
  return name && name.split(':')[0].toLowerCase() === 'devicon'
}
</script>

<style scoped>

</style>