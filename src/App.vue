<template>
  <HeaderBar
    :text="`Este trabalho explora diferentes frameworks, destacando suas funcionalidades e aplicabilidade.
      Serão analisados alguns frameworks relevantes, enfatizando seu papel no desenvolvimento de
      software e na melhoria da eficiência.`"
  />
  <div class="text-container">
    &emsp;De forma simples, um framework é um “template”, que já vem de forma pronta e com diversas
    funcionalidades, além de ferramentas que auxiliam no processo de desenvolvimento, o que acaba se
    tornando um código limpo e facilmente adaptável. Os frameworks geralmente são utilizados para
    resolver problemas recorrentes de uma forma mais genérica, ou seja, fazendo com que tarefas mais
    manuais e/ou repetitivas se tornem mais simples ou até mesmo automáticas, o que faz com que o
    foco na resolução do problema aumente. É importante também escolher o framework que se encaixa
    melhor com a proposta do projeto. Seu uso é primordial, pois economiza tempo e reduz o risco de
    erros, pelo fato de que muito código já vem pronto.
  </div>
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
              ouvir as requisições. O parâmetro <strong>debug=True</strong> ativa o modo de
              depuração, o que é útil durante o desenvolvimento, pois exibe mensagens detalhadas de
              erro, recarrega automaticamente o aplicativo quando o código é modificado, entre
              outras funcionalidades úteis.
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

      <div class="code-example">
        <div class="title">Código</div>

        <div class="code-img">
          <img src="../public/img/vue.png" alt="" />
        </div>

        <div class="tab-text">
          <ol>
            <li>
              <strong>&lt;template&gt;:</strong> Esta é a seção onde você define a estrutura do seu
              componente usando a sintaxe do Vue.js. No exemplo, temos uma <strong>div</strong> que
              contém um cabeçalho <strong>&lt;h1&gt;</strong> e um botão
              <strong>&lt;button&gt;</strong>.
            </li>
            <li>
              <strong v-text="'{{ message }}:'"></strong> Aqui, usamos a sintaxe de interpolação do
              Vue.js para exibir o valor da variável <strong>message</strong>. O conteúdo dessa
              variável será exibido dentro do cabeçalho &lt;h1&gt;.
            </li>
            <li>
              <strong>&lt;button @click="changeMessage"&gt;Alterar Mensagem&lt;/button&gt;:</strong>
              Este é um botão que, quando clicado, chama o método <strong>changeMessage</strong>. O
              <strong>@click</strong> é uma diretiva do Vue.js que escuta o evento de clique e
              associa-o a um método específico.
            </li>
            <li>
              <strong>&lt;style scoped&gt;:</strong> A tag é usada para definir estilos CSS dentro
              de um componente Vue.js. O atributo <strong>scoped</strong> indica que os estilos
              definidos nesta tag se aplicam apenas ao componente atual e não afetam outros
              componentes.
            </li>
            <li>
              <strong>&lt;script&gt;:</strong> Esta seção contém a lógica do componente. Nele, você
              pode definir dados, métodos e outras configurações.
            </li>
            <li>
              <strong>export default { ... }:</strong> Aqui, exportamos o objeto Vue que representa
              o componente. O objeto contém várias propriedades, como <strong>data</strong>,
              <strong>methods</strong> e outras, que ajudam a definir o comportamento do componente.
            </li>
            <li>
              <strong>data() { ... }:</strong> Esta é uma função dentro do objeto Vue que retorna um
              objeto. Neste exemplo, a função <strong>data()</strong> retorna um objeto com uma
              única propriedade chamada <strong>message</strong>, que inicialmente contém o valor
              "Olá, mundo!".
            </li>
            <li>
              <strong>methods: { ... }:</strong> Nesta seção, definimos os métodos que podem ser
              usados dentro do componente. No exemplo, temos um método chamado
              <strong>changeMessage()</strong>, que é chamado quando o botão é clicado. Esse método
              atualiza o valor da propriedade <strong>message</strong> para "Nova mensagem!".
            </li>
          </ol>
        </div>
      </div>
    </template>

    <template v-slot:tabPanel-3>
      <div class="tab-text">
        &emsp; É um framework <strong>C#</strong>, utilizado para construir serviços HTTP, que
        possibilita diversos dispositivos (browsers e dispositivos móveis) acessá-lo e/ou consumi-lo
        diretamente.
      </div>

      <div class="code-example">
        <div class="title">Código</div>

        <div class="code-img">
          <img src="../public/img/aspnetcontroller.png" alt="" />
        </div>

        <div class="tab-text">
          <ol>
            <li>
              <strong>using:</strong> Esta instrução define os namespaces que serão usados no
              código. Neste exemplo, são importados alguns namespaces comuns do ASP.NET Web API.
            </li>
            <li>
              <strong>namespace:</strong> É o escopo onde as classes do código estão definidas.
              Neste caso, o código está definido no namespace "WebApiExample.Controllers".
            </li>
            <li>
              <strong>public class ProductsController : ApiController:</strong> Esta é a declaração
              de classe para o controlador de API. A classe herda da classe
              <strong>ApiController,</strong> que é uma classe base fornecida pelo ASP.NET Web API.
            </li>
            <li>
              <strong
                >private static List&lt;Product&gt; products = new List&lt;Product&gt;() { ...
                };:</strong
              >
              Aqui, definimos uma lista estática de objetos <strong>Product</strong>. Essa lista é
              usada como uma fonte de dados fictícia neste exemplo.
            </li>
            <li>
              <strong>public IEnumerable&lt;Product&gt; Get():</strong> Este é um método HTTP GET
              para obter todos os produtos. Ele retorna a lista de produtos como um objeto
              <strong>IEnumerable&lt;Product&gt;</strong>.
            </li>
            <li>
              <strong>public IHttpActionResult Get(int id):</strong> Este é um método HTTP GET para
              obter um produto específico pelo seu ID. Ele recebe o ID como parâmetro e retorna o
              produto correspondente se encontrado, ou retorna um resultado "NotFound" se o produto
              não existir.
            </li>
            <li>
              <strong>public IHttpActionResult Post(Product product):</strong> Este é um método HTTP
              POST para adicionar um novo produto. Ele recebe um objeto
              <strong>Product</strong> como parâmetro e adiciona-o à lista de produtos. Retorna um
              resultado "Created" juntamente com os detalhes do produto criado.
            </li>
            <div class="code-img">
              <img src="../public/img/aspnetclass.png" alt="" />
            </div>
            <li>
              <strong>public class Product { ... }:</strong> Esta é a definição da classe
              <strong>Product</strong>, que representa um produto. Ela possui propriedades como
              <strong>Id</strong>, <strong>Name</strong> e <strong>Price</strong>.
            </li>
          </ol>
        </div>
      </div>
    </template>

    <template v-slot:tabPanel-4>
      <div class="tab-text">
        &emsp; É um framework <strong>PHP</strong>, também utilizado para sistemas web. Conhecido
        pela sua sintaxe elegante, ele disponibiliza diversas extensoes e funções, como por exemplo
        gerenciamento de usuário, cache e outras. Possui integração com plataformas externas (AWS,
        etc.), além de melhorar a performance por meio da execução de tarefas assíncronas.
      </div>

      <div class="code-example">
        <div class="title">Código</div>

        <div class="code-img">
          <img src="../public/img/laravel.png" alt="" />
        </div>

        <div class="tab-text">
          <ol>
            <li>
              <strong>namespace:</strong> Esta instrução define o namespace no qual a classe está
              localizada. Neste exemplo, a classe está no namespace "App\Http\Controllers".
            </li>
            <li>
              <strong>use:</strong> Aqui são importadas as dependências necessárias para a classe.
              Neste caso, estamos importando a classe <strong>User</strong> do modelo, a classe
              <strong>Request</strong> do Laravel e a classe <strong>Validator</strong> do Laravel.
            </li>
            <li>
              <strong>class UserController extends Controller:</strong> Esta é a definição da classe
              <strong>UserController</strong>, que estende a classe base
              <strong>Controller</strong>. A classe base <strong>Controller</strong> é fornecida
              pelo Laravel e fornece recursos comuns para controladores.
            </li>
            <li>
              <strong>public function index():</strong> Este é um método que retorna uma
              visualização (view) contendo todos os usuários cadastrados. Ele busca todos os
              usuários no banco de dados usando o modelo <strong>User</strong> e passa-os para a
              visualização "users.index".
            </li>
            <li>
              <strong>public function store(Request $request):</strong> Este é um método que lida
              com a criação de um novo usuário. Ele recebe um objeto <strong>Request</strong> que
              contém os dados enviados pelo formulário. O método faz a validação dos campos do
              formulário usando a classe <strong>Validator</strong> do Laravel. Se a validação
              falhar, ele redireciona de volta ao formulário com os erros e os dados de entrada
              anteriores. Caso contrário, cria um novo objeto <strong>User</strong>, define seus
              atributos com os valores fornecidos e salva-o no banco de dados. Em seguida,
              redireciona para a rota "users.index" e exibe uma mensagem de sucesso.
            </li>
            <li>
              Dentro do método <strong>store</strong>, usamos o método <strong>bcrypt</strong> para
              criptografar a senha antes de salvar no banco de dados. O PHP fornece esse método, que
              utiliza técnicas de criptografia adequadas para proteger as informações confidenciais.
            </li>
          </ol>
        </div>
      </div>
    </template>
  </TabPanel>
  <FooterBar />
</template>

<style scoped>
.tab-text {
  font-size: 1rem;
  color: var(--tertiary-color);
}
.tab-text ol {
  padding: 3rem 2rem;
}
.tab-text ol li {
  margin: 0.8rem 0;
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
.text-container {
  padding: 3rem;
  color: var(--tertiary-color);
}
</style>


<script lang="ts">
import HeaderBar from './components/HeaderBar.vue'
import TabPanel from './components/TabPanel.vue'
import FooterBar from './components/FooterBar.vue'

export default {
  components: {
    HeaderBar,
    TabPanel,
    FooterBar,
  },
  data() {
    return {
      tabList: ['Flask', 'Vue.js', 'ASP.NET Web API', 'Laravel']
    }
  }
}
</script>
