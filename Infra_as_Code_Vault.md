# Vault by HashiCorp

- Quando falamos de API tokens, certificados, senhas ou outro dado que seja confidencial ou que necessite alguma proteção especial, estamos falando de secrets.

- Vault é uma ferramenta para o armazenamento de secrets de maneira segura, centralizada e com alta disponibilidade.

Desenvolvido em Go

[Doc Vault](https://www.vaultproject.io/docs)

## Primeiros passos

Para isso, nesse primeiro exemplo, nós vamos utilizar o `vault server` em `dev mode`, isso faz com que tenhamos um ambiente pronto para estudarmos e para que possamos realizar os nossos testes iniciais.

Quando estamos utilizando o `dev mode`, nós não precisamos de um backend, como o Consul, para armazenar as secrets. As secrets serão armazenadas em memória. 

Outro detalhe importante é que quando estamos utilizando em `dev mode`, o nosso Vault já é criado `Initialized` e `unsealed`, ou seja, já vem pronto para uso.

Initialized => É o momento onde o serviço do Vault é realmente criado, inclusive é nesse momento onde é criada o `root token` e as chaves para realizar o `unseal` do Vault.

Unseal => É tornar aquela instância do Vault pronta para que os secrets possam ser acessados. É o momento onde tornamos os dados que estão armazenados no Vault descriptografados e disponíveis para acesso mediante autorização.

`vault server -dev `
`vault server -dev -dev-listen-address=0.0.0.0:8200 -dev-root-token-id=giropops &`


Perceba que agora passamos alguns parâmetros, personalizando um pouco o nosso Vault server.

-dev-listen-address => Utilizada para passar o endereço onde a API estará ouvindo

-dev-root-token-id => Para personalizar um root token

### Root token

O `root token` é muito importante para o gerenciamento de nosso serviço. É com ele que iremos realizar a autenticação em nossos primeiros exemplos.

Os `root tokens` são tokens que não expiram nunca e nem precisam renovados, além de ter a `root policy` com ele, ou seja, ele tem total poder sobre o nosso serviço Vault.

`vault -autocomplete-install`

Perceba que para criar a secret, utilizamos o sub-comando `put`. Ele é o responsável por criar ou atualizar um valor para uma chave no Vault.

`vault kv put secret/giropops value=VAIIII`

`vault kv get secret/giropops`

`vault kv put secret/giropops value=FUIIII`

`vault kv get -version=1 secret/giropops`

`vault kv delete -versions=1 secret/giropops`

`vault kv metadata get secret/giropops`


Success! Data written to: secret/undelete/giropops

`vault kv undelete -versions=1 secret/giropops`

Exatamente, temos a opção `undelete` para voltar uma versão da secret que foi `deleted`.



Caso queira destruir uma versão de uma secret, podemos fazer da seguinte forma:

`vault kv destroy -versions=1 secret/giropops`

Success! Data written to: secret/destroy/giropops
