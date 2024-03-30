# Configuracao de ambiente Ubuntu no WSL

Comece instalando a versão LTS mais recente do Ubuntu

```bash
wsl --install -d Ubuntu-22.04
```

## Setup do GitHub

1. Instale o git.

```bash
sudo apt-get install git-all
```

2. Defina o usuário.

```bash
git config --global user.email "name@email.com"
```

3. Gere uma chave ssh.
```bash
ssh-keygen -t rsa -b 4096 -C "name@email.com"
```

4. Visualize a chave gerada.
```bash
cat ~/.ssh/id_rsa.pub
```

5. Copie todo o código do início ao fim.

6. No GitHub, vá para `Settings` > `SSH and GPG keys` e clique em `New SSH key`.

7. Digite qualquer título de identificação, coloque o tipo `Authentication key` e cole todo o código da chave gerada no passo 3.

8. Agora que está autorizado, clone este repositório.

```bash
git clone git@github.com:adilsonsds/notes.git
```

9. Navegue até a pasta usando `cd notes` e defina a pasta remota de origem

```bash
git remote set-url origin git@github.com:adilsonsds/notes.git
```

10. Modifique algum arquivo no VSCode `code .` e faça um commit de teste

```bash
git add .
git commit -m "test commit"
git push
```


## Setup do Docker

1. Siga as intruções de instalação do Docker disponível em [Docker.docs](https://docs.docker.com/engine/install/ubuntu/#install-using-the-repository).

2. Para executar os comandos do docker sem o `sudo`, adicione seu usuário ao grupo `docker` seguindo as intruções disponíveis em [Linux postinstall](https://docs.docker.com/engine/install/linux-postinstall/).