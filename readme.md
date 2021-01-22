
Repositório sobre o curso de Git e GitHub.

=)


$ git config --global alias.co checkout
$ git config --global alias.br branch
$ git config --global alias.ci commit
$ git config --global alias.st status

*Configurar nome do usuário
	-> git config --global user.name "Hudson Carlos"

*Configurar e-mail do usuário
	-> git config --global user.email "hudsonscarlos@outlook.com"

*Configurar editor de codigo padrão
	-> git config --global core.editor subl

*Criando Alias (Atalhos)
	-> git config --global alias.s status
	
*Para inserir texto em um arquivo pelo prompt
	-> copy con note.txt

*Visualiza informações de configuração do git
	-> git config user.name
	-> git config user.email
	-> git config core.editor
	-> git config --list

*Criar pasta para começar o controle de versão
	-> mkdir git-course

*Entrar em uma pasta criada
	-> cd git-course
	
*Para iniciar o controle de versão na pasta desejada, entre na pasta e em seguida digite o comando
	-> git init
	
*Reporta como estão os status das pastas neste momento
	-> git status
	
*Adicionar arquivo ao git 
	-> git add Readme.md

*Commitando arquivos, neste momento é criado uma imagem dos arquivos, uma versão.
	-> git commit -m "Add Arquivo Readme.md" 
	-> git commit -am "Add Arquivo Readme.md"
	
*Visualizando logs do controle de versão
	-> git log
	-> git log --decorate
	-> git log --author="Hudson"
	-> git shortlog
	-> git shortlog -sn
	-> git log --graph

*Visualizando registros de log pela hash	
	-> git show 00d440ed8bb739d2937be5e59376b7b1e04da061

*Visualizando restros de edição antes do commit
	-> git diff
	-> git diff --name-only
	
*Para desfazer uma alteração, antes do commit é claro
	-> git checkout "Comando Git.txt"
	
*Para desfazer o staged, ou seja depois que a alteração foi adicionada 
	-> git reset HEAD "Comando Git.txt"
	
*Para desfazer um commit 
	**soft	- Ele desfaz a ultima hash que foi comitada e o arquivo volta para staged fica proto para ser comitada novamente
	**mixed	- Ele desfaz a ultima hash que foi comitada e o arquivo volta para modified
	**hard	- Ele desfaz a ultima hash que foi comitada e todas as alterações

	-> git reset --soft 723b87a4c20627a294b39028a44a68b274321cfe	- Mata o commit e volta os arquivos para staged.
	-> git reset --mixed 723b87a4c20627a294b39028a44a68b274321cfe	- Mata o commit e volta os arquivos para antes do staged modified.
	-> git reset --hard 723b87a4c20627a294b39028a44a68b274321cfe	- Mata o commit e qualquer alteração, um reset bem bruto.
	
*Para usar o revert (Outra forma de reverter um commit assim como reset)
	-> git revert 723b87a4c20627a294b39028a44a68b274321cfe	
	
*Para adicionar um link de uma pasta remota no github
	-> git remote add origin git@github.com:HudsonCarlos/github-course.git
	-> git remote add origin https://github.com/HudsonCarlos/Cursos.git
	-> git remote add origin https://github.com/HudsonCarlos/CheckList.git

*Para criar uma chave SSH
	-> ssh-keygen -t rsa -b 4096 -C "hudsonscarlos@outlook.com"
	
*Para adicionar arquivos e logs ao repositório remoto do github
	-> git push -u origin master 
	
*Listando repositório remoto
	-> git remote
	-> git remote -v

*Da um Get no repositório para buscar as ultimas atualizações.
	-> git pull	origin "Branch"
	
*Renomeando repositório remoto
	-> git remote rename teste origin

*Clonando um repositório remoto
	-> git clone git@github.com:HudsonCarlos/Cursos.git
	-> git clone https://github.com/HudsonCarlos/Cursos.git
	-> git clone https://github.com/HudsonCarlos/CheckList.git

*Criando um branch
	-> git checkout -b testing

*Criando um branch com Git Flow
	git flow feature start Criacao_Projeto	

*Listar todos os branch
	-> git branch

*Para mudar de branch
	-> git branch master <-(Nome do branch )
	-> git checkout master <-(Nome do branch )

*Para apagar um branch local e remoto
	-> git branch -D testing
	-> git push origin :testing

*Para criar um merge
	-> git merge "merge"	

*Para criar um rebase 
	-> git rebase "master"
	
*Para criar um stash (quando eu não terminei um arquivo e não quer adicionar ele ao meu branch eu uso stash)
	-> git stash

*Para aplicar as mudanças que eu tinha feito nos arquivos guardados em stash
	-> git stash apply 
	
*Para listar todos os stash que eu estiver fazendo
	-> git stash lists
	
*Para limpar todos os stash que estiver guardado
	-> git stash clear

*Para criar uma tag (uma separação maior tipo uma nova versão do projeto)
	-> git tag -a 1.0.0 -m "Readme finalizado"

*Para visualizar todas as tag criada
	-> git tag
	
*Para subir uma tag para o repositório remoto
	-> git tag -a 1.0.0 --tags

*Para apagar tag local e remoto
	-> git tag -d 1.0.2
	-> git push origin :1.0.2

* Realizar merge para o develope Git Flow
	-> $ git flow feature finish Criacao_Projeto  (Para sair do Vim ":x")

* Enviando alterações para o servidor
	-> $ git push origin develop

