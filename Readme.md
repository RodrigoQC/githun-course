# Git Course

Este é um repositorio teste para mostrar como o git funciona

saiba mais em [willianjusten.com.br](http://willianjusten.com.br)

Gostou do curso? Quer mais? Ajude com uma doação, até um café é valido =)

[Meu FaceBook](https://www.facebook.com/rodrigo.q.decastro)

outros cursos em :[wilian justen cursos](http://willianjusten.teachable.com)

# Minhas anotações durante o curso

git status 
verifica o estado dos arquivos(versão)

git add NOMEDOAQUIVO.EXTESÃO
adiciona um arquivo a versão

git commit -m " COMENTARIO ..."
criar uma versão com um comentario para ajudar a entender o que foi mudado

-------------------------------------------------

git commit -am " COMENTARIO ..."
cria um commit sem ter que adicionar os arquivos para criar a versão

-------------------------------------------------

git log 
mostrar todos os commit

git log --author="Exemplo"
mostra todos os commit que tem nome "Exemplo"

git shortlog
mostra os autores e quantos commit fizeram e seus comentarios

git shortlog -sn
mostra quantos commit cada autor fez

git log --graph
mostrar todos os commit com um grafico

-------------------------------------------------

git show HASH_DO_COMMIT
mostra as auterações feitas naquele commit

-------------------------------------------------
git push
envia os arquivos adicionados/atulizados para o repositorio remoto

-------------------------------------------------

git diff
mostra o que foi mudado dentro dos arquivos

git diff --name-only
mostra somente o nome do arquivos que foram alterados

-------------------------------------------------

git checkout NOMEDOAQUIVO.EXTESÃO
ele remove as alterações feitas no arquivo

git reset HEAD NOMEDOAQUIVO.EXTESÃO
ele remove o arquivo que foi adicionado, mas não remove as alterações feitas no arquivo

git reset --soft HASH_DO_COMMIT_QUE_SERÁ_O_QUE_VOLTARA
ele volta um commit mas com os arquivos com as mesmas modificações e ja adicionados para commit

git reset --mixed HASH_DO_COMMIT_QUE_SERÁ_O_QUE_VOLTARA
ele volta um commit mas com os arquivos com as mesmas modificações

git reset --hard HASH_DO_COMMIT_QUE_SERÁ_O_QUE_VOLTARA
ele volta o commit e iguinora o que foi feito nele

-------------------------------------------------

git clone SSH_DO_REPOSITORIO_CLONADO  NOME_PARA_O_NOVO_REPOSITORIO
comando para clonar um repositorio

-------------------------------------------------

git checkout -s NOME_DO_BRANCH_A_SER_CRIADO
ele cria um branch

git branch
mostra os branch criados, e com um asterisco no branch que está acessando no momento

git checkout NOME_DO_BRANCH
esse comando muda do branch atual para o  branch determinado

git branch -D NOME_DO_BRANCH
esse comando apaga um branch

-------------------------------------------------

git rebase NOME_DO_BRANCH
execute esse comando dentro do master, esse comando junta os branchs

git merge NOME_DO_BRANCH
execute esse comando dentro do master, esse comando cria um novo branch e junta os branchs

-------------------------------------------------

## git ignore
como o proprio nome ja diz ele serve para que o git ignore os arquivos com nome escritos dentro do arquivo dentro do arquivo ".gitignore"
Ex: teste.txt
	bloqueio o arquivo especifico
	*.txt
	bloqueia todos os arquivos com a extenção .txt

-----------------------------------------------------------------------------------------------------------------------------------------------------------------

git stash
ele guarda as modificações feitas(ele não é um commit) nos arquivos

git stash apply
ele mostra as modificações feitas nos arquivos que estavam guardadas

git stash list
mostra a lista de todos os stash que esta fazendo

git stash clear
limpa todos os stash que estão fazendo

-------------------------------------------------
## Alias
ele serve para criar atalho para um comando

git config --global alias.NOME_ATALHO  COMANDO

Ex: git config --global alias.s status

-------------------------------------------------
## Tags


git tag -a 1.0.0    -m "Readme finalizado"
		   versão       Comentario
Cria uma tag
		   	   
git push origin master --tags
envia a tag para o git hub

git tag
mostra as tags criadas

git tag -d VERSÃO_DA_TAG
paga a tag  local

git push origin :VERSÃO_DA_TAG
paga a tag do repositorio


-------------------------------------------------
## Reverte

git revert HASH_DO_COMMIT
ele reverte o commit mas ele não destroi o código commit
