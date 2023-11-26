<script setup lang="ts">
import { store } from '../store';
defineProps<{
  xPlayer: string,
  oPlayer: string
}>()
</script>

<template>
  <div v-if="store.isPlaying">Estamos jugando</div>
  <div v-else>
    <div>¿Desea comenzar a jugar?</div>
    <!-- <input v-model="xPlayer" placeholder="Put your name for X">
    <input v-model="oPlayer" placeholder="Put your name for O"> -->
    <h1>{{ xPlayer }}</h1>
    <h1>{{ oPlayer }}</h1>
  </div>
</template>