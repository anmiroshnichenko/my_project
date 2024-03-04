##  Глобальные настроки

    git config --global user.name "Aleksandr Miroshnichenko"
    git config --global user.email "alexand.miroshnichenko@yandex.ru"
    git config --global --list 

    ## Правильное окончание строк для Linux, Mac OS
    git config --global core.autocrlf input 
    git config --global core.safecrlf warn
    
    ##  ДЛЯ WINDOWS  
    git config --global core.autocrlf true
    git config --global core.safecrlf warn

## Дальше общая для всех операционных систем команда, которая позволит избежать нечитаемых строк в неправильной кодировке:
    git config --global core.quotepath off

## Задайте общепринятое название основной ветки в репозитории в Git — main
    git config --global init.defaultBranch main
    git help -g  #справка       
    git init  # создать локальный ропозиторийgit
    git status
    git add  README.md   -добавить файл для отслеживания
    git commit -m "Initial commit"
    git commit -am "update README.md"    добавлени е и commit одной командой 
    git log     посмотреть полную  историю 
    git commit --amend -m "add date"   изменить   коммит 
    git add -A  # добавить все новые файлы
    git commit --amend -m "add file error"   # добавить файл в предыдущий коммит
    git checkout хеш коммита
    git checkout 5dbc984  - переключение между  коммит  (хеш)
    git log  --oneline   -  посмотреть историю 
    git log --oneline --all  -  посмотреть всю  историю 
    git checkout main   -вернутся на пследний (текущий) коммит
    git remote -v  проверить  связь с удаленным репозиторием
    git remote add origin git@github.com:anmiroshnichenko/my_project.git     - связать с удаленным репозиторием
    git remote add target git@github.com:anmiroshnichenko/earlyorder.git
    git push -u origin main  
    git push -u target main
    git push -u origin new-branch  
  ###  Настроить разрешения для ssh ключа 
    	chmod 600 ~/.ssh/id_rsa
## Обновить локальный репозиторий  с  удаленного 
	git pull
## Клонировать репозиторий
        git clone git@github.com:anmiroshnichenko/my_project.git        
## Ветвление в Git
  ### Посмотреть существующие ветки в репозитории
        git branch
  ### Создать новую ветку
        git branch  new-branch
  ### Посмотреть все ветки  
        git branch -a
  ### Создать новую ветку и переключиться на нее       
        git checkout -b fix
  ### Переключится на новую ветку
        git checkout new-branch 
  ### Просмотр истории проекта в новой ветке 
        git log new-branch --oneline
  ###  Сливать изминения из одной ветки в другую (из ветки new-branch >  в ветку main)
        git checkout main 
        git merge new-branch
        git commit -am 'Conflict resolved'
   #### Для слияния не нужно клонировать удалённые ветки в локальный репозиторий. Можно выполнить команду
        git merge origin/earlyorder
   ### Отменяет изменения, которые были внесены в последний коммит
		git revert
		
		
##  Настройка .gitignore
  ### если файл проиндексирован:  
	1 Добавьте нужное правило в .gitignore
	2 Уберите файл из индекса, удалите из отслеживаемых. 
	  Для этого воспользуйтесь командой git rm --cached имя-файла. При помощи команды git rm с ключом --cached мы удаляем файл из индекса,
	  из отслеживаемых, но оставляем его на компьютере
	3 Теперь сработает правило игнорирования и Git перестанет следить за файлом или папкой
	### правила заполнения файла  .gitignore:		
		- README.md ← будет игнорировать только файл с таким именем
		- *.md ← будут проигнорированы все файлы с расширением .md на конце
		- private/todo.md ← будет проигнорирован файл todo.md, находящийся в папке private

             
