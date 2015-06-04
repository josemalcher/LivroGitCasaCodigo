# 3 Trabalhando com repositório local

Manter o histórico é importante, para caso necessite voltar e recuperar aquivos.

## 3.1 Criando um repositório local

- Criação da pasta 'moveis' e iniciando o versionamento *git init*.
- Pode-se executar o **git init moveis** se quisermos criar um diretório vazio que já é um repositório Git, ou seja, que já possui o *.git*.
- Se por algum motivo quisermos parar de usar o Git, basta **remover** esse único diretório *.git*.
- Basta o comando *git init* para criar um repositório Git, mais simples entre outro sistemas de controle de versão.

## 3.2 Rastreando arquivos

- Verificar o estado atual do repositório **git status**
- Aparecerá arquivos não rastreados. (Untracked files).
- Usando **git add arquivo.html** para rastrear o arquivo. O arquivo ficará pronto para gravar no repositório(Changes to be committed).
- Para rastrear vários arquivos de uma só vez: **git add .**

### A área de stage

Uma vez que o arquivo está na área de *stage*, todas as mudanças nesse arquivo passam a ser examinadas.(Diretório de trabalho ou Working Directory)  
Se houver modificações em arquivos que estejam na *stage* área, deverá novamente usar o comando **git add .** para alocar as modificações.

### Ignorando arquivos

- Para ignorar arquivos: Criar um arquivo **.gitignore** no diretório principal. O mesmo não será *rastreado* pelo git.
- É importante o rastreamento do mesmo! **git add .gitignore**
- adicionar os arquivos e pastas a serem ignorados.
- Site com Templates de projetos com arquivos a serem ignorados: https://github.com/github/gitignore

## 3.3 Gravando arquivos no repositório

- A pós o *commit*, é registrado no repositório com 40 números, apenas 7 deles são apresentados. 40 dígitos são da função hash SHA-1 que serve para verificar a integridade dos arquivos alocados.


### Rastreando e comitando mudanças de uma só vez

É possível **Adicionar** e **Comitar** em apenas um comando: **git commit -a -m "mensagem"** ou **git commit -am "mensagem"**

### Novos arquivos git add

Ao Adicionar um novo arquivo e modificar um arquivo. O comando **git commit -am "mensagem"** adicionará apenas o arquivo modificado.  
O arquivo adicionado tera que passar pelo **git add novo.html** para depois passar para o processo de *commit*.

### Para que serve o *stage*

"Permite que as mudanças que fizemos no código sejam agrupadas de maneira lógica. Desta forma, podemos montar commits menosres, que farão mais sentido posterior ao revisarmos o histórico do projeto e ajudaram ao mesclarmos nossas mudanças com os dos outros membros do time"

## 3.4 Verificando o histórico do seu repositório

- **git log** lista os commits efetuados.
- git log **-n 2** lista os dois ultimos commits
- git log **--oneline** Lista os commits resumidos.
- git log **--stat** Mostra um resumo dos arquivos alterados, com o nuero de linhas adicionadas e removidas. Para sair usar tecla **q**.
- git log **-n 2 --online --stat** Combinação de opções.

## 3.5 Verificando mudanças nos arquivos rastreados

- A pós um ajuste em um arquivo do repositório, verifica-se: **git status**;

### Verificando mudanças ainda não rastreadas

- **git diff** Verifica as diferenças entre o arquivo alterado e o que foi comitado anteriormente.
- git **diff nomeAquivo.html** Para verificar mudanças em um arquivo específico.
- Não dá para usar **git diff** em arquivos novos, que ainda não passaram pelo *git add* antes.

### Verificando mudanças rastreadas

- Adicionando o arquivo na área de stage (*git add*).
- Executando o comando **git diff** - Quando usado sem parâmetros, mostra a diferença entre os arquivos no diretório de trabalho e área de stage, exibe as mudanças ainda não rastreadas.
- **git diff --staged** Mostra a diferenças entre os arquivos na área de stage e a última versão que foi comitada.

### Verificando mudanças rastreadas e não rastreadas ao mesmo tempo

- É necessário descobrir o código do último commit: ** git log -n 1 --online**.
- Com os 7 dígitos deve-se usar: **git diff 1234567**
- Pode-se usar o comando: **git diff HEAD**, porém o *HEAD* aponta para o último commit efetuado, mas não é sempre assim, o *HEAD* pode apontar para commits anteriores.

### Verificando mudanças já comitadas




3.6 Removendo arquivos do repositório
3.7 Renomeando e movendo arquivos
3.8 Desfazendo mudanças
