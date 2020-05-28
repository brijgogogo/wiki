= fzf =
Fuzzy finder
- The letters used in search have to appear in that order, but don't have to be adjacent
  eg. tosearch file table-of-contents.js : search by tocj
- Fuzzy finder also sorts the results using a ranking algorithm

== Functionalty from FZF ==
:FZF   : look for files under current directory
:FZF   : look for file in home directory
:FZF!  : starts fzf in full screen mode

<c-t> : open selected file in new tab
<c-x> : open in horozontal split
<c-v> : open in vertical split


== what files to include ==
By default, fzf builds a list of all the files beneath your current working directory. It generates that list of files using a variation of "find . -type f" command.

You can set FZF_DEFAULT_COMMAND environment variable to the command that will be used instead of default command.
e.g: export FZF_DEFAULT_COMMAND='git ls-files'
(git ls-files: considers .gitignore file to not include ignored files)
If using "git", it won't work when out of version control repository or files are not yet added to git index.

Use Ripgrep:
e.g: export FZF_DEFAULT_COMMAND='rg --files'
It filters out files marked ignore in Git and also includes files not yet added to git index.

== source and sink ==
Fzf works on a list of items to be filtered. This list is called "source", and action to be performed on the selected result is called the "sink". FZF can work to find buffers, ex command from history, etc.

== FZF.vim ==
https://github.com/junegunn/fzf.vim
:FZF : open fzf picker interface
* <c-j> or <c-k>: move up down from listed items
* <C-c> : dismiss fzf picker interface
* <CR>: triggers default action (open)
* <C-x>, <C-v>, <C-t>: open file in horizontal split, vertical split, new tab
* :Files [Path] : same as :FZF
* :Buffers   : open buffers
* :Colors color schemes
* :Ag [Pattern] : ag search result (alt-a to select all, alt-d to deselect all)
* :Lines [Query] : lines in loaded buffers
* :Marks
* :Windows
* :History
* :History/   : search history
* :Snippets  : Ultisnips snippets
* :Maps
* :FileTypes



== sources ==
https://github.com/junegunn/fzf/blob/master/README-VIM.md
