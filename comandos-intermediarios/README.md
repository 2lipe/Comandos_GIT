# Uso Intermediário do GIT

- Obs: antes de iniciar a leitura dos comandos.
  - Aspas simples significa que não precisa usar aspas para realizar o comando
  - Aspas dupla significa que precisa usar aspas para realizar o comando

### Criando novas branches

- $git branch
  - Informa qual a branch estamos no momento e quantas branches possui

- $git branch 'nome_da_branch'
  - Cria uma nova branch

- $git checkout -b 'nome_da_branch'
  - Cria a branch e muda para a branch criada ao mesmo tempo

### Mudando a branch

- $git checkout 'nome_da_branch'

### Deletando uma branch

- $git branch -d 'nome_da_branch'
  - Observa se foi feito o merge antes de deletar

- $git branch -D 'nome_da_branch'
  - Deleta sem perguntar sobre o merge

### Jutando branches (merge)

- $git merge 'nome_da_branch'

### Fazendo rebase

- $git rebase 'nome_da_branch'

### Clonando repositorios

- $git clone 'URL_do_repositorio' ou 'SRC_do_repositorio'

### Enviando arquivos para o repositorio principal

- $git push
  - Envia os commits para o repositório central

### Baixando arquivos do repositorio principal (atualizando)

- $git fetch
  - Para adicionar no repositorio precisa realizar um rebase

- $git pull
  - Adiciona diretamente os arquivos sem precisar de rebase

### Iniciando um Bare repository

- $git init --bare
  - É um diretório centralizador do projeto

### Criando/Trabalhando com Tags

Obs: Não existe commits em tags, usado para entrar em produção
`Release`

- $git tag 'nome_da_tag'
  - Versão do software Ex: git tag v1.0

- $git checkout 'nome_da_tag'
  - visualizar o projeto em sua respectiva versão

- $git switch -c 'nome_da_branch'
  - Cria uma nova branch da tag selecionada
