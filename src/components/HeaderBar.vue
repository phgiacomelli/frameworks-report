

<template>
  <div class="container">
    <div class="left">Relatório <br><span style="font-size: 4rem">sobre</span><br> Frameworks</div>
    <div class="right">
      {{ text }}
    </div>
  </div>
</template>

<style scoped>
.container {
  width: 100%;
  padding: 2rem;
  display: flex;
  justify-content: space-between;
  align-items: end;
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
    text: String
  },
}
</script>
