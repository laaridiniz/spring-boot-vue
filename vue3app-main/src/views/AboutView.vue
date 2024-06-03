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
import { ref } from 'vue';
const nome = ref("Cha Eun Woo");

const usuarios = ref([
{ id: 1, nome: "usuario 1", senha: "123" },
{ id: 2, nome: "usuario 2", senha: "456" }
]);

</script>