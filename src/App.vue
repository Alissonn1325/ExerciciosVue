<script setup>
import { ref } from 'vue'
const nome = ref('')
const email = ref('')
const senha = ref('')
const confirmarSenha = ref('')
const idade = ref('')
const data = ref('')
const endereco = ref('')
const cidade = ref('')
const estado = ref('')
const hobbies = ref('')
const programacao = ref('')
const biografia = ref('')
const enviar = ref(false)
</script>

<template>
  <main class="main">
    <div class="info">
      <form @submit.prevent="">
        <h1>Preencha o Formulário</h1>
        <hr />
        <p>Nome:</p>
        <input type="text" v-model="nome" minlength="3" maxlength="20" placeholder="Nome" required/>
        <p>Email:</p>
        <input type="email" v-model="email" placeholder="Email" required />
        <p>Senha:</p>
        <input type="password" v-model="senha" placeholder="Senha" required />
        <p>Confirmar Senha:</p>
        <input type="password" v-model="confirmarSenha" placeholder="Confirmar Senha" required />
        <p>Idade:</p>
        <input type="number" v-model="idade" minlength="3" maxlength="60" placeholder="0" required/>
        <p>Data:</p>
        <input type="date" v-model="data" required />
        <p>Endereço:</p>
        <input type="text" v-model="endereco" placeholder="Endereço" required />
        <p>Cidade:</p>
        <input type="text" v-model="cidade" placeholder="Cidade" required />
        <p>Estado:</p>
        <select v-model="estado">
          <option value="AC">Acre</option>
          <option value="AL">Alagoas</option>
          <option value="AP">Amapá</option>
          <option value="AM">Amazonas</option>
          <option value="BA">Bahia</option>
          <option value="CE">Ceará</option>
          <option value="DF">Distrito Federal</option>
          <option value="ES">Espírito Santo</option>
          <option value="GO">Goiás</option>
          <option value="MA">Maranhão</option>
          <option value="MT">Mato Grosso</option>
          <option value="MS">Mato Grosso do Sul</option>
          <option value="MG">Minas Gerais</option>
          <option value="PA">Pará</option>
          <option value="PB">Paraíba</option>
          <option value="PR">Paraná</option>
          <option value="PE">Pernambuco</option>
          <option value="PI">Piauí</option>
          <option value="RJ">Rio de Janeiro</option>
          <option value="RN">Rio Grande do Norte</option>
          <option value="RS">Rio Grande do Sul</option>
          <option value="RO">Rondônia</option>
          <option value="RR">Roraima</option>
          <option value="SC">Santa Catarina</option>
          <option value="SP">São Paulo</option>
          <option value="SE">Sergipe</option>
          <option value="TO">Tocantins</option>
        </select>
        <p>Hobbies:</p>
        <textarea v-model="hobbies" />
        <p style="white-space: pre-line"></p>
        <p>Linguagens de Programação:</p>
        <input type="radio" v-model="programacao" value="JavaScript" /> JavaScript
        <input type="radio" v-model="programacao" value="Python" /> Python
        <input type="radio" v-model="programacao" value="Java" /> Java
        <input type="radio" v-model="programacao" value="C++" /> C++
        <input type="radio" v-model="programacao" value="C#" /> C#
        <input type="radio" v-model="programacao" value="SQL" /> SQL
        <input type="radio" v-model="programacao" value="PHP" /> PHP
        <input type="radio" v-model="programacao" value="VBA" /> VBA
        <p>Biografia:</p>
        <textarea v-model="biografia" />
        <p style="white-space: pre-line"></p>
        <hr />
        <button type="submit" @click="enviar = !enviar">Enviar</button>
      </form>
    </div>
    <div class="info2" v-if="enviar">
      <h1>Formulário Preenchido</h1>
      <p>Nome: <br>{{ nome }}</p>
      <p>Email: <br>{{ email }}</p>
      <p>Senha: <br>{{ senha }}</p>
      <p>Confirmar Senha: <br>{{ confirmarSenha }}</p>
      <p>Idade: <br>{{ idade }}</p>
      <p>Data de Nascimento: <br>{{ data }}</p>
      <p>Endereço: <br>{{ endereco }}</p>
      <p>Cidade: <br>{{ cidade }}</p>
      <p>Estado: <br>{{ estado }}</p>
      <p>Hobbies: <br>{{ hobbies }}</p>
      <p>Linguagem de Programação: <br>{{ programacao }}</p>
      <p>Biografia: <br>{{ biografia }}</p>
    </div>
  </main>
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
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 28%;
  margin:  0 auto;
  margin-top: 20px;
  margin-bottom: 20px;
}

.info2 {
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 28%;
  margin:  0 auto;
  background-color: rgb(31, 31, 31);
  padding: 20px 30px;
  color: rgb(183, 210, 219);
  border-radius: 10px;
  text-align: center;
  margin-top: 20px;
  margin-bottom: 20px;
}

</style>
