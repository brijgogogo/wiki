= vimwiki =

== Syntax ==
  *bold text*
  _italic text_
  ~~strikeout text~~
  `code (no syntax) text`
  super^script^
  sub,,script,,

== Searching ==
* *:VWS* /pattern/
To display all matches use |:lopen| command.
To display next match use |:lnext| command.
To display previous match use |:lprevious| command.
* :vimwikiSearchTags tag

http://thedarnedestthing.com/vimwiki%20cheatsheet

== Viewing ==
* <leader>hh : Convert current wiki into HTML and open in browser. Use single h to only convert.

= Wiki Management =
* [number]<leader>ww :open wiki index file
* [number]<leader>wt : open wiki index file in tab
* <leader>ws : list and select available wikis
* <leader>wr : rename wiki page you are in
* <leader>wd : delete current wiki page

== Navigation ==
* <CR> : follow/create link
 Press <CR> twice to remove list symbol that comes in insert mode
* <S-CR> : Split and follow
* <C-CR> :  Vertical split and follow
* <C-S-CR> : follow/create wiki link in new tab
* <backspace> : go back to previous wiki page
* <Tab> : go to next link
* <S-Tab> : got to previous link

== List Management ==
* <C-Space>
Toggle checkbox of a item in list
* gl<space>
Remove checkbox (use gL<space> to remove from all siblings)
* gll
Increase the level of list item (use gLl for children)
* glh
Decrease the level of list item
* glr
Renumber numbered list item
* gl*
Make list item out of normal line. (similarly gl#, gl-, gl1, gla, gli)
* gL*
Change list symbol to *


== Editing shortcuts ==
* <C-Space> : toggle list item on/off
* = : add header level
* - : remove header level
* + : create or decorate links
* gl* or gl8 : switch or insert * symbol
 similarly gl# or gl3, gl-, gl1
* gll or glm : increase or declrease indent of list item

== Links ==
* [[Link]]
* [[Link|Description of Link]]
* [[/index|Home]]
* [[dotnet/|Links to subdirectories]]
* [[Link#Anchor]]
* [[file:/home/somebody/a/b/c/music.mp3]]
* :tag-example:
* :tag1:tag2:

== Diary ==
number: default 1
* [number]<leader>wi : open diary index
* [number]<leader>w<leader>w : open today's diary file for wiki
* [number]<leader>w<leader>t : open today's diary file for wiki in new tab
* <leader>w<leader>i : generate index of all your diary pages
* <C-Up/Down> : open previous/next day's diary
* == text == : visiable at diary index
* :VimWikiDiaryGenerateLinks
* <leader>c : calendar
