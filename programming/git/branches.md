= git branches =
* branches are cheap
don't take lot of space, can be easily deleted
* one working directory
same directory where we work
* fast context switchin


Default branch is called master.
HEAD points to the last commit in current branch.

== creating branches ==
* git branch
list branches
current branch is marked with asterist
* cat .git/HEAD
where HEAD is pointing (or which branch is active)
* ls -la .git/refs/heads
has all branches
* cat /git/refs/heads/master
SHA of master


* git branch <branch_name>
create branch
* git checkout <branch_name>
switches to an existing branch
* git checkout -b <name>
create a new branch and immediately switch to it.
* git log --graph --oneline --decorate --all

you cannot switch to a different branch if you have any uncommitted conflicting changes. This includes modified files, but not untracked files. We can either scrap changes by checking out specific files, or commit changes, or stash changes, which is like a pocket where we save changes for later.

== comparing branches ==
* git diff master..<another_branch>
compare branches
* git diff --color-words <branch1>..<branch2>
* git diff --color-words <branch1>..<branch2>^
previous commit of branch2
* git branch --merged
to know if current branch contains another branch


== renaming, deleting branches ==
* git branch -m branch_name new_branch_name
renames branch
-m = --move
* git branch -d branch_to_delete
or --delete
use -D to force delete


== show branch on prompt ==
__git_ps1 is a function in git completion script that gives branch name prompt

export PS1='$(__git_ps1 "(%s")) > '
export PS1='\W$(__git_ps1 "(%s")) > '

put it inside import of git completion script

In Windows, put export statement in .bashrc in user directory.
