<script setup>
import { ref } from 'vue'
const nome = ref('')
const email = ref('')
const senha = ref('')
const idade = ref('')
const enviar = ref(false)
</script>

<template>
  <header>
    <div class="info">
    <form @submit.prevent="">
      <h1>Preencha o Formulário</h1>
      <hr>
      <p>Nome:</p>
      <input type="text" v-model="nome" minlength="3" maxlength="20" placeholder="Digite seu nome"/>
      <p>Senha:</p>
      <input type="password" v-model="senha" placeholder="Digite sua senha"/>
      <p>Email:</p>
      <input type="email" v-model="email" placeholder="Digite seu email"/>
      <p>Idade:</p>
      <input type="number" v-model="idade" minlength="3" maxlength="60"/>
      <hr>
      <button type='submit' @click="enviar = !enviar">Enviar</button>
      <div v-if="enviar">SUCESSO!</div>
    </form>
    </div>
  </header>
</template>

<style scoped>

p {
  margin: 15px 15px 15px 15px;
  color: red;
  font-family: monospace;
}

button {
  font-weight: bold;
  border-radius: 4px;
  color: red;
  background-color: black;
  padding: 5px 10px;
  margin: 15px 15px 15px 15px;
  cursor: pointer;
}

h1 {
  color: rgb(255, 0, 0);
  font-weight: bold;
  font-size: 1.5em;
  font-family: monospace;
}
.info {
  background-color: rgb(31, 31, 31);
  padding: 20px 30px;
  color: rgb(183, 210, 219);
  border-radius: 10px;
  text-align: center;
  margin: 10px;
}

</style>
