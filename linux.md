# Comandos de navegação de diretórios

- `pwd` (Ver o caminho da pasta atual)
- `cd ~` (Ir para o diretório home)
- `cd /` (Pasta raiz)
- `cd mnt` > `ls c` (Lista os arquivos da pasta C:// do Windows)
- `explorer.exe .` (Abre o diretório na janela do Windows Explorer); inverso: na janela do Windows Explorer: `\\wsl$` (Lista as pastas com todas as distribuições)
- `code .` (Abre o diretório na janela do VS Code)

# Pastas do Linux

- `/` -> Diretório raiz, parecido com o C: do Windows
- `/home` -> Onde ficam os diretórios de trabalhos dos usuários. Cada usuário tem sua pasta. Ex: /home/adilson. Parecido com a pasta Users do Windows.
- `/root` -> É o diretório home do usuário root
- `/bin` -> Principais comandos do Linux (cat, su, rm, pwd)
- `/lib` -> Bibliotecas compartilhadas pelos programas e módulos do kernel
- `/usr` -> Onde a maioria dos programas são instalados, normalmente é usado com acesso de somente leitura.
- `/boot` -> Arquivos estáticos para inicialização do sistema
- `/etc` -> Arquivos de configuração e scripts de inicialização do sistema.
- `/sbin` -> Diretório de programas usados pelo superusuário root, para administração e controle do funcionamento do sistema.
- `/tmp` -> Arquivos temporários
- `/var` -> Dados variáveis como log, dados de administração, login e arquivos transitórios
- `/dev` -> Arquivos de dispositivos (periféricos)
- `/mnt` -> Ponto de montagem para montar um sistema de arquivos temporariamente.

# Comandos

- `uname`, `uname -a`, `uname -s`, `uname -n` -> Mostra dados como o nome e versão do kernel atual
- `clear` -> Limpa o terminal
- `date` -> Mostra a data
- `who` -> Mostra quais usuários estão logados
- `whoami` -> Mostra qual usuário você logou
- `shutdown` -> Desliga a máquina
- `shutdown -r now` -> Reinicia agora
- `man <COMANDO>` (Ex: `man shutdown`, `man clear`) -> Mostra as opções de outros comandos
- `pwd` -> Mostra o diretório atual
- `cd <DIRETÓRIO>` -> Navegar entre pastas/diretórios
- `cd /` -> Ir para a pasta raiz
- `cd ~` -> Ir para o diretório home do usuário
- `cd ..` -> Volta um nível
- `sudo <COMANDO>` -> Executar como superusuário
- `ls` -> Lista todos arquivos e pastas
- `ls -a` -> Lista todos os arquivos e pastas, incluindo os ocultos
- `ls -l` -> Lista todos arquivos e pastas contendo mais detalhes
- `mkdir` -> Cria diretórios
- `mkdir -p pasta-teste/novissima-pasta/outra-pasta` -> O parâmetro `-p` cria toda a hierarquia completa.
- `rm <ARQUIVO/DIRETÓRIO>` -> Remove diretórios e arquivos
- `rm arquivo.txt` -> Remove o arquivo.txt
- `rm -r nova-pasta` -> Remove recursivamente um diretório
- `rm -f` -> Remove um arquivo forçadamente
- `rm -rf` -> Remove recursivamente e forçadamente um diretório
- `cp <ORIGEM> <DESTINO>` -> Copia arquivos
- `cp Test1.txt ~/Test1-copy.txt` -> Copia o arquivo Test1.txt para o diretório home (~) com o nome de Test1-copy.txt
- `mv <ORIGEM> <DESTINO>` -> Move arquivos
- `mv ~/Test1.txt Test1-moved.txt` -> Move o arquivo Test1.txt do diretório home (~) para a pasta atual com o nome de Test1-moved.txt

# Manipulação de arquivos

- `touch` -> Cria arquivos
- `touch teste.txt` -> Cria o arquivo teste.txt; caso o arquivo já exista, a data de alteração será atualizada
- `cat` -> Visualizar o conteúdo de um arquivo
- `head` -> Exibe as primeiras linhas do conteúdo de um arquivo
- `head -n 10 teste.txt` -> Exibe as 10 primeiras linhas
- `tail` -> Exibe as últimas linhas do conteúdo de um arquivo
- `tail -n 5 teste.txt` -> Exibe as 5 últimas linhas
- `more teste.txt` -> Exibe o conteúdo de um arquivo de forma paginada. Pressione ENTER para mostrar mais.
- `less teste.txt` -> Exibe o conteúdo de um arquivo de forma paginada. Use PAGE UP e PAGE DOWN para navegar pelo conteúdo do arquivo. Pressione Q para sair.
- `grep brasil teste.txt` -> Busca pelo texto 'brasil' no arquivo teste.txt
- `grep -n brasil teste.txt` -> Mostra a linha
- `grep -i brasil teste.txt` -> Ignora o case sensitive

# Combinação de comandos

- `ls -l | grep Desktop` -> Pega o resultado do ls e busca por pastas e arquivos com nome Desktop
- `ls -l > comando.txt` -> Pega o resultado do ls e guarda no arquivo comando.txt (Sobrescreve, caso arquivo já exista)
- `ls -l >> comando.txt` -> Pega o resultado do ls e guarda no arquivo comando.txt (Concatena, caso arquivo já exista)
- `cats 2> erro.txt` -> Pega o resultado do cats (comando inválido) e guarda no arquivo erro.txt

# Processos

- `ps` -> Lista os processos em execução na máquina
- `ps -a` -> Mostra os processos criados por você e outros usuários
- `ps -x` -> Mostra os processos que não são controlados pelo terminal
- `ps -u` -> Mostra o nome do usuário e momento que iniciou o processo
- `ps -m` -> Mostra o consumo de memória dos processos
- `ps -f` -> Mostra os processos e subprocessos em árvore
- `kill <NOME>` -> Mata um processo
- `top` -> Mostra detalhes de todos os processos
- `htop` -> Mostra detalhes de todos os processos (precisa instalar)
- `apt update` -> Atualiza os repositórios para pegar as versões mais atuais
- `apt install` -> Instala um pacote

# Acesso remoto via SSH

- `ssh-keygen` -> Gera a chave pública e privada
- `ssh-keygen -t` -> Define o tipo de chave que será criada (dsa, ecdsa, ecdsa-sk, ed25519, ed25519-sk ou rsa)
- `ssh-keygen -b` -> Define o tamanho em bits da chave que será criada

- `ssh-keygen -t rsa -b 2048` -> Irá gerar as chaves id_rsa.pub (pública) e id_rsa (privada) na pasta /home/adilson/.ssh

- `ssh` -> Mostra em detalhes os programas
- `ssh -i` -> Define qual chave será utilizada.

- `ssh -i ~/.ssh/id_rsa root@127.0.0.1`
