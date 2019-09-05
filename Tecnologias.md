# Node.js
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
- - npm 
- - yarn (rapido, seguro e confiável)

* **Obs**: Sempre verificar qualidade do biblioteca que se está usando.
Dados de `downloads`, `open issues` e sua interação com a comunidade ajuda na hora de saber se o pacote se mantem atualizado e 
se está sendo utilizado ou bem avaliado. Assim pode-se decidir, com mais clareza,
se vale a pena utilizar determinada biblioteca em seu projeto.
