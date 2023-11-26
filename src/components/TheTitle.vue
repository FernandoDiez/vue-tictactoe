<script setup lang="ts">
defineProps<{
  title: string,
  subtitle: string
}>()
</script>

<template>
  <header>
    <div class="header">
      <h1>{{ title }}</h1>
      <h2>{{ subtitle }}</h2>
    </div>
  </header>
</template>

<style scoped>
h1,
h2 {
  text-align: center;
}
</style>