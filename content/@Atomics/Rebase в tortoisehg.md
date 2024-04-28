#vcs #vcs/hg 

First enable rebase:

File -> Settings -> Extensions

![[Pasted image 20240108204151.jpeg]]

Then (after restarting tortoisehg)

1) Update to the changeset you <u>want to rebase on to</u>

![[Pasted image 20240108204205.jpeg]]

2) Right click on change you <u>want to rebase</u> and select the Modify History -> Rebase menu

![[Pasted image 20240108204218.jpeg]]

3) Click Rebase
4) Update на первоначальный коммит

And you should end up with something like this

![[Pasted image 20240108204245.jpeg]]

Warnings:
1) It's not usually a good idea to rebase a changeset with a public Phase
2) Avoid rebasing changes that are likely to produce complicated merge conflicts