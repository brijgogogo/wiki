== Things to check ==
* Syntastic
* ternjs
* YouCompleteMe
* mxw/vim-jsx
* pangloss/vim-javascript
* deoplete
* vim-dadbod
* https://github.com/w0rp/ale
* ack.vim and ag
* vim-gitgutter, vim-fugitive, vim-rhubarb
* lightline
* vim-commentary
* vim-polyglot
* repeat.vim
* closetag.vim
* endise - ruby
* sleuth.vim
* yourcompleteme
* Repeat.vim
* SystemCopy
* TitleCase
* text-obj wiki
* replaceWithRegister
* Commentry
*

= Vim Topics =
* [[statusline]]
* [[Code Folding]]
* [[Searching]]
* [[vim-navigation]]
* [[Quick Editing]]
* [[Visual Mode]]
* [[Indenting]]
* [[General]]
* [[Buffers]]
* [[Windows]]
* [[Tabs]]
* [[Macros]]
* [[Netrw]]
* [[vim-vinegar]] for use with Netrw
* [[CTags]]
* [[Sessions]]
* [[CtrlP]]
* [[Jump List]]
* [[Change List]]
* [[vim-markers]]
* [[Registers]]
* [[Themes]]
* [[Text-Objects]]
* [[vim_settings]]
* [[mappings]]
* [[vim-reg-ex]]
* [[vim-functions]]
* [[vim-auto-completion]]
* [[vim-abbreviations]]
* [[vim_other_tips]]
* [[vimdiff]]
* [[clipboard]]

* set ft=text

== Plugins ==
* [[vim-surround]]
* [[vim-unimpaired]]
* [[Emmet Vim]]
* [[NerdTree]]
* [[Vimwiki]]
* [[fzf]]
* [[calendar.vim]]

== Plugin Managers ==
* [[vim-plug]]
* [[minpac]]


:py print 2*2


* [[.net_in_vim]]

:messages
:version
:e
* g + Ctrl + g
see info of file: number of words, line, etc.

bestofvim.com
reddit.com/r/vim
http://learnvimscriptthehardway.stevelosh.com/
vimgolf.com

:h todo.txt
:help user-manual

* Ctrl+S : freezes vim (it is scroll-lock in Linux Termial), use Ctrl+Q to unfreeze
* Ctrl+V u <FA unicode number >

* :help defaults.vim
check defaults
* :filetype
check filetype detection
* vim --version

jump to specific line number
vim myfile.txt +28

* :py3 print('hello')
executes the specified command using a Python 3 interpreter

* [[vim_vs_neovim]]

:echo join(split(&runtimepath,','),"\n")
see runtimepath values

== vim plugins ==
A package is a directory that contains one or more plugins.
A plugin is a directory that contains one or more scripts.
A script is a standalone file containing instructions written in vim script.


function!GetMyName()
  echo 'Brij'
endfunction

command! MyName call GetMyName()

nnoremap M :MyName<CR>


Installing a plugin means adding it to Vim's 'runtimepath' (:help 'runtimepath')

:set runtimepath+=/.vim/mypackage/my-plugin

When vim launches, it searches for plugins under .vim/pack/*/start


:helptags ALL
index the documentations

:packadd <plugin-name>
load optional plugin from .vim/pack/bundle/opt/<plugin-name>


:messages
see previous messages


:help channel
info on Vim's job control



fzf
:FZF : open fzf picker interface
<C-c> : exit fzf picker interface
<C-v> : opens file in vertical split
<C-x> : open in horizontal split
<C-t> : open in new tab
<C-k/j> : change selection

== navigating help ==
:help user-manual
<C-]> : visit hyperlink
<C-o> : go back


== Sources ==
https://statico.github.io/vim3.html
http://colorswat.ch/vim
http://vimcasts.org/episodes/packages/
https://vimways.org/2018/the-power-of-diff/
https://benmccormick.org/2014/07/02/learning-vim-in-2014-vim-as-language/
https://www.blaenkdenum.com/posts/a-simpler-vim-statusline/


= pending reads =
https://benmccormick.org/2014/07/02/learning-vim-in-2014-vim-as-language
https://gist.github.com/nifl/1178878
https://stackoverflow.com/questions/1218390/what-is-your-most-productive-shortcut-with-vim/1220118
https://medium.com/usevim/stop-the-vim-configuration-madness-c825578bbf3e
https://medium.com/@mkozlows/why-atom-cant-replace-vim-433852f4b4d1
https://blog.carbonfive.com/2011/10/17/vim-text-objects-the-definitive-guide/
http://docs.emmet.io/customization/snippets/

= pending plugins =
https://github.com/mattn/webapi-vim
