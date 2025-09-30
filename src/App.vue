<template>
  <div id="app">
    <HeaderComponent />

    <SectionComponent title="Sobre Mim" :items="aboutMe" type="about" />

    <SectionComponent title="Experiência Profissional" :items="experiences" type="experience" />

    <SectionComponent title="Educação" :items="education" type="education" />

    <SectionComponent title="Habilidades" :items="skills" type="skills" />

    <SectionComponent title="Projetos (Opcional)" :items="projects" type="experience" />

  </div>
</template>

<script setup>
import { ref } from 'vue';
import HeaderComponent from './components/HeaderComponent.vue';
import SectionComponent from './components/SectionComponent.vue';

const aboutMe = ref(
  "Desenvolvedor com 2 anos de experiência em estágios criando aplicações web do zero, API's e integrando software com outras tecnologias."
);

const experiences = ref([
  {
    title: 'Estágio desenvolvedor Back-end PHP',
    subtitle: 'MP-MS | Campo Grande, MS',
    date: 'Jun 2025 – Presente',
    description: [
      'Desenvolvimento e manutenção de aplicações web utilizando PHP com Laravel, Keycloak e MongoDB.',
      'Desenvolvimento de scripts em python para gerenciamento e troubleshoot via API dos firewalls'
    ]
  },
  {
    title: 'Estágio Suporte',
    subtitle: 'TRE-MS | Campo Grande, MS',
    date: 'Jan 2025 – Jun 2025',
    description: [
      'Levantamento e gerenciamento de ativos',
      'Estudo em ferramentas de BI - Looker Studio'
    ]
  },
  {
    title: 'Estágio desenvolvedor Back-end C#',
    subtitle: 'CREA-MS | Campo Grande, MS',
    date: 'Jan 2022 – Jul 2022',
    description: [
      'Desenvolvimento e manutenção de aplicações web utilizando C# com Entity Framwork, Blazor e MySQL.',
      'Desenvolver casos de uso e casos de teste.',
      'Desenvolvimento de aplicação utilizando conceitos SOLID, DDD e Clean Architecture',
      'Suporte técnico geral'
    ]
  }
]);

const education = ref([
  {
    title: 'Cursando Análise e Desenvolvimento de Sistemas',
    subtitle: 'Universidade Católica Dom Bosco',
    date: '2023 – 2026',
    description: null
  },
  {
    title: 'Cursando Ciência de Dados',
    subtitle: 'UFMS',
    date: '2023 – 2026',
    description: null
  }
]);

const skills = ref([
  'HTML5', 'CSS3', 'JavaScript (ES6+)', 'Vue.js', 'Node.js',
  'Git', 'GitHub', 'RESTful APIs', 'DDD', 'C#', 'PHP', 'Laravel'
]);

const projects = ref([
  {
    title: 'Minha Plataforma de E-commerce',
    subtitle: 'Projeto faculdade',
    linkText: 'Ver no GitHub',
    linkUrl: 'https://github.com/arthurdronov/simple-ecommerce',
    date: '2023',
    description: [
      'Plataforma de e-commerce completa construída com Vue.js e um backend Node.js (API simulada).',
      'Funcionalidades: carrinho de compras, autenticação de usuário, listagem de produtos e filtros.'
    ]
  },
  {
    title: 'Plataforma de Minigame Quiz',
    subtitle: 'Projeto Pessoal',
    linkText: 'Ver no GitHub',
    linkUrl: 'https://github.com/arthurdronov/Quiz1',
    date: '2023',
    description: [
      'Plataforma construída com C# e blazor.',
      'Funcionalidades: Cadastro de usuário, autenticação de usuário, Perfil de usuário, cadastro de quiz, gerenciamento de quiz, pontuação.'
    ]
  },
  {
    title: 'Portfólio Pessoal',
    subtitle: 'Este site',
    linkText: 'Ver no GitHub',
    linkUrl: 'https://github.com/arthurdronov/web-curriculo',
    date: '2022',
    description: [
      'Desenvolvimento de um portfólio para exibir projetos e habilidades.'
    ]
  }
]);
</script>

<style>
</style>