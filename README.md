# 🗄️Arquivo - Turma de Introdução à Computação
Disciplina de Introdução à Computação (C e C++), cursada em 2021.2 na Universidade Federal do Rio de Janeiro (UFRJ).

Neste curso temos a introdução às ferramentas e exercícios dessa linguagem clássica.

*Enunciados serão postados mais a frente, estou dando prioridade a subir o código.*

## 💾 Instalação e Configuração

Faça o download do compilador [MSYS](https://github.com/msys2/msys2-installer/releases/download/2021-07-25/msys2-x86_64-20210725.exe). Instale em algum local cujo caminho não tenha espaços e seja curto. Após isso, sempre use o _MSYS2 MinGW 64-bit_. Facilite o trabalho, fixe-o na barra de tarefas.

Logo abaixo temos um tutorial de configuração padrão.

Faremos a instalação e atualização da base de dados.
```bash
  pacman --noconfirm -Syu
  pacman --noconfirm -S base-devel gcc make openssh man-pages-posix
```

Recomendo instalar um editor de texto pra ser chamado pelo shell. Para isto, o [Sublime](https://download.sublimetext.com/sublime_text_build_4121_x64_setup.exe) é muito usado. Efetue toda instalação, adicione ao menu de contexto e todos os procedimentos comuns. Para que possamos chamar o sublime pelo prompt, acesse o arquivo ```.bashrc``` que está presente na pasta ```c:\<diretório-do-msys2>\home\<seu-username>\.bashrc```. Aberto o arquivo, adicione as seguintes linhas no topo do arquivo:

```
# (*) Shortcuts
alias ls='ls -G' # 

# (*) Environment variables
#export PS1=%
export PATH="$HOME/sublime:$PATH"
```

## 🖥️ Terminal
Note que o prompt pode ser bastante poluído pois contém o nome do usuário e local, para isto, troque por um símbolo curto para facilitar a leitura, como por exemplo "%". Para isto, abra seu arquivo ```.bashrc``` e adiciona a linha ao final do arquivo. Lembre de trocar para o símbolo que preferir.

```
export PS1='% '
```

A variável de ambiente que controla o _prompt_ é a PS1.  Por que "PS1"? _Prompt string one_.
Existe a PS2: um shell costuma de dois prompts diferentes.  O segundo é usado quando o shell aguarda por input que não termina ao se pressionar ENTER.  Por exemplo, se você abre aspas e aperta ENTER sem fechá-las, o shell sabe que você não terminou a string ainda e continua a aguardar.

Caso queira verificar qual é seu caminho (diretório) atual, use o comando ```pwd``` a qualquer momento.


## 👨🏽‍💻 Compilação

Para compilar qualquer código em C, abra o MSYS2 MinGW na pasta desejada (de preferência a raíz do diretório do usuário) e utilize os seguintes comandos:

```
gcc -c hello.c
gcc -o hello hello.o
./hello.exe
```

Troque o ```hello.c``` e os ```hello``` seguintes para o nome oficial do seu arquivo.