<template>
  <div class="container">
    <h1>{{ message }}</h1>
    <button @click="changeMessage">Alterar Mensagem</button>
  </div>
</template>

<style scoped>
.contianer{
    width: 100%;
    height: 100vh;
}
</style>

<script lang="ts">
export default {
  data() {
    return {
      message: 'Olá, mundo!'
    }
  },
  methods: {
    changeMessage() {
      this.message = 'Nova mensagem!'
    }
  }
}
</script>