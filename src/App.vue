<template>
  <HeaderBar />
  <TabPanel :tabList="tabList">
    <template v-slot:tabPanel-1> teststst </template>
    <template v-slot:tabPanel-2> Content 2 </template>
    <template v-slot:tabPanel-3> Content 3 </template>
    <template v-slot:tabPanel-4> Content 4 </template>

  </TabPanel>
</template>


<script lang="ts">
import HeaderBar from './components/HeaderBar.vue';
import TabPanel from './components/TabPanel.vue';

export default {
  components: {
    HeaderBar,
    TabPanel
  },
  data() {
    return {
      tabList: ["Flask", "Vue.js", "ASP.NET Web API", "Laravel"],
    };
  },
};
</script>
