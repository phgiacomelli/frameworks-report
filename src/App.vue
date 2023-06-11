<template>
  <HeaderBar />
  <div class="text-container"></div>
  <TabPanel :tabList="tabList" :title="`Alguns exemplos`">
    <template v-slot:tabPanel-1>
      <div class="tab-text">
        &emsp; É um micro framework para web, em <strong>Python</strong>, que simplifica e
        flexibiliza o processo de produção. Sendo possíveis, as configurações de roteamento, testes
        unitários, controle de sessão e muito mais. Justamente por ser um micro framework que sua
        estrutura é mais simples, tornando essa simplicidade uma de suas maiores vantagens. Também é
        bastante utilizado no desenvolvimento de aplicações pequenas, integrações de aplicações além
        de organização das chamadas e resposta de uma API REST.
      </div>

      <div class="code-example">
        <div class="title">Código</div>

        <div class="code-img">
          <img src="../public/img/flask.png" alt="" />
        </div>
        
        <div class="tab-text">
          <ol>
            <li>
              <strong>from flask import Flask, request, jsonify:</strong> Esta linha importa as
              classes e funções necessárias do módulo Flask, como Flask (classe principal), request
              (objeto para acessar dados da requisição) e jsonify (função para converter objetos em
              formato JSON).
            </li>
            <li>
              <strong>app = Flask(__name__):</strong> Aqui, criamos uma instância da classe
              <strong>Flask</strong> e a atribuímos à variável <strong>app</strong>. O parâmetro
              <strong>__name__</strong> é uma variável especial no Python que representa o nome do
              módulo atual.
            </li>
            <li>
              <strong>@app.route('/'):</strong> Este é um decorador usado para definir a rota da
              página inicial. Quando um cliente acessa o caminho '/', a função
              <strong>hello()</strong> será chamada.
            </li>
            <li>
              <strong>def hello():</strong> Esta é a definição da função <strong>hello()</strong>,
              que é chamada quando a rota da página inicial é acessada. Ela retorna a string "Hello,
              World!".
            </li>
            <li>
              <strong>@app.route('/api/add', methods=['POST']):</strong> Este é outro decorador
              usado para definir a rota '/api/add' e especificar que essa rota aceitará apenas
              requisições POST.
            </li>
            <li>
              <strong>def add_numbers():</strong> Esta é a definição da função add_numbers(), que é
              chamada quando a rota '/api/add' é acessada com uma requisição POST. Ela extrai os
              dados da requisição usando <strong>request.get_json()</strong>, que retorna um
              dicionário Python contendo os dados JSON enviados na requisição. Em seguida, os
              números <strong>num1</strong> e <strong>num2</strong> são obtidos desse dicionário e
              somados para obter o resultado. O resultado é retornado como um objeto JSON usando
              <strong>jsonify()</strong>
            </li>
            <li>
              <strong>if __name__ == '__main__':</strong> Esta é uma verificação para garantir que o
              servidor de desenvolvimento do Flask só seja executado quando o arquivo for executado
              diretamente, não quando importado como um módulo. Isso permite que o código seja
              executado apenas quando o script é iniciado diretamente, não quando é importado por
              outros módulos.
            </li>
            <li>
              <strong>app.run(debug=True):</strong> Esta linha inicia o servidor de desenvolvimento
              do Flask. Quando o arquivo é executado, o servidor é iniciado e o aplicativo começa a
              ouvir as requisições. O parâmetro <strong>debug=True</strong> ativa o modo de depuração, o que é útil
              durante o desenvolvimento, pois exibe mensagens detalhadas de erro, recarrega
              automaticamente o aplicativo quando o código é modificado, entre outras
              funcionalidades úteis.
            </li>
          </ol>
        </div>
      </div>
    </template>

    <template v-slot:tabPanel-2>
      <div class="tab-text">
        &emsp; É um framework <strong>Javascript</strong> destinado para aplicações web. Ele nos
        permite criar aplicações de forma reativa, e utiliza um DOM virtual, o que é muito
        performático em grande parte das situações. Muito utilzado para criar aplicações SPA (Single
        Page Application). Algumas vantagens deste framework são: baixa curva de aprendizado, boa
        documentação oficial e versatilidade. Para aplicações de baixa escala, se torna a solução
        perfeita.
      </div>
    </template>

    <template v-slot:tabPanel-3>
      <div class="tab-text">
        &emsp; É um framework <strong>C#</strong>, utilizado para construir serviços HTTP, que
        possibilita diversos dispositivos (browsers e dispositivos móveis) acessá-lo e/ou consumi-lo
        diretamente.
      </div>
    </template>

    <template v-slot:tabPanel-4>
      <div class="tab-text">
        &emsp; É um framework <strong>PHP</strong>, também utilizado para sistemas web. Conhecido
        pela sua sintaxe elegante, ele disponibiliza diversas extensoes e funções, como por exemplo
        gerenciamento de usuário, cache e outras. Possui integração com plataformas externas (AWS,
        etc.), além de melhorar a performance por meio da execução de tarefas assíncronas.
      </div>
    </template>
  </TabPanel>
</template>

<style scoped>
.tab-text {
  font-size: 1rem;
  color: var(--tertiary-color);
}
.tab-text ol{
  padding: 3rem 2rem;
}
.tab-text ol li{
  margin: .4rem 0
}
.tab-text strong {
  color: var(--secondary-color);
}
.title {
  font-size: 2rem;
  font-weight: 500;
  color: var(--secondary-color);
  padding: 1rem 0;
}
.p-tb {
  padding: 2rem 0;
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
