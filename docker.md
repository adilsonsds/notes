# Comando build
Produz uma imagem. Requer arquivo Dockerfile.

- `docker build .` -> Faz o build do Dockerfile no diretório atual.
- `docker build . -t olamundo` -> Faz o build do Dockerfile e produz uma imagem com apelido olamundo

# Comando push
Publica uma imagem.

- `dcoker push`

# Comando run

- `docker run olamundo` -> Executa uma imagem pelo apelido
- `docker run 4ec58c40b86f` -> Executa uma imagem pelo ID

# Comando images

- `docker images` -> Lista as imagens 

# Comando ps
- `docker ps -a` -> Lista todas as images
- `docker ps -aq` -> Lista os ID de todas as images

# Comando rm

- `docker rm -f 4ec58c40b86f` -> Remove uma imagem pelo ID
- `docker rm -f 4ec58c40b86f d9d1dd146c63` -> Remove uma lista de imagens pelo ID
- `docker rm -f $(docker ps -aq)` -> Remove todas as imagens forçadamente