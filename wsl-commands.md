# Instalacao

- `wsl -l -o` -> Listar as distribuicoes disponiveis na loja
- `wsl --install -d Ubuntu-22.04` -> Instalar uma distruibuicao
- `wsl -l -v` -> Listar as distribuicoes instaladas

# Execucao

- `wsl -s Ubuntu-22.04` -> Definir uma distruibicao padrao
- `wsl` -> Iniciar a distribuicao padrao
- `wsl -d Ubuntu-22.04`-> Iniciar a distribuicao pelo nome
- `wsl --shutdown` -> Desligar a distribuicao atual
- `wsl -t Ubuntu-22.04`-> Desligar a distribuicao pelo nome

# Desinstalação

- `wsl --unregister Ubuntu-22.04` -> Desistala a distribuicao pelo nome


# Integracao

- `\\wsl$` -> Acessar arquivos nas distribuicoes pelo windows explorer

