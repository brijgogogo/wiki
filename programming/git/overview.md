= GIT =
version control system (VCS)
source code management (SCM)

* [[history]]
* [[distributed]]
* [[cofiguration]]
* [[auto-completion]]
* [[help]]
* [[architecture]]
* [[git-checksum]]
* [[head-pointer]]

* git --version

== initializing git repository ==
* git init
make git repository


== staging changes ==
* git add .
add all changes in current directory
* git add '*.txt'
* git add file_name.ext
* git add -A
adds everything
* git rm file_to_delete.ext
add the file to remove to staging index
* git rm '*.txt'
remove files form disk and stage them for removal
* git mv file1.txt file2.txt
moving/renaming
* git commit -am 'message'
adds and commits in one go. It doesn't include untracked and deleted files.
* git add directory/ = git add directory/*


== checking changes ==
* git status
Lets us know about the difference between working directory, staging index and repository
* git diff
compare what's in repository (the version that out HEAD pointer is pointing at) vs what's in our working directory
* git diff fileName.ext
to see changes not yet staged in a specif file
* git diff --staged
to see all changes staged
* git diff --cached fileName.ext
old version of --staged
* git diff --stat
* git diff --color-words file.ext
show changed words (instead of line)

== committing changes ==
* git commit -m 'message'

== logs ==
* git log
* git log -n 5
view recent 5 commits
* git log --since=2018-09-15
* git log --until=2018-09-15
* git log --author="Brij"
* git log --grep="Init"


== undo changes done at working directory ==
* git checkout -- file.ext
undo the changes done in file.ext in working directory by getting it from repository
-- means to stay on current branch (we do not want branch)
`checkout` is used to get branch as well, if folder and branch names are same, then it will get the branch, so to stay in current branch use --
* git clean -n
test runs git clean -f
* git clean -f
removes anything in working directory that is not in our repository (untracked)


== undo changes done at staging directory ==
* git reset HEAD file.ext
reset the staging index from repository at HEAD. The staging index gets the file from repository until HEAD.
It removes the staged file.ext from staging index


== undo changes done at repository ==
* git commit --amend -m 'new message'
change commit message
only last commit is allowed to be changed as changing previous commits would need the SHA to be changed/recomputed for all the following commits. Last commit doesn't point to anything so it can be easily amended.
* git checkout <full or partial SHA> -- file.ext
checkout file with a specifc revision
After taking checkout, file will show modified, then you can commit it (reverting to previous revision)
* git revert <full or partial SHA>
reverts change from a revision, and commits
* see git reset below

== git reset ==
moves the HEAD pointer to specific commit
reset types:
1. --soft
does not change staging index or working directory
2. --midex (default)
changes staging index to match repository
does not change working directory
3. --hard
changes staging index and working directory to match repository

* cat .git/HEAD
check HEAD pointer
* cat .git/refs/heads/master
check master HEAD pointer
* git reset --soft <full or partial SHA>
* git reset --mixed <full or partial SHA>
* git reset --hard <full or partial SHA>

== ignoring files ==
create .gitignore files at root directory and commit
we can use regular expressions like * ? [aeiou] [0-9]
we can negate expressions with !
for comments use #
blank lines are ignored
examples:
*.php
!index.php
assets/directory/
!assets/directory/tour_*.mp4
tempfile.txt
# comment
log/*.log
log/*.log.[0-9]

https://help.github.com/articles/ignoring-files
https://github.com/github/gitignore

== globally ignoring files ==
git config --global core.excludesfile ~/.gitignore_global
Not committed. Is as per user/operating system generated files.

== ignoring tracked file ==
git will not ignore already tracked file, even if it later added to .gitignore
* git rm file.ext
* git rm --cached file.ext
remove file from staging index.
git will start ignoring the file, still keep the file in repository and working directory

== tracking empty directories ==
git does not track empty directories, git is designed to be a file-tracking system.
To track empty directory, people use a trick to add a file like .gitignore or .gitkeep with no contents or comments

== branches ==
Default branch is called master.
* git branch
%% lists all branches on your local machine

* git branch <name>
%% Create a branch

* git checkout <name>
%% switches to an existing branch

* git checkout -b <name>
%% create a new branch and immediately switch to it.

* git merge <branch>
%% Merge another branch into current branch

* git pull origin <branch>
* git push -u origin master
%% The name of our remote is origin and the default local branch name is master.
%% The -u tells Git to remember the parameters, so that next time we can simply
%% run git push and Git will know what to do.
* git branch -d branchB
%% To delete the branch. It won't work if the branch to delete has something
%% that hasn't been merged. You can either add the --force (-f) option or use -D which combines -d -f together into one command.



* git clone <url>

%% To initialize Git in a repository

* git remote -v
%% View the origin
%% If you’re using GitHub and you’re pushing code to a GitHub repo that’s stored
%% online, you’re using a remote repo. The default name (also known as an alias)
%% for that remote repo is origin.

* git remote add origin <URL>


* git remote set-url origin <newurl>
%% To change url






* git pull origin master

* git stash
%% Sometimes when you go to pull you may have changes you don't want to commit
%% just yet. One option you have, other than commiting, is to stash the changes.
%% Use the command 'git stash' to stash your changes, and 'git stash apply' to
%% re-apply your changes after your pull.

%% The HEAD is a pointer that holds your position within all your different
%% commits. By default HEAD points to your most recent commit, so it can be used
%% as a quick way to reference that commit without having to look up the SHA.

* git diff HEAD
%% What is different from our last commit

* git diff --staged
%% To see the changes you just staged

* git reset filename.ext
%% To unstage file
%% After unstaging file will still be there with changes.


* git checkout -- file.ext (edited)
%%Files can be changed back to how they were at the last commit using git checkout -- <target>:


* git rm -r folder
%% Mark folder for removal recursively



https://try.github.io/levels/1/challenges/1
https://git-scm.com
