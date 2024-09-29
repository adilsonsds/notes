# Comandos Docker

## Build
Produz uma imagem. Requer um Dockerfile.

- `docker build .` -> Constrói o Dockerfile no diretório atual.
- `docker build . -t olamundo` -> Constrói o Dockerfile e produz uma imagem com a tag `olamundo`.

## Push
Publica uma imagem.

- `docker push`

## Run
Executa uma imagem Docker.

- `docker run olamundo` -> Executa uma imagem pela tag.
- `docker run 4ec58c40b86f` -> Executa uma imagem pelo ID.

## Images
Lista imagens Docker.

- `docker images` -> Lista todas as imagens.

## PS
Lista contêineres Docker.

- `docker ps -a` -> Lista todos os contêineres.
- `docker ps -aq` -> Lista os IDs de todos os contêineres.

## RM
Remove contêineres Docker.

- `docker rm -f 4ec58c40b86f` -> Remove um contêiner pelo ID.
- `docker rm -f 4ec58c40b86f d9d1dd146c63` -> Remove uma lista de contêineres pelo ID.
- `docker rm -f $(docker ps -aq)` -> Remove forçadamente todos os contêineres.

## Compose
Gerencia aplicações Docker multi-contêiner.

- `docker-compose up` -> Cria e inicia contêineres.
- `docker-compose build` -> Constrói imagens para serviços definidos em um `docker-compose.yml`.
- `docker-compose logs` -> Visualiza logs dos contêineres.
- `docker-compose restart` -> Reinicia contêineres.
- `docker-compose ps` -> Lista contêineres.
- `docker-compose scale` -> Escala o número de instâncias de contêineres.
- `docker-compose start` -> Inicia contêineres.
- `docker-compose stop` -> Para contêineres.
- `docker-compose down` -> Para e remove todos os contêineres e seus componentes como redes, imagens e volumes.