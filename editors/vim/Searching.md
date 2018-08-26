= Searching, Finding and Replacing =

* /search_pattern
* ?search_pattern %:searches backward
* & : repeat last substitution command

* /\t : Show all tabs:

* /\s\+$ : Show trailing whitespace:

* /\S\zs\s\+$ : Show trailing whitespace only after some text (ignores blank lines):

* / \+\ze\t : Show spaces before a tab:

* :%s//WON/g : here we have left the content to replace as empty. Vim uses the last searched content to replace.

Ack
-------------------------------
:Ack [options] {pattern} [{directories}]
:Ack <pattern>
:Ack -i <pattern> (case insensitive search)


* https://jezenthomas.com/how-i-find-and-replace-in-vim/
  :args `ack -l '\bClass\b' --ignore-dir=compiled`
  :argdo %s/\<Class\>/MooTools.Class/gc | update

  The -l flag in ack tells the tool to just return me the file names. I’m using the \b word-boundary to refine my search results so I’m not overwhelmed with noise.
  Vim’s word-boundaries (\< and \>) look different from the ones in ack.
  The substitute command is passed the g and c flags. The c flag is interesting here; it stands for ‘confirmation’, and will ask me to confirm or deny substitutions with the y and n keys.
  The pipe character in the context of an Ex command is not the same as piping data through the shell; it’s more like a semicolon in C-like languages and allows you to perform separate commands in one move.


* [[vim-reg-ex]]
