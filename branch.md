# Branch

São ramificações que divergem da linha principal de desenvolvimento que se pode trabalhar sem alterar essa linha principal, ou seja, um ponteiro móvel que leva a um commit.

Como se fosse uma linha independente de desenvolvimento que permite alterações isoladas do projeto principal.

## Branch Main

É linha principal/padrão mais estável e consolidada do projeto em desenvolvimento. Nela fica todo o histórico do projeto.

O branch é criado apenas após o primeiro commit. Evitar quebrar o branch não realizando commits direto no main.

## Exibindo os branchs

Para exibir os branchs no repositório, executamos o comando abaixo.

```bash
git branch
```

## Criando branchs

Para criar os branchs no repositório, executamos o comando abaixo.

```bash
git branch nome-branch
```

Se quisermos criar e alternar para o branch criado, podemos usar o comando abaixo.

```bash
git checkout -b nome-branch
```

## Alternando o  branch

Para mudar de branch no repositório, executamos o comando abaixo.

```bash
git checkout nome-branch
```

## Removendo branchs

Para remover um branch que não precisamos, executamos o comando abaixo.

### Repositório local

```bash
git branch -D nome-do-branch
```

### Repositório remoto

```bash
git push origin :nome-branch
```
