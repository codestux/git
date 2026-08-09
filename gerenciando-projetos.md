# Gerenciando projetos

Para iniciarmos e controlar os arquivos de um projeto, precisamos criar um repositório. Um repositório é um local virtual de armazenamento que podemos acessar quando precisar.

## Inicializando um projeto

Dentro do diretório do projeto executamos o comando abaixo para criarmos um controle de versão dos arquivos. Ele é executado apenas no início do projeto e cria um diretório **.git** e suas ramificações.

```bash
git init ou git init <diretório-do-projeto>
```

Após o comando, o Git começa a monitorar as alterações que ocorrem dentro do diretório. Ele transforma a pasta em um projeto com controle de versão.

Uma pasta oculta chamada **.git** será criada e nela serão feitos o controle de versão dos arquivos/pastas do projeto.

## Ciclo de vida dos arquivos

Há no repositório controlado pelo Git alguns estados dos arquivos e que precisam ser entendidos perfeitamente para entender sobre os versionamentos.


1. **untracked(não marcado)**

O arquivo foi adicionado no repositório do Git, mas ainda não está marcado para monitoramento pelo GIT.

2. **tracked**

O arquivo foi adicionado no repositório do Git e está marcado para monitoramento pelo GIT.

3. **unmodified**

Quando o arquivo é adicionado para monitoramento pelo Git ele assume o estado de não modificado e passa a ser monitorado pelo Git.

4. **modified**

Assume esse status no momento que ocorre alguma modificação no arquivo e pode receber uma status de arquivo versionado.

5. **stage**

Quando o arquivo já pode ser enviado para aguardar o fechamento de uma versão. Quando um commit é feito os arquivos são modificados para o estado unmodified.

## Ignorando arquivos dentro do repositório

Para ignorar os arquivos que não queremos controlar o versionamento, criamos um arquivo oculto **.gitignore** e especificamos os arquivos pelos nomes ou extensões que serão ignorados.

## Verificando o estado atual do repositório

Podemos verificar o estado dos arquivos no repositório. É uma comparação dos estado atual com os arquivos que estão no repositório.

```bash
git status
```

## Adicionando arquivo para commit

Os comandos abaixo adicionam os arquivos ao projeto e prepara-os para o commit.

```bash
git add arquivo1 arquivo2 arquivo3	 --> Adiciona um ou mais arquivos informados.

git add .  --> Adiciona todos os arquivos do repositório.

git add -all --> Adiciona todos os arquivos alterados e não monitorados ao repositório.
```

## Commintando arquivos

O commit informa ao Git para criar uma imagem/check point dos arquivos do repositório.

```bash
git commit -m "Mensagem de descrição do commit"

git commit -am "Texto explicativo do commit"  --> O parâmetro -am significa: a=adicionar todos e m=mensagem
```

## Exibindo log dos processos no repositório

Exibe o histórico de commits.

```bash
git log --oneline --> Exibe informações dos commits em apenas uma linha.

git log --decorate --> Exibe informações com alguns detalhes.

git log --author="name" --> Exibe informações por autor(usuário) dos processos no repositório.

git shortlog --> Exibe informações por autor(usuário) dos processos no repositório, quantidade e quais processos foram feitos. A opção -sn informa a quantidade de commits por usuário.

git log --graph --> Exibe informações com alguns detalhes de forma gráfica.

git log -p --> Exibe informações detalhadas dos commits com linhas removidas e adicionadas nos arquivos.

git log --pretty="format: %h %s %T" --> Personaliza o resultado do log com as informações que desejamos.

git show [hash] --> Exibe detalhes de uma hash.
```

## Visualizando as alterações antes de adicionar para commit

Podemos visualizar o conteúdo adicionado ou removido antes de adicionar para commit com o **diff**. 

Isso permite ler o conteúdo antes de enviar algo que pode quebrar algo no código.

```bash
git diff --> Exibe as alterações realizadas nos arquivos.

git diff --name-only --> Exibe apenas os arquivos que foram alterados.
```

## Desfazendo modificações

É possível desfazer alterações nos arquivos com o Git. Com os comandos abaixo, podemos realizar essas operações.

```bash
git checkout nome-do-arquivo  --> Desfaz alterações realizadas no arquivo antes de estar no stage.

git reset HEAD nome-do-arquivo --> Retira o arquivo da área de stage.

git reset --soft hash --> Retira o hash do commit e volta para o stage

git reset --mixed hash --> Retira o hash do commit e volta para o estado para antes do stage.

git reset --hard hash --> Remove o commit completamente.

git revert hash --> Desfaz as modificações, mas permite ter acesso ao código em outro momento.
```
