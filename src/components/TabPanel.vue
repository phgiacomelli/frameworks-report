<template>
  <div class="container">
    <div class="title">
      {{ title }}
    </div>
    <ul class="tab-list">
      <li
        v-for="(tab, i) in tabList"
        :key="i"
        :class="{
          'active': i + 1 === activeTab,
          'default': i + 1 !== activeTab
        }"
      >
        <label :for="`${i}`" v-text="tab" />
        <input
          :id="`${i}`"
          type="radio"
          :name="`${i}-tab`"
          :value="i + 1"
          v-model="activeTab"
          class="hide"
        />
      </li>
    </ul>

    <template v-for="(tab, i) in tabList">
      <div :key="i" v-if="i + 1 === activeTab" class="panel-content">
        <slot :name="`tabPanel-${i + 1}`" />
      </div>
    </template>
  </div>
</template>

<style scoped>
.container {
  width: 100%;
  display: flex;
  /* justify-content: center; */
  align-items: center;
  padding: 2rem 3rem;
  flex-direction: column;
}
.title{
  font-size: 2rem;
  font-weight: 500;
  color: var(--secondary-color);
  padding: 1rem;
}
.tab-list {
  display: flex;
  align-items: center;
  list-style: none;
  background-color: var(--primary-light-color);
  padding: 1rem;
  border-radius: 0.8rem;
  gap: 1.5rem;
}

li {
  padding: 0.3rem 0.8rem;
}
li.active {
  color: var(--primary-color);
  font-weight: bold;
  background-color: var(--secondary-color);
  
  border-radius: 0.6rem;
}
label{
  width: 100%;
  height: 100%;
}

label:hover{
  cursor: pointer;
}
.default {
  color: var(--tertiary-color);
}
.hide {
  display: none;
}

.panel-content {
  margin-top: 1rem;
  background-color: var(--primary-light-color);
  width: 100%;
  border-radius: 1rem;
  padding: 2rem 3rem;
}

.tab-title{
  color: red;
}
</style>

<script lang="ts">
export default {
  props: {
    tabList: {
      type: Array,
    },
    title: String
  },
  data() {
    return {
      activeTab: 1
    }
  },
}
</script>
