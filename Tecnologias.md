# Tecnologias para auxiliar o desenvolvimento de aplicações Node.js
**Primeiros passos**:
* `npm init`
* *npm scripts* como o `nodemon` usar para desenvolvimento. 


* Criar um arquivo `README.md` para documentação na raiz do projeto.
* `.gitignore` para não armazenar os *node_mudules*
* `"private" : true` no *package.json*. Isso evita que você publique no repositório `npm` informações que não devem ser compartilhadas
de projetos privados (`npm registry` || `npm publish`)
* Caso não haja conexão com o servidor, por alguma razão, pode-se configurar um **Proxy registry** usando o Verdacio ou Nexus.

##  Tools 
* **NVM** : Permite que se tenha *mais de uma versão de Node.js* no sistema, caso seja necessário fazer algum teste local.
* **Nodemon** , basicamente observa os arquivos e caso haja alteração reinicia o processo.
**Nodemon** em produção pode limpar a memória da aplicação, isso pode te fazer perder a conexão com os usuários, por exemplo.
* **Debugger** : `console.log()` não é uma boa pratica para se debugar o código, existem ferramentas mais adequadas para isso.
Por exemplo: 
rodando o server como o comando abaixo, teremos acesso ao `chrome:// inspect` ou podemos também usar o Debugger da ide (VSCode)
 `node --inspect-brk index.js`
* **Package Managers**:
  * npm 
  * yarn (rapido, seguro e confiável)

   * **Obs**: Sempre verificar qualidade do biblioteca que se está usando.
       Dados de `downloads`, `open issues` e sua interação com a comunidade ajuda na hora de saber se o pacote se mantem            atualizado e se está sendo utilizado ou bem avaliado. Assim pode-se decidir, com mais clareza,
       se vale a pena utilizar determinada biblioteca em seu projeto.
* **TypeScript** : `npm install -g typescript` . Para executar `tsc index.ts`. Basicamente o **Typescript** transpila com codigo para javascript usando o *tsc*.
  * **Definitely typed**: pode ser usando junto com bibliotecas javascripts, pra uso das tipagens. 
Basicamente agente vai criar um repositório de tipagem que vai ser carregado na aplicação para ser usado junto a essas bibliotecas (Expres,Jquery...).
* **Code Styles**
Assunto controverso, pois cada um tem um estilo de programação, mas a ideia principal aqui e ser consistente, e algumas 
ferramentas ajudam nesse processo. 
  * **Eslint**: Roda Lint regras com o estilo desejado, pré-configurado. 
  * **Prettier**: Suporta vários estilos de estilização de códigos; Integração com vários editores; Configurável

  Exemplos de estilos de codificação:
  * a) https://github.com/airbnb/javascript
  * b) https://github.com/standard/standard
  * c) http://google.github.io/styleguide/jsguide.html
  
* **Async**
  * Uso de `callBacks` = Assim que resultado tiver disponível a função retorna o valor (baseado no *event loop* do Node.js)
  * Uso de `Promises`
  * Uso de `async`/`await` (*success || fail*)
  * Uso de `streams` (muitos estados) **ReactiveX**

* **API**
  * `express`: combinado com *Swagger ou Typescript*
  * `resfify`
  
* **GRAPHQL**

     `npm install graphql`

     Passo a passo:

     * 1) Construir um **Schema**: onde estará como os dados serão estruturados, (nomes, formato, tipos).
     * 2) Escrever os **Resolvers**: no lado do servidor, para retornar os dados corretamente.
     * 3) Escrever as **Queries**: O cliente tem que criar as queries que serão enviadas na requição da Api.

* **Testes**
  * Testes unitários
  
        * `Mocha`  `Jasmine` (Frameworks)
        * `Sinon.js`  `Mockery`  `Istanbul` (Helper librarys) 
        
  * Testes de integração
       
        * `Supertest`  `Jest`? 
        
* **Documentação**

  Documentar pelo menos a Api publica da aplicação ;-) 

  `usejsdoc.org` :  https://jsdoc.app
   
 * **Integração continua**
   * `Jekins integration`
   * `Travis CI`
  
 * **Deploy** (pensar em escalabilidade)
   * `Docker`
   * `PM2`
   * `Kubernetes`
   * `Google Cloud`
   
 * **Performace**
  
      `Performance Timing API` (Node.js) e `Chrome Dev Tools`
      * Memória
      * Uso de CPU
   
 * **Segurança**
    * Filtragem de input
    * Escape output
    * `Validadores`: https://github.com/validatorjs/validator.js
    * Escape DataBase queries
    
           https://www.npmjs.com/advisories
   
  
