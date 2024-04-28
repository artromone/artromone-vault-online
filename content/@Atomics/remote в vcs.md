#vcs/git #vcs 

По умолчанию склонируется только одна ветка (главная)
Можно склонировать все, используя `--no-single-branch`

```bash
git branch --all

* master
remotes/origin/HEAD -> origin/master
remotes/origin/another_fix_branch
remotes/origin/master
remotes/origin/new_feature
```

Имя `remote` тут – `origin`

`remote` – ссылка с локального репозитория к оригинальному. "Адрес к другому репозиторию git"

![[Pasted image 20240412214725.jpeg]]

После выполнения `git checkout another_fix_branch`:
```
Branch another_fix_branch set up to track remote branch another_fix_branch
➥ from origin.
Switched to a new branch 'another_fix_branch'
```

Возникает две ссылки на `another_fix_branch`

![[Pasted image 20240412215448.jpeg]]

На самом деле происходит `git checkout -b another_fix_branch remotes/origin/another_fix_branch`

> Локальная ветка теперь отслеживает удаленную ветку


```
$ git remote -v show
origin c:/Users/Rick/Documents/gitbook/math.git (fetch)
origin c:/Users/Rick/Documents/gitbook/math.git (push)

❯ git remote -v show  
origin  git@github.com:artromone/ginsengine.git (fetch)  
origin  git@github.com:artromone/ginsengine.git (push)
```

remote может быть директорией на компьютере, или сервер в интернете

Переименовать можно: `git remote rename origin beginning`

