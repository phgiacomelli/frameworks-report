<template>
  <div class="container">
    <div class="left">
      <h1>Relatório<span>sobre</span>Frameworks</h1>
      <!-- Relatório <br /><span style="font-size: 4rem">sobre</span><br />
      Frameworks -->
    </div>
    <div class="right">
      <p>
        {{ text }}
      </p>
    </div>
  </div>
</template>

<style scoped>
.container {
  width: 100%;
  display: flex;
  justify-content: space-between;
  align-items: end;
  padding-top: 2rem;
}

.left,
.right {
  max-width: 50%;
  height: 100%;
}
.left {
  color: var(--secondary-color);
  font-weight: 700;
  /* padding: 0 5rem; */
  /* margin-left: 2rem; */
}
.left h1 {
  display: flex;
  flex-direction: column;
  font-size: 6rem;
}
.left h1 span {
  font-size: 3rem;
  transform: translateX(4rem);
  max-width: fit-content;
}
.right {
  display: flex;
  color: var(--tertiary-color);
  width: 100%;
  justify-content: start;
  align-items: end;
  text-align: justify;
  /* padding: 0 5rem; */
}

@media only screen and (max-width: 767px) {
  .container {
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }
  .left,
  .right {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    max-width: 100%;
    width: 100%;
  }
  .left h1 {
    font-weight: 700;
    font-size: 3rem;
    padding: 0;
  }
  .right {
    margin-top: 1rem;
    padding: 0;
  }
}

@media only screen and (min-width: 768px) and (max-width: 1024px) {
  .left h1 {
    font-weight: 700;
    font-size: 3rem;
    padding: 0;
  }

  .left h1 span {
    transform: translateX(2rem);
  }
}
</style>

<script lang="ts">
export default {
  props: {
    text: String
  }
}
</script>
