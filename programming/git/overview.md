= GIT =

https://try.github.io/levels/1/challenges/1

* git config --global user.email "brijgogogo1@gmail.com"
* git config --global user.name "Brij Sharma"
%% to set identity of user
* git config --global user.name
%% to view value

* git clone <url>

* git init
%% To initialize Git in a repository

* git remote -v
%% View the origin
%% If you’re using GitHub and you’re pushing code to a GitHub repo that’s stored
%% online, you’re using a remote repo. The default name (also known as an alias)
%% for that remote repo is origin.

* git remote add origin <URL>


* git remote set-url origin <newurl>
%% To change url

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

* git status
* git diff fileName.ext
%% to see what you haven't git added yet
* git diff --cached fileName.ext
%% to see already added changes
* git diff --stat

* git log

* git add '*.txt'

* git add -A
%% adds everything

* git add .
%% add changes in current directory

* git push -u origin master
%% The name of our remote is origin and the default local branch name is master.
%% The -u tells Git to remember the parameters, so that next time we can simply
%% run git push and Git will know what to do.

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

* git rm '*.txt'
%% Remove file form disk and stage them for removal

* git rm -r folder
%% Mark folder for removal recursively

* git branch -d branchB
%% To delete the branch. It won't work if the branch to delete has something
%% that hasn't been merged. You can either add the --force (-f) option or use -D which combines -d -f together into one command.


* git config --list
List settings

* git config user.name
See a setting

* git commit --amend
%% change commit message
