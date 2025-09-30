<template>
  <header class="header">
    <h1>{{ name }}</h1>
    <p>{{ title }}</p>
    <p>{{ email }} | {{ phone }} | <a :href="linkedin" target="_blank">LinkedIn</a> | <a :href="github" target="_blank">GitHub</a></p>
  </header>
</template>

<script setup>
import { ref } from 'vue';

const name = ref('Arthur Chagas Dronov da Cruz');
const title = ref('Desenvolvedor Back-end');
const email = ref('arthurdronov@gmail.com');
const phone = ref('+55 67 99202-0232');
const linkedin = ref('https://www.linkedin.com/in/arthur-dronov-b37a32190/');
const github = ref('https://github.com/arthurdronov');
</script>

<style scoped>
</style>