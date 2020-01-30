# Usando Docker para colocar um servidor no ar

## 1) Criando imagem e rodando localmente

    1.1 Criar a receita para criar a imagem da aplicação
    * Dockerfile

    1.2 Criar uma imagem localmente utilizando a receita acima
    * `sudo docker build -t image/mapa .`

    1.3 Criar um container usando a imagem que geramos para poder usar de fato a aplicação
    * `sudo docker run --name mapa -d image/mapa -p 8008:8080`

    **Nesse ponto teremos um container rodando localmente, agora temos que levar isso para nuvem.**

    1.4 Remover o container parado e todas as imagens, incluindo imagens não utilizadas ou pendentes
    * `docker system prune -a`

## 2) Salvando a imagem no Docker Hub

### Push da imagem no DockerHub
