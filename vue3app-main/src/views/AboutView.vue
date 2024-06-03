<template>
  <div class="about">
  <h1>Bem vindo {{ nome }}</h1>
  <input type="text" v-model="nome"/>
  <p v-if="nome.length > 5">Nome grande</p>
  <p v-else>Nome pequeno</p>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';
const nome = ref("Cha Eun Woo");
</script>