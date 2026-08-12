# Tags

## Criando tags

Podemos criar um controle de versão extendidos com **tags**. Com isso podemos baixar o código do projeto usando tags.

```bash
git tag -a 1.0.0 -m "Final release"
```

E em seguida executar **push** para o repositório remoto.

```bash
git push origin master --tags
```

## Listando as tags

Podemos listar as tags existentes do repositório com o comando abaixo.

```bash
git tag
```

## Removendo tags

Podemos remover as tags existentes do repositório com o comando abaixo.

### Repositório local

```bash
git tag -d numero-tag
```

### Repositório remoto

```bash
git push origin :numero-tag
```
