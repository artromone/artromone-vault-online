#vcs/git #vcs 

![[Pasted image 20240413160144.jpeg]]

![[Pasted image 20240413160522.jpeg]]

```
fatal: The current branch new_branch has no upstream branch.
To push the current branch and set the remote as upstream, use

git push --set-upstream origin new_branch
```

![[Pasted image 20240413162421.jpeg]]

Удалить ветку:
- Локально:
	- Если была слита с другой веткой: `git branch -d new_branch`
	- Если не была слита с другой веткой: `git branch -D new_branch`
- В удаленном репозитории:
	- `git push origin :new_branch`
	- `git push origin --delete new_branch`

push.default настройка

| push.default | value                                                                            |
| ------------ | -------------------------------------------------------------------------------- |
| nothing      | Don’t push unless a source and a destination are specified.                      |
| current      | Push current branch to update a branch with the same name.                       |
| upstream     | Similar to current.                                                              |
| simple       | Similar to upstream, but check that the branch name matches what<br>is upstream. |
| matching     | Push all branches that have corresponding branches on the remote.                |
