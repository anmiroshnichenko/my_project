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
    git checkout 5dbc984  - переключение между  коммит  (хеш)
    git log  --oneline --all   -  посмотреть историю 
    git checkout main   -вернутся на пследний коммит
    git remote -v  проверить  связь с удаленным репозиторием
    git remote add origin git@github.com:anmiroshnichenko/my_project.git     - связать с удаленным репозиторием
###  Настроить  разрешения для ssh ключа 
    chmod 600 ~/.ssh/id_rsa
      
    git push -u origin main   
    git push -u origin new-branch
		 

## Клонировать репозиторий
	git clone git@github.com:anmiroshnichenko/my_project.git	

## Ветвление в Git
  ### Посмотреть существующие ветки в репозитории
        git branch
  ### Создать новую ветку
        git branch  new-branch  
  ### Переключится на новую ветку
        git checkout new-branch 
  ### Просмотр истории проекта в новой ветке 
        git log new-branch --oneline
  ###  Сливать изминения из одной ветки в другую (из ветки new-branch >  в ветку main)
        git checkout main 
        git merge new-branch


