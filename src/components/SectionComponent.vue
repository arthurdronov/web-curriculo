<template>
  <section class="section">
    <h2>{{ title }}</h2>
    <div v-if="type === 'experience' || type === 'education'">
      <div v-for="(item, index) in items" :key="index" class="item">
        <h3>{{ item.title }}</h3>
        
        <p>
          {{ item.subtitle }}
          <span v-if="item.linkUrl">
            | <a :href="item.linkUrl" target="_blank" rel="noopener noreferrer">{{ item.linkText || 'Link' }}</a>
          </span>
        </p>
        
        <p v-if="item.date">{{ item.date }}</p>
        <ul v-if="item.description">
          <li v-for="(desc, dIndex) in item.description" :key="dIndex">{{ desc }}</li>
        </ul>
      </div>
    </div>
    <div v-else-if="type === 'skills'" class="skills-grid">
      <span v-for="(skill, index) in items" :key="index" class="skill-tag">{{ skill }}</span>
    </div>
    <div v-else-if="type === 'about'">
      <p>{{ items }}</p>
    </div>
  </section>
</template>

<script setup>
import { defineProps } from 'vue';

const props = defineProps({
  title: {
    type: String,
    required: true
  },
  items: {
    type: [Array, String],
    required: true
  },
  type: {
    type: String,
    default: 'experience'
  }
});
</script>

<style scoped>
.item p {
  margin-top: 4px;
  margin-bottom: 4px;
}
</style>