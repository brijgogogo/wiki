= NETRW =

* Invoking netrw
:e . (to open explorer)
:Explore - opens netrw in the current window
:Sexplore (:sex) - opens netrw in a horizontal split
:Vexplore - opens netrw in a vertical split

* views
i : to switch views
`let g:netrw_liststyle = 3`
Press I to show banner at top
`let g:netrw_banner = 0` : to permently remove banner

* :bd to close

* How to open files
`let g:netrw_browse_split = 3`
1 - horizontal split
2 - vertical split
3 - new tab
4 - in previous window

The width of the directory explorer can be fixed with the netrw_browse_split option. The following sets the width to 25% of the page.
let g:netrw_winsize = 25

If NERDtree is your thing netrw can give you a similar experience with the following settings
let g:netrw_banner = 0
let g:netrw_liststyle = 3
let g:netrw_browse_split = 4
let g:netrw_altv = 1
let g:netrw_winsize = 25
augroup ProjectDrawer
  autocmd!
  autocmd VimEnter * :Vexplore
augroup END

https://shapeshed.com/vim-netrw/
https://andrew.stwrt.ca/posts/vim-ctags/


D (delete file/directory)
d (create directory)
% (create file)
R (rename file/directory)


use tpope/vim-vinegar to enhance netrw

