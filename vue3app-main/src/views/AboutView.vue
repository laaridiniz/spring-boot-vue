<template>
  <div class="about">
  <h1>Bem vindo {{ nome }}</h1>
  <input type="text" v-model="nome"/>
  <p v-if="nome.length > 5">Nome grande</p>
  <p v-else>Nome pequeno</p>
  <table>
    <thead>
      <td>Id</td>
      <td>Nome</td>
    </thead>
    <tr v-for="usuario in usuarios" :key="usuario.id">
      <td>{{ usuario.id }}</td>
      <td>{{ usuario.nome }}</td>
    </tr>
  </table>
  </div>
</template>

<script setup lang="ts">
import { onMounted,ref } from 'vue';
import axios from 'axios';
const nome = ref("Cha Eun Woo");
const usuarios = ref();
async function atualizar () {
  usuarios.value = (await axios.get("https://8080-mineda.gitpod.io/usuario")).data;
}
onMounted(() => {
  atualizar();
});
</script>