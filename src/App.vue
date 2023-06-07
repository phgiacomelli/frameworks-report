<template>
  <HeaderBar />
  <TabPanel :tabList="tabList" :title="`Alguns exemplos`">
    <template v-slot:tabPanel-1>
      <div class="tab-text">
        &nbsp;&nbsp;&nbsp;&nbsp; É um micro framework para web, em <strong>Python</strong>, que
        simplifica e flexibiliza o processo de produção. Sendo possíveis, as configurações de
        roteamento, testes unitários, controle de sessão e muito mais.
      </div>
    </template>

    <template v-slot:tabPanel-2>
      <div class="tab-text">
        &nbsp;&nbsp;&nbsp;&nbsp; É um framework <strong>Javascript</strong> destinado para
        aplicações web. Ele nos permite criar aplicações de forma reativa, e utiliza um DOM virtual,
        o que é muito performático em grande parte das situações. Muito utilzado para criar
        aplicações SPA (Single Page Application).
      </div>
    </template>

    <template v-slot:tabPanel-3>
      <div class="tab-text">
        &nbsp;&nbsp;&nbsp;&nbsp; É um framework <strong>C#</strong>, utilizado para construir
        serviços HTTP, que possibilita diversos dispositivos (browsers e dispositivos móveis)
        acessá-lo e/ou consumi-lo diretamente.
      </div>
    </template>

    <template v-slot:tabPanel-4>
      <div class="tab-text">
        &nbsp;&nbsp;&nbsp;&nbsp; É um framework <strong>PHP</strong>, também utilizado para sistemas web. Conhecido
        pela sua sintaxe elegante, ele disponibiliza diversas extensoes e funções, como por exemplo
        gerenciamento de usuário, cache e outras. Possui integração com plataformas externas (AWS,
        etc.), além de melhorar a performance por meio da execução de tarefas assíncronas.
      </div>
    </template>
  </TabPanel>
</template>

<style scoped>
.tab-text {
  font-size: 1.2rem;
  color: var(--tertiary-color);
}
.tab-text strong {
  color: var(--secondary-color);
}
</style>


<script lang="ts">
import HeaderBar from './components/HeaderBar.vue'
import TabPanel from './components/TabPanel.vue'

export default {
  components: {
    HeaderBar,
    TabPanel
  },
  data() {
    return {
      tabList: ['Flask', 'Vue.js', 'ASP.NET Web API', 'Laravel']
    }
  }
}
</script>
