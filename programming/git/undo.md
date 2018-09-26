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

