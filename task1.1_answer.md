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

## 6.
$ git clone /home/evetaell/work/project1/ /home/evetaell/work/project13
Клонирование в «/home/evetaell/work/project13»…
готово.

## 7. 
Создала fileA и fileB. Изменила tast1.1_answer. 

git status
На ветке master
Ваша ветка обновлена в соответствии с «origin/master».
Изменения, которые будут включены в коммит:
  (используйте «git reset HEAD <файл>…», чтобы убрать из индекса)

	новый файл:    fileA.md
	новый файл:    fileB.md

Изменения, которые не в индексе для коммита:
  (используйте «git add <файл>…», чтобы добавить файл в индекс)
  (используйте «git checkout -- <файл>…», чтобы отменить изменения
   в рабочем каталоге)

	изменено:      task1.1_answer.md

git commit -m "Create fileA and fileB"

cd /home/evetaell/work/project1/
$ git pull project13 master

remote: Подсчет объектов: 4, готово.
remote: Сжатие объектов: 100% (2/2), готово.
remote: Total 4 (delta 0), reused 0 (delta 0)
Распаковка объектов: 100% (4/4), готово.
Из /home/evetaell/work/project13
 * branch            master     -> FETCH_HEAD
   fdc80f9..4553ce3  master     -> project13/master
Обновление fdc80f9..4553ce3
Fast-forward
 fileA.md | 1 +
 fileB.md | 1 +
 2 files changed, 2 insertions(+)
 create mode 100644 fileA.md
 create mode 100644 fileB.md

## 8.
git diff fileA.md
diff --git a/fileA.md b/fileA.md
index 0906b88..d3dce88 100644
--- a/fileA.md
+++ b/fileA.md
@@ -1 +1,2 @@
-String 1
\ No newline at end of file
+String 1
+String 2

git rm fileB.md
rm 'fileB.md'

$ git hist
* 56249b8 2017-07-30 | Change fileA, delete fileB (HEAD -> master) [Светлана Хмелева]
* 4553ce3 2017-07-30 | Create fileA and fileB (project13/master) [Светлана Хмелева]
* fdc80f9 2017-07-29 | Create file - task1.1_answer.md (ourPep/master) [Светлана Хмелева]

$ git push ourPep master
Username for 'https://github.com': evetaell
Password for 'https://evetaell@github.com': 
Подсчет объектов: 8, готово.
Delta compression using up to 4 threads.
Сжатие объектов: 100% (5/5), готово.
Запись объектов: 100% (8/8), 1001 bytes | 0 bytes/s, готово.
Total 8 (delta 1), reused 0 (delta 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/evetaell/my_project.git
   fdc80f9..56e8fe9  master -> master

## 9.
во втором

git add . 
evetaell@evetaell-To-be-filled-by-O-E-M ~/work/project13 $ git commit -m "Cgange task1.1_answer"
[master 5acedf1] Cgange task1.1_answer
 1 file changed, 78 insertions(+)
evetaell@evetaell-To-be-filled-by-O-E-M ~/work/project13 $ git log
commit 5acedf11918e976c5fd2348cfe3fdd0d215ad715
Author: Светлана Хмелева <hmeleva@reg.ru>
Date:   Sun Jul 30 08:38:25 2017 +0400

    Cgange task1.1_answer

commit 4553ce38de751ea75a21252b5bd63f56ca56d800
Author: Светлана Хмелева <hmeleva@reg.ru>
Date:   Sun Jul 30 00:27:17 2017 +0400

    Create fileA and fileB

commit fdc80f99e40e827edf189afdfc8e254383b043b7
Author: Светлана Хмелева <hmeleva@reg.ru>
Date:   Sat Jul 29 14:10:26 2017 +0400

    Create file - task1.1_answer.md

в первом
cd /home/evetaell/work/project1
evetaell@evetaell-To-be-filled-by-O-E-M ~/work/project1 $ git hist
* 56e8fe9 2017-07-30 | Change fileA, delete fileB (HEAD -> master, ourPep/master) [Светлана Хмелева]
* 4553ce3 2017-07-30 | Create fileA and fileB (project13/master) [Светлана Хмелева]
* fdc80f9 2017-07-29 | Create file - task1.1_answer.md [Светлана Хмелева]

во втором фикс правок

cd /home/evetaell/work/project13/
evetaell@evetaell-To-be-filled-by-O-E-M ~/work/project13 $ git add .
evetaell@evetaell-To-be-filled-by-O-E-M ~/work/project13 $ git commit --amend -m "Change task1.1_answer"
[master 6fc4de6] Change task1.1_answer
 Date: Sun Jul 30 08:38:25 2017 +0400
 1 file changed, 110 insertions(+)

git pull project13 master
remote: Подсчет объектов: 3, готово.
remote: Сжатие объектов: 100% (3/3), готово.
remote: Total 3 (delta 1), reused 0 (delta 0)
Распаковка объектов: 100% (3/3), готово.
Из /home/evetaell/work/project13
 * branch            master     -> FETCH_HEAD
   4553ce3..6fc4de6  master     -> project13/master

