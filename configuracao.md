# Configuração

## Configurando usuários

### Escopo do sistema

```bash
git config --system user.name "Acme Tech"

git config --system user.email "code@acme.com.br"

git config --system core.editor vim
```

### Escopo global

```bash
git config --global user.name "Acme Tech"

git config --global user.email "code@acme.com.br"

git config --global core.editor vim
```

### Escopo local

```bash
git config --local user.name "Acme Tech"

git config --local user.email "code@acme.com.br"

git config --local core.editor vim
```

## Removendo configurações

```bash
git config [--system/--global/--local] --unset user.name
```

## Criando Alias

```bash
git config --global alias.s status  --> O comando passa a ser git s

git config --local alias.s status  --> O comando passa a ser git s
```

## Listando as configurações de parâmetros do git

### Todas as configurações

```bash
git config --list
```

### Configurações em cada escopo

```bash
git config --list --show-origin
```

### Configurações do escopo local

```bash
git config --list --local
```

### Configuração do escopo global

```bash
git config --global
```

### Configuração do sistema

```bash
git config --system
```

### Configurações específicas do usuário

```bash
git config user.name

git config user.email
```
