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
* git rm -r folder
Mark folder for removal recursively
* git mv file1.txt file2.txt
moving/renaming
* git commit -am 'message'
adds and commits in one go. It doesn't include untracked and deleted files.
* git add directory/ = git add directory/*


* [[checking_changes]]
== committing changes ==
* git commit -m 'message'

* [[logs]]
* [[undo]]
* [[ignoring]]
* [[navigating]]



* [[branches]]
== branches ==
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










https://try.github.io/levels/1/challenges/1
https://git-scm.com
