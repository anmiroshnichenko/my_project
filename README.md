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
	git push -u origin main   
		chmod 600 ~/.ssh/id_rsa - настроить  разрешения для ключа 
