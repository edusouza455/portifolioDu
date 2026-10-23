<template>
  <section id="servicos" class="w-full py-4">
    <div class="flex flex-col items-center text-center mb-8">
      <span class="text-xs font-semibold uppercase tracking-wider text-sky-300 mb-1">
        Como posso ajudar seu projeto ou equipe
      </span>
      <h2 class="text-2xl md:text-3xl font-bold text-white mb-2">
        Meus Serviços de QA &amp; Testes
      </h2>
      <p class="text-sm md:text-base text-gray-300 max-w-2xl">
        Soluções completas de Engenharia de Qualidade para garantir entregas estáveis, rápidas e seguras em todas as camadas da sua aplicação.
      </p>
    </div>

    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-5">
      <div
        v-for="service in services"
        :key="service.title"
        class="bg-zinc-700/60 border border-zinc-600/70 hover:border-sky-400/50 rounded-2xl p-6 flex flex-col justify-between transition-all duration-200 hover:-translate-y-1 shadow-lg"
      >
        <div>
          <div class="w-11 h-11 rounded-xl bg-zinc-800 border border-sky-400/30 flex items-center justify-center mb-4">
            <Icon :name="service.icon" class="w-6 h-6 text-sky-300" />
          </div>

          <h3 class="text-lg font-bold text-white mb-2">
            {{ service.title }}
          </h3>

          <p class="text-sm text-gray-300 leading-relaxed mb-4">
            {{ service.description }}
          </p>
        </div>

        <div class="flex flex-wrap gap-1.5 pt-3 border-t border-zinc-600/60">
          <span
            v-for="item in service.highlights"
            :key="item"
            class="text-xs px-2.5 py-0.5 rounded-md bg-zinc-800 text-sky-300 font-medium"
          >
            {{ item }}
          </span>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const services = [
  {
    icon: 'codicon:beaker',
    title: 'Automação de Testes E2E (Web & Mobile)',
    description:
      'Desenvolvimento e manutenção de suítes automatizadas escaláveis para interfaces Web e aplicativos Android, reduzindo o tempo de validação manual e prevenindo regressões.',
    highlights: ['Playwright', 'Selenium', 'Pytest', 'Appium (Android)']
  },
  {
    icon: 'codicon:symbol-interface',
    title: 'Testes Integrados & Validação de APIs',
    description:
      'Validação avançada de regras de negócio no back-end, contratos de APIs REST, status codes, payloads, segurança e integridade de dados diretamente via banco SQL.',
    highlights: ['Java', 'RestAssured', 'Postman', 'SQL']
  },
  {
    icon: 'codicon:checklist',
    title: 'Testes Funcionais, Regressivos & Exploratórios',
    description:
      'Planejamento, mapeamento e execução estruturada de cenários de testes baseados nas boas práticas do ISTQB (CTFL), cobrindo fluxos críticos, usabilidade e bordas.',
    highlights: ['Funcionais', 'Regressivos', 'Exploratórios', 'Usabilidade']
  },
  {
    icon: 'codicon:dashboard',
    title: 'Testes de Performance, Carga & Estresse',
    description:
      'Simulação de múltiplos usuários simultâneos para identificar gargalos, avaliar tempo de resposta e garantir estabilidade sob alta demanda em produção.',
    highlights: ['JMeter', 'Grafana', 'Análise de Gargalos', 'Estabilidade']
  },
  {
    icon: 'codicon:layers-active',
    title: 'Gestão de Qualidade, Requisitos & STLC',
    description:
      'Liderança técnica de QA, refinamento de Histórias de Usuário (BDD/Critérios de Aceite), rastreabilidade completa de cobertura e gestão rigorosa do ciclo de defeitos.',
    highlights: ['Jira & Xray', 'Azure DevOps', 'Refinamento', 'Scrum / Kanban']
  },
  {
    icon: 'codicon:rocket',
    title: 'CI/CD, Relatórios & QA com IA',
    description:
      'Integração de testes contínuos em pipelines DevOps com containers Docker, relatórios gerenciais detalhados e uso de Inteligência Artificial para otimizar cenários e documentação.',
    highlights: ['CI/CD', 'Docker', 'Allure Reports', 'IA aplicada a QA']
  }
]
</script>

<style scoped>
</style>
