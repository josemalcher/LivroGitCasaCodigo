# 2 - Tour prático 5

## 2.1 Instalando e configurando o Git  
- Para Windows - http://msysgit.github.io/, instalação padrão com Git Bash.  
- Para Mac  - https://code.google.com/p/git-osx-installer/downloads  
- Para Linux - sudo apt-get install git ou sudo yum install git  
Outras Distros: http://git-scm.com/download/linux

### Configurações básicas

No GitBash ou terminal, digitar:  
$ git config --global user.name "Fulano da Silva"  
$ git config --global user.email fulanodasilva.git@gmail.com  

## 2.2 Criando um arquivo texto para versionarmos  
- Cria-se uma pasta chamada citações com um arquivo de texto "filmes.txt"

## 2.3 Versionando seu código com Git
- Acesse a pasta "citações" e para transforma-la em um repositório: digite **git init**  
- Aparecerá: Initialized empty Git repository in /home/fulano/EstudosLivroGitCasa/.git/  
- Projeto esta em um repositório vazio.  
- É criado um arquivo .git oculto.

### Rastreado o arquivo

- Para ver a situação do repositório, digite: **git status**, observe a mensagem de retorno.  
- O arquivo filmes.txt ainda não foi rastreado pelo git.  
- Para **adicionar** rastreamento no arquivo:  **git add filmes.txt**  
- Executando novamente **git status** note que o arquivo é adicionado.

### Gravando o arquivo no repositório

- Para **Gravar** ou **Commit** o arquivo no repositório: **git commit -m "Arquivo inicial de citacoes"**  (-m informa a mensagem).  
- para verificar se está o repositório: "git status".

### Alterando o arquivo

- Ajuste ou altere o arquivo de texto "filmes.txt", salvar, e em seguida verifique *git status*, haverá uma nova mudança para ser rastreada.  

### Rastreado e gravando as alterações no repositório

- Para *rastrar* - **git add filmes.txt**  
- Com a modificação *rastreada*, pode partir para gravação no repositório:  
- **git commit -m "Inserindo nova alteração e adição"**, retornará confirmação.

### Verificando alterações relizadas

- Verificar o histório das alterações **gravadas** no repositório:  
- **git log**

## 2.4 Compartilhando seu código através do GitHub

- Criar uma conta no https://github.com/ preencher com os dados requisitados. Há planos *free*.
- Para Criar um novo Repositório, botão **New Repository**  
- No *Repository name* deve-se preencher o nome do repositorio remoto.

### Apontando seu projeto para o GitHub

- Apontar o repositório local para o repositório do GitHub.
- Verificar se a pasta está posicionada no terminal onde foi dado o *git init*.
- Executar o comando: **git remote add origin https://github.com/josemalcher/LivroGitCasaCodigo.git**

### Enviando as alterações para o GitHub

- Para enviar: **git push origin master** 
- Com o comando acima é enviado as alterações para o repositório configurado como nome **origin**
- Será solicitado usuário e senha do github.

### Obtendo projeto do GitHub

- crie uma pasta "projetos_gitHub"
- O comando **clone** deve ser usando para baixar o projeto: git clone https://github.com/fulanodasilva/citacoes.git  
- E feito a cópia do repositório inclusive com o ".git".
- Usando o **git log** dá para ver o histórico do projeto.

