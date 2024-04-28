#vcs #vcs/git 

> (Синхронизируемся с основной версией проекта)

**Делаем один раз - добавляем основной репозиторий в remote:**
`git remote add upstream git@gitlab.com:Volgarenok/spbspu-labs-aads-904-a.git`

**Синхронизируем свои репозитории так, чтобы в** ***рабочей ветке*** **были все последние изменения из** ***основного*** **репозитория:**

- Переключаемся на master-ветку в **локальном** репозитории
	`git checkout master`
- Скачиваем метаданные git-а из **основного** репозитория
	`git fetch upstream`
- Сливаем изменения из master-а **основного** репозитория в master **локального** – синхронизируемся с master-ом **основного** репозитория
	`git merge upstream/master`
- Синхронизируем master **локального** репозитория со **своим удаленным**
	`git push`
- Переключаемся на ветку с лабораторной
	`git checkout ivanov.petr/S1`
- Синхронизируем рабочую ветку с **локальным** master-ом
	`git merge master`
- Синхронизируем изменения в **локальной** ветке с соответствующей веткой в своем **удаленном** репозитории
	`git push`

```
git checkout master
git fetch upstream
git merge upstream/master
git push
git checkout romanovich.artem/
git merge master
git push
```

Обзываем коммит