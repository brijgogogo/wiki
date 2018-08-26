= vim-vinegar =

* - : see directory listing of the file, and go up once in
* gh : toggle file hiding
* ~ : go to home
* y : copy absolute path of file under cursor
* . : put file at : command line
* ! : puts fle at command line with ! (eg. :!chmod +x path/to/file)

To hide dot files by default:
let g:netrw_list_hide = '\(^\|\s\s\)\zs\.\S\+'
