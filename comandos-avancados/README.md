# Uso Avançado do GIT

- Obs: antes de iniciar a leitura dos comandos.
  - Aspas simples significa que não precisa usar aspas para realizar o comando
  - Aspas dupla significa que precisa usar aspas para realizar o comando


### Adicionando Repositório BARE

- $git remote add origin 'url_para_onde_sera_enviado'

- $git push -u origin master
  - Registra o branch no repositório

- $git remote -v
  - Informações da url do repositório

### Clonando Repositório

- $git clone 'url ou ssh'
  - Faz um clone do projeto na pasta aberta no seu terminal

### Realizando Pull (Atualizando projeto)

- $git pull origin master

### Desfazer Checkouts

- $git checkout -- .
  - Desfaz a alteração de todos os arquivos

- $git checkout -- 'nome_do_arquivo'
  - Desfaz a alteração do arquivo selecionado

- $git checkout HEAD -- .
  - Desfaz a alteração mesmo após adicionado

- $git checkout HEAD -- 'nome_do_arquivo'
  - Desfaz do aqruivo selecionado mesmo após adicionado

### Executando Revert

- $git revert 'id_do_commit'
  - Reverte as alterações do arquivo mantendo o histórico após commitado

### Removendo Commit

- $git reset HEAD~1
  - Desfaz o commit, o numero 1 representa a quantidade de commits começando do último commitado
