

<template>
  <div class="container">
    <div class="left">Relatório <span style="font-size: 4rem">sobre</span> Frameworks</div>
    <div class="right">
      Este trabalho explora diferentes frameworks, destacando suas funcionalidades e aplicabilidade.
      Serão analisados alguns frameworks relevantes, enfatizando seu papel no desenvolvimento de
      software e na melhoria da eficiência. Serão discutidas as vantagens e boas práticas
      relacionadas à escolha adequada de frameworks para projetos específicos.
    </div>
  </div>
</template>

<style scoped>
.container {
  width: 100%;
  padding: 1.5rem;
  display: flex;
  gap: 1rem;
  align-items: end;
  background-color: var(--primary-color);
}

.left,
.right {
  max-width: 50%;
  height: 100%;
}
.left {
  color: var(--secondary-color);
  font-weight: 700;
  font-size: 6rem;
  padding: 0 0 0 1rem;
}
.right {
  display: flex;
  color: var(--tertiary-color);
  width: 100%;
  justify-content: start;
  align-items: end;
  padding: 0 1rem 1rem 0;
}
</style>

<script lang="ts">
export default {
  props: {
    name: String
  },
  mounted() {
    console.log('Header montado')
  }
}
</script>
