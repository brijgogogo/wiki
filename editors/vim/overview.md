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
* [[vim-auto-completion]]
* [[vim-abbreviations]]
* [[vim_other_tips]]
* [[vimdiff]]
* [[clipboard]]
* [[terminal_mode]]

* set ft=text

== Plugins ==
* [[vim-surround]]
* [[vim-unimpaired]]
* [[Emmet Vim]]
* [[NerdTree]]
* [[Vimwiki]]
* [[fzf]]
* [[calendar.vim]]
* [[projectionist]]
* [[coc_vim]]

== Plugin Managers ==
* [[vim-plug]]
* [[minpac]]

* [[VimPlugins|Vim plugins, script, functions]]
* [[help|help/documentation in vim]]

:py print 2*2


* [[.net_in_vim]]

* review previous messages
:messages
:version
:e
* g + Ctrl + g
see info of file: number of words, line, etc.

bestofvim.com
reddit.com/r/vim
http://learnvimscriptthehardway.stevelosh.com/
vimgolf.com


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

see runtimepath values

* [[quickfix]]


:messages
see previous messages


:help channel
info on Vim's job control

:help cmdline-special

:!patch % break-things.diff
apply a patch on current file



== navigating help ==
:help user-manual
<C-]> : visit hyperlink
<C-o> : go back

== ex command ==
ex, short of EXtended, is a line editor for Unix systems.
Line editor: In computing, a line editor is a text editor in which each editing command applies to one or more lines of text designated by the user.
ex was eventually given a full-screen visual interface (adding to its command line oriented operation), thereby becoming the vi text editor.
"ex mode" is invoked by typing the : (colon).
Core ex commands: search, replace
(source: Wikipedia)


= options =
use :set option? to check the value of an option,
use :verbose set option? to also see where it was last set.

== Sources ==
https://statico.github.io/vim3.html
http://colorswat.ch/vim
http://vimcasts.org/episodes/packages/
https://vimways.org/2018/the-power-of-diff/
https://benmccormick.org/2014/07/02/learning-vim-in-2014-vim-as-language/
https://www.blaenkdenum.com/posts/a-simpler-vim-statusline/
https://github.com/romainl/idiomatic-vimrc

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
