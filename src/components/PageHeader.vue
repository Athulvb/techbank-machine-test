<script setup lang="ts">
// Define props that this component accepts
interface Props {
  title: string
}

// Define props with TypeScript
defineProps<Props>()
</script>

<template>
  <header class="header">
    <h1>{{ title }}</h1>
    <p class="subtitle">A Vue.js Learning Example</p>
  </header>
</template>

<style scoped>
.header {
  text-align: center;
  padding: 2rem 0;
  border-bottom: 2px solid #42b883;
  margin-bottom: 2rem;
}

.header h1 {
  color: #2c3e50;
  margin: 0;
  font-size: 2.5rem;
}

.subtitle {
  color: #7f8c8d;
  margin: 0.5rem 0 0 0;
  font-size: 1.1rem;
}
</style>
