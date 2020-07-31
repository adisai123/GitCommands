# GitCommands


1. git commit --amend   # rewrite commit

2. git log --oneline

3. git config  --global -e   || git config  --local -e

4. git difftool 184d9c4 5a61781

5. git reflog (all the history still avaliable even if amend override it)

6. git reflog expire --expire-unreachable=now --all (removes detached unreachable version)

6. git checkout 184d9c4

7. create new branch from existing brach: git checkout -b stage

8. to delete branch from local : git branch -D testdelete

9. squash : concept is while merging changes if there are multiple commit entries and if you want to clube them all together; while merging you can use merge and squash option available in gui.

10. alias : as name indicate you can create alias of git options 
	```bash 
	aditya@aditya-nupur:~/GOProjects/Aditya/src/github.com/GitCommands$ git config --global alias.onelinegraph 'log --oneline --graph --decorate'
	aditya@aditya-nupur:~/GOProjects/Aditya/src/github.com/GitCommands$ git  onelinegraph

	```
11. git fetch --prune    -- fetch from remote repo , any references delete from remote repo will also be deleted from my local machine
	git config --global fetch.prune true --- everytime you type git fetch , you need not to type --prune

12. Soft reset : git reset head
      It will simply unstage stagged changes.
