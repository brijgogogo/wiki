NeoVim uses ~/.config/nvim folder
NeoVIm uses ~/.config/nvim/init.vim file instead of ~/.vimrc file for configuration
:command (get list of user-defined commands)

:Explore (opens file explorer window)
Select a file or directory name and press Enter to open that file or directory.
To return to the explorer window, press Ctrl-^ (usually Ctrl-6).
You can also "edit" a directory to explore that directory. For example, :e .. lists files in the parent directory.

c-x, c-o to show auto-complete list in vim
Vim comes with an auto complete of ctrl+p and ctrl+n. It is for the variables and functions you have written.

:!ls (to run shell commands from vim)
:r!date (to put output of shell command in current document)

:pwd (to see directory from where vim is operating)
:verbose map <key> (to find key-mapping)
:map (to display list of keys that are currently mapped)
* :copen (to see results of grep, errors, etc)
:sort (select some lines, then :sort to sort them)
vat (visually select a tag)
dat (delete a tag)
To paste in comand mode use <C-R>"p


Misc
:version (to see location of vimrc file)
:set gfn? (see font used)
:h gui

:set hls! (toggles boolean flag hlsearch)
:set history& (set back to default value)
z <CR> (makes the current line, first line in editor)

:color Ctrl+d (to see color schemes available)

Reload vimrc
:source .vimrc (to run vim command from a files)

gg=G
Format code of whole page (gg > go to top, = > fix indentation, G > till the end
of file)

g& (replease last :s command)


https://github.com/tpope/vim-surround/blob/master/doc/surround.txt
https://raw.githubusercontent.com/mattn/emmet-vim/master/TUTORIAL

//use these for project searching
https://github.com/ggreer/the_silver_searcher
https://github.com/mileszs/ack.vim

https://dougblack.io/words/a-good-vimrc.html

https://github.com/mhinz/vim-galore

:scriptnames list all the .vim files that Vim loaded for you, including your .vimrc file.
:e $MYVIMRC open & edit the current .vimrc that you are using, then use Ctrl + G to view the path in status bar.
https://github.com/tpope/vim-sensible/blob/master/plugin/sensible.vim
https://github.com/VundleVim/Vundle.vim

ntpeters/vim-better-whitespace
:ToggleWhitespace
:StripWhitespace

vim-gitgutter
[c, ]c to move between hunks
:GitGutterToggle

https://github.com/vim-syntastic/syntastic

https://github.com/janko-m/vim-test
di' (delete text inside ' around the cursor)

https://github.com/wellle/targets.vim
https://github.com/junegunn/fzf.vim
:Files
:Colors

https://github.com/myusuf3/numbers.vim
nnoremap <F3> :NumbersToggle<CR>
nnoremap <F4> :NumbersOnOff<CR>

https://www.cheatography.com/stepk/cheat-sheets/vim-nerdtree/

Vim
=G  (indent all file)
== (indent single line)

https://sanctum.geek.nz/arabesque/buffers-windows-tabs/
:ls (list buffers)
:split /path/to/file
:vsplit /path/to/file
:tabn (move to next tab)
:tabp (move to previous tab)

https://github.com/jistr/vim-nerdtree-tabs
:NERDTreeTabsToggle

Jump List
Ctrl + o (to jump back to previous location) 
Ctrl + i  (to jump forward) 
:jumps (display jump list for current window)

:set ignorecase (case insensitive search)
:set noignorecase (edited)

https://github.com/w0rp/ale


:Loremipsum!wordcount
I (toggles hidden files in NERDTree)
:%s/search/replace/g   (search, replace in entire file)

:8,10 s/search/replace/g
:s/search/replace/
:%/search/replace/gc  (confirm before replace)
