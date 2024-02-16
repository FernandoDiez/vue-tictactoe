<script setup lang="ts">
import { store } from '../store';

defineProps<{
  xPlayer: string,
  oPlayer: string,
  counter: number
}>()
const a = () => {
  console.log((document.getElementById('nameX') as HTMLDataElement).value)
}
</script>

<template>
  <div v-if="store.isPlaying">Estamos jugando</div>
  <div v-else>
    <div>¿Desea comenzar a jugar?</div>
    <h1>{{ xPlayer }}</h1>
    <h1>{{ oPlayer }}</h1>
    <h1>{{ counter }}</h1>
    <input id="nameX" :value="xPlayer" @input="$emit('nameX', ($event.currentTarget as HTMLInputElement).value)" />
    <button @click="$emit('sumaUno', 5)">SUM</button>
    <button @click="$emit('nameX', 'ferchito')">Cambia nombre</button>
    <button @click="a">Cambia nombre</button>
  </div>
</template>