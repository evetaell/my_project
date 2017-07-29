# Ответы на упражнения

## 1. 

Создала в директории /home/evetaell/work каталог project1

$ cd /home/evetaell/work/project1
$ git init

## 2. 
$ git config --global user.name "Светлана Хмелева"
$ git config --global user.email hmeleva@reg.ru

$git config --list

user.name=Светлана Хмелева
user.email=hmeleva@reg.ru
core.autocrlf=input
core.safecrlf=true
core.repositoryformatversion=0
core.filemode=true
core.bare=false
core.logallrefupdates=true
alias.co=checkout
alias.ci=commit
alias.st=status
alias.br=branch
alias.hist=log --pretty=format:"%h %ad | %s%d [%an]" --graph --date=short
alias.type=cat-file -t
alias.dump=cat-file -p
remote.ourPep.url=https://github.com/evetaell/my_project.git
remote.ourPep.fetch=+refs/heads/*:refs/remotes/ourPep/*

## 3. 
1. Зарегистрировалась на гитхаб
2. Создала новый проект
3. git remote add ourPep https://github.com/evetaell/my_project.git
4. git remote -v
   * ourPep	https://github.com/evetaell/my_project.git (fetch)
   * ourPep	https://github.com/evetaell/my_project.git (push)
5. git push ourPep master

## 4. 

Создала в репозитории файл task1.1.md, скопировала в него текст этого задания.

$git status

На ветке master
Начальный коммит
Неотслеживаемые файлы:
  (используйте «git add <файл>…», чтобы добавить в то, что будет включено в коммит)
	task1.1.md

Создала файл .gitignore, внесла туда task1.1.md

$git status

На ветке master
Начальный коммит

## 5. 

Создала в репозитории файл task1.1_answer.md, внесла все выполненные задания.

evetaell@evetaell-To-be-filled-by-O-E-M ~/work/project1 $ git add .
evetaell@evetaell-To-be-filled-by-O-E-M ~/work/project1 $ git add .
evetaell@evetaell-To-be-filled-by-O-E-M ~/work/project1 $ git commit -m "Create file - task1.1_answer.md"[master (корневой коммит) ca52e25] Create file - task1.1_answer.md
 1 file changed, 65 insertions(+)
 create mode 100644 task1.1_answer.md
evetaell@evetaell-To-be-filled-by-O-E-M ~/work/project1 $ git status
На ветке master
нечего коммитить, нет изменений в рабочем каталоге


