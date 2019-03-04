<template>
  <div>
    <b-button variant="info" class="mt-5" @click="expressao = !expressao;"
      >Alternar</b-button
    >
    <p v-if="expressao">Você quer me ver ...</p>
    <p v-else>...ou eu</p>
    <p v-show="expressao">Você quer me ver ...</p>
    <p v-show="!expressao">...ou eu</p>

    <hr />

    <div v-for="(nome, inome) in nomes" :key="inome">
      {{ inome }} - {{ nome }}
    </div>

    <hr />

    <div v-for="(valor, chave, ilivro) in livro" :key="ilivro">
      {{ ilivro + 1 }}) {{ chave }}: {{ valor }}
    </div>

    <hr />

    <div v-for="(valor, ialuno) in aluno" :key="ialuno">
      <template v-if="!Array.isArray(valor)">
        {{ valor }}
      </template>
      <template v-else>
        Notas:
        <ul>
          <li v-for="(nota, inota) in valor" :key="inota">{{ nota }}</li>
        </ul>
      </template>
    </div>
  </div>
</template>

<script>
export default {
  name: "Listing",
  data() {
    return {
      expressao: true,
      nomes: ["Thiago", "Camilla", "Julis", "Clarinha"],
      livro: {
        titulo: "O Senhor dos Anéis",
        autor: "J.R.R. Tolkiens",
        volume: "3"
      },
      aluno: {
        id: 10,
        nome: "Thiago",
        notas: [10.0, 9.98, 11, 9.99]
      }
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style></style>
