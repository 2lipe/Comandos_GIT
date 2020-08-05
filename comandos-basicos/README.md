# Uso Básico do GIT

- Obs: antes de iniciar a leitura dos comandos.
  - Aspas simples significa que não precisa usar aspas para realizar o comando
  - Aspas dupla significa que precisa usar aspas para realizar o comando

### Iniciando GIT em um projeto

- $git init

### Criando .gitignore

- $touch .gitignore
  - * ignora qualquer arquivo com a extensão Ex: *.ext
  - 'nome_do_diretorio' para ignorar diretorios
  - usar **'nome_do_arquivo' para ignorar arquivos

### Comandos de configuração do GIT

- Local
  - $git config user.name "name"
  - $git config user.email "email"

- Global
  - $git config --global user.name "name"
  - $git config --global user.email "email"

### Comandos básicos (Listar e Adicionar)

**IMPORTANTE**
- $git status
  - Listar arquivos do projeto com git

- $git add .
  - Adicionar todos os arquivos para serem monitorados
- $git add 'nome_do_arquivo'
  - Adicionar arquivo específico para ser monitorado

### Comitando arquivos/projetos

- $git commit -m "msg_do_commit"
  - Essa mensagem visa descrever mudanças realizadas no projeto/arquivo
  - "Salva" as alterações realizadas no monitoramento do git
  - A cada novo commit um novo hashId do commit

##### Consultando histórico de commits 'log'

- $git log
  - Consulta o autor do commit data e hora

- $git log --oneline
  - Consulta simplificada dos commits

- $git log -'numero_de_comits'
  - Retorna a consulta da quantidade selecionada de commits Ex: 1, 2, 3...

- $git log --before="ano-mes-dia"
  - Retorna a consulta de commits realizados antes da data selecionada Ex: 2020-08-04

- $git log --after="ano-mes-dia"
  - Retorna a consulta de commits realizados depois da data selecionada Ex: 2020-06-15

- $git log --since="2 days ago"
  - Retorna a consulta de commits relizados desde 2 dias atras Obs: selecione a quantidade de dias desejados

- $git log --author="nome_do_autor"
  - Retorna a consulta dos commits realizados pelo autor selecionado

- $git help log
  - Para mais informações sobre o uso do comando "log"

- $git config core.pager cat
  - Configura para retornar a consulta de todos os commits
- $git config core.pager less
  - Configura para retornar a quantidade de commits que couber em seu terminal

### Voltando no tempo com GIT

- $git checkout 'hashId_do_commit'
  - Retorna o projeto para o commit selecionado

- $git checkout master
  - Retorna para a branch principal do projeto

- $git checkout 'nome_do_arquivo'
  - Restaura alterações indesejadas no arquivo até o ponto do último commit

- $git reset HEAD --hard
  - Reseta todas as alterações do projeto até o último commit

- $git reset HEAD^ --hard
  - Desfaz o commit realizado e retorna para o commit anterior

### Renomeando arquivos/diretorios com GIT

- $git mv 'nome_do_arquivo' 'novo_nome_do_arquivo'

### Removendo arquivos/diretorios com GIT

- $git rm 'nome_do_arquivo'

### Mostrando alterações de arquivos

- $git diff --staged
  - Antes de realziar o commit do arquivo, retorna as alterações adicionadas
  - OBS: Antes de comitar o arquivo

- $git diff 'hashId_do_commit'
  - Retorna a diferença do projeto atual até o commit selecionado

- $git diff 'hashId_do_1°_commit'..'hashId_do_2°_commit'
  - Retorna a diferenca dos arquivos entre commits

### Refazendo o commit com o GIT

- $git commit --amend -m "nova_msg_do_commit"
  - Refaz o commit
  - Adiciona alterações no mesmo commit

### Removendo arquivos de staged

- $git restore --staged 'nome_do_arquivo'
  - Retira o arquivo/diretorio do monitoramento
