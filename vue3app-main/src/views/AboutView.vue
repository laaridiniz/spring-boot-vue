<template>
  <div class="about">
  <h1>Bem vindo {{ nome }}</h1>
  <label for="nome">Nome: </label>
  <input id="nome" type="text" v-model="nome"/>
  <label for="senha">Senha: </label>
  <input id="senha" type="password" v-model="senha"/>
  <button @click="cadastrar">Cadastrar</button>
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

const nome = ref("Nome");
const senha = ref("123");
const usuarios = ref();

async function atualizar() {
  usuarios.value = (await axios.get("usuario")).data;
}

async function cadastrar() {
  await axios.post("usuario",
  {
    nome: nome.value,
    senha: senha.value
  });
  atualizar();
}

onMounted(() => {
  atualizar();
});
</script>