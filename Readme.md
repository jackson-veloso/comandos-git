# Comandos GIT:
Referência:
https://gist.github.com/leocomelli/2545add34e4fec21ec16


# configuração pós instalação:
## definir username
git config --global user.name "USERNAME"

## definir email
git config --global user.email "EMAIL"

## definir editor principal
git config --global core.editor nano

## consultar valores definidos:
git config user.name
git config user.email
git config core.editor
git config --list

# criar projeto no git
## na pasta principal (raiz/pai) do projeto inserir o comando:
git init

## verificar status do projeto
git status

## adicionar arquivo para ser monitorado ou adicionar modificações de um arquivo
git add ARQUIVO

## commit, criar uma versao
git commit -m "MENSAGEM"
git commit -am "MENSAGEM" ##adiciona e comita arquivos

## log, verificar mudanças
git log
git log --decorate
git log --author="Will"
git shortlog
git shortlog -sn
git shortlog --graph

## show
git show "ID do commit"

## verificar mudanças antes de passar pra modo STAGE
git diff
git diff --name-only

# Desfazendo coisas
## arquivo após modificacao:
git checkout "ARQUIVO" ##retorna arquivo pra antes da edição
## arquivo após ter sido adicionado para modo STAGE
git reset HEAD "ARQUIVO" ##retira arquivo do STAGE e volta pra modo pos edicao
## arquivo após ter sido comitado
git reset --soft "ID do commit" ##apaga o commit e deixa arquivo no modo STAGE
git reset --mixed "ID do commit" ##apaga o commit e deixa arquivo no modo edicao
git reset --hard "ID do commit" ##apaga o commit e mudancas dos arquivos

# ligando repositorio remoto
## primeiro criar projeto no GITHUB depois:
git remote add origin git@github.com:jackson-veloso/"NOME DO PROJETO" ##ideal é copiar a linha do proprio GITHUB
## para verificar
git remote
git remote -v

## enviar arquivos para o repositorio remoto
git push -u origin main 
git push -u origin master

## clonar repositorio remoto
git clone "REMOTO" "NOME LOCAL"
git clone git@github.com:jackson-veloso/comandos-git.git github-course-clone

## criar um Branch
git checkout -b "NOME"
git checkout -b testing
git branch #mostra os Branch existentes e qual vc está no momento
git branch -D "NOME"

## MERGE
git merge "BRANCH"

## REBASE
git rebase "BRANCH"

## STASH
git stash
git stash apply
git stash list

## ALIAS
git config --global alias."NOMEALIAS" "COMANDO"
git config --global alias.s status
git 

# TAG
git tag -a "VERSAO" -m "MENSAGEM"
git tag -a 1.0.0 -m "Readme finalizado" ##add tag repositorio local
git push origin master --tags ##envia tag para repositorio remoto
git tag -d "TAG"
git tag -d 1.0.0 #apaga tag no repositorio local
git tag origin :"TAG"
git push origin :1.0.0 #apaga tag no repositorio remoto

# REVERT
git revert "ID COMMIT"

# integrar vscode com github
https://imasters.com.br/desenvolvimento/use-git-com-interface-grafica-visual-studio-code-e-aumente-sua-produtividade




