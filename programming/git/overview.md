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
* [[stash]]
* [[remotes]]
* [[aliases]]
* [[gui_tools]]
* [[git_hosting]]
* git_flow
* git_modules
* gitignore

== sources ==
https://try.github.io/levels/1/challenges/1
https://git-scm.com
https://www.linkedin.com/learning/git-essential-training
