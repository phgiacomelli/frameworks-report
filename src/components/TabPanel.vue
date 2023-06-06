<template>
  <div class="container">
    <ul class="tab-list">
      <li
        v-for="(tab, i) in tabList"
        :key="i"
        :class="{
          'active': i+1 === activeTab,
          'default': i+1 !== activeTab
        }"
      >
        <label :for="`${i}`" v-text="tab" />
        <input
          :id="`${i}`"
          type="radio"
          :name="`${i}-tab`"
          :value="i+1"
          v-model="activeTab"
          class="hide"
        />
      </li>
    </ul>

    <template v-for="(tab, i) in tabList">
      <div
        :key="i"
        v-if="i+1 === activeTab"
      >
        <slot :name="`tabPanel-${i+1}`" />
      </div>
    </template>
  </div>
</template>

<style scoped>
.active{
    color: var(--secondary-color);
}

.default{
    color: var(--tertiary-color);
}
.hide{
    display: none;
}
.container {
  width: 100%;
  height: 500px;
  background-color: var(--primary-color);
  display: flex;
  /* justify-content: center; */
  align-items: center;
  flex-direction: column;
}

.tab-list{
    display: flex;
    list-style: none;
    background-color: var(--primary-light-color);
    padding: 1rem;
}
</style>

<script lang="ts">
export default {
  props: {
    tabList: {
      type: Array,
      required: true
    }
  },
  data() {
    return {
      activeTab: 1
    }
  },
  mounted() {
    console.log('TabPanel montado')
  }
}
</script>
