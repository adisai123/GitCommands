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

13. hard reset :  git reset  --hard
aditya@aditya-nupur:~/GOProjects/Aditya/src/github.com/GitCommands$ > info3.txt
aditya@aditya-nupur:~/GOProjects/Aditya/src/github.com/GitCommands$ git clean -d -x -f
Removing info3.txt
aditya@aditya-nupur:~/GOProjects/Aditya/src/github.com/GitCommands$ 

clean command will clean new untracted files.

safe way is to use -i instead of -d : git clean -d -x -i

14. Hard reset on previous commit : Its harmful , as it will  completly wipe out changes and also history 
    git reset 719a49e --hard

15. Revert (history will be get created or intacted) 
    git revert <version> # version can be HEAD or any hash number

16. Rebase: to make your branch up to date with master or any other branch 
  1. git checkout master
  2. git pull master
  3. git checkout mybranchname
  4. git rebase master

17. cherrypick: 





# config:   

    to edit config:
git config --global -e
git config --local -e

```
[merge]
    tool = vscode
[mergetool "vscode"]
    cmd = code --wait $MERGED
[diff]
    tool = vscode
[difftool "vscode"]
    cmd = code --wait --diff $LOCAL $REMOTE
[credential]
        helper = store

```