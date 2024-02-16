<script setup lang="ts">
import { ref } from 'vue';
import TheTitle from './components/TheTitle.vue';
import ThePlayersVue from './components/ThePlayers.vue';

const title: string = "TIC TAC TOE";
const subtitle: string = "By Fernando Diez";

const counter = ref(0);
const xPlayer = ref('Candela');
const oPlayer = ref('Alejandra');

const sumaUno = (cant: number) => {
  counter.value += cant;
}

const nameX = (name: string) => {
  xPlayer.value = name;
}
</script>

<template>
  <TheTitle :title="title" :subtitle="subtitle" />
  <ThePlayersVue :xPlayer="xPlayer" :oPlayer="oPlayer" :counter="counter" @sumaUno="sumaUno" @nameX="nameX" />
</template>
