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

## Renomeando um repositório remoto

Usamos o comando abaixo.

```bash
git remote rename antigo-nome novo-nome
```

## Recebendo arquivos do servidor remoto

Dentro do repositório local, executamos o comando abaixo .

```bash
git pull repositório-local repositório-remoto
```

# Fork

É uma forma de contribuir com projetos que você não é o dono.
