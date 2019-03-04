<template>
  <div>
    <b-button variant="info">Info</b-button>
    <p>Você quer me ver ...</p>
    <p>...ou eu</p>
    <p>Você quer me ver ...</p>
    <p>...ou eu</p>
  </div>
</template>

<script>
export default {
  name: "Listing",
  data() {
    return {
      livro: {
        titulo: "O Senhor dos Anéis",
        autor: "J.R.R. Tolkiens",
        Volume: "3"
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
