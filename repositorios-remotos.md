# Conectando servidor remoto ao local

Dentro do nosso projeto, precisamos adicionar um servidor remoto para o qual devemos enviar os arquivos que podem ser acessados por outros usuários. Usando o comando abaixo. Exemplo:

## Conexão SSH

```bash
git remote add origin git@github.com:codestux/nome-repositorio.git
```

## Conexão HTTPS

```bash
git remote add origin https://github.com/codestux/test.git
```

## Informações dos servidores remotos

Dentro do repositório local, podemos usar os comandos abaixo para informações sobre repositórios remotos existentes.

```bash
git remote --> Exibe o nome do repositório remoto.

git remote -v --> Exibe mais detalhes do repositório remoto.
```

## Envio de arquivos para o servidor remoto

Dentro do repositório local, executamos o comando abaixo.

```bash
git branch -M master
git push -u(apenas uma vez no repositório) origin master --> Envia todos os arquivos e logs para o repositório remoto.
```

## Clonando repositório existentes

Podemos clonar(copiar) um repositório já existente com o Git. O comando abaixo cria um clone de um projeto remoto já existente.

### Clone SSH

```bash
git clone git@github.com:codestreambr/project.git nome-do-diretorio-local
```

### Clone HTTPS

```bash
git clone https://github.com/codestreambr/git-course.git nome-da-diretorio-local
```

Será criado um diretório com o mesmo nome do repositório se não for informado um nome.

## Exibindo lista de stashs

Guarda modificações não commitadas e que pode ser chamadas quando necessária.

O **git stach list** exibe os stashes ativos.

```
git stash list
```

## Congelando versão ainda não finalizada

O **git stash** permite que seja congelado arquivos que ainda não estão finalizados para commit e que depois você pode voltar a trabalhar nele.

```
git stash
```

## Descongelando versão ainda não finalizada

O **git stash apply** permite que seja descongelado arquivos que ainda não estão finalizados para commit e precisam ser finalizados e voltar a trabalhar nele.

```
git stash apply
```

## Limpando versão ainda não finalizada

O **git stash clear** permite limpar arquivos estão no modo **stash**.

```
git stash clear
```

## Criando tags

Podemos criar um controle de versão extendidos com **tags**. Com isso podemos baixar o código do projeto usando tags.

```
git tag add -a 1.0.0 -m "Final release"
```

E em seguida executar **push** para o repositório remoto.

```
git push origin master --tags
```

## Listando as tags

Podemos listar as tags existentes do repositório com o comando abaixo.

```
git tag
```

## Removendo tags

Podemos remover as tags existentes do repositório com o comando abaixo.

### Repositório local

```
git tag -d numero-tag
```

### Repositório remoto

```
git push origin :numero-tag
```

## Revert

Permite reverter as alterações realizados ou commitadas sem perder o que foi feito. O histórico não é removido e pode ser usado para verificar o código revertido.

```
git revert 3e6d9650512b0508ae53637fcdb9e839281a9d3e
```

# Apagando tags e branch remotos

Podemos remover tags e branchs dos repositórios remotos com os comandos abaixo.

```
git push origin :nome-tag
git push origin :nome-branch
```

# Fork

É uma forma de contribuir com projetos que você não é o dono.
