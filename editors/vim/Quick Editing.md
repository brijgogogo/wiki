Quick Editing commands
------------------------------------------------------
https://vimcommands.github.io/

* cs work like ds but replacing the surround instead of deleting them. For instance, ci"' will turn "text" into 'text'
* diw : delete inner word (the entire word under the cursor)
* db : delete until the beginning of the word or a word backward if the cursor is already in the beginning of some word
* ds', ds", ds{, ds[, ds( delete surrounds ('', "", {}, (), [])
* di', di", di{, di[, di( delete content inside the given surround
* da', da", da{, da[, da( delete all content of the given surround, including the surround
* dit delete inner tag content
* y$ : yank rest of the line from cursor
nnoremap Y y$

* C change remaining part of line
* D delete until the end of line
* ggdG [d]elete entire buffer from [gg] beginning to [G] end

* Shift + R replace text
* ~ : toggle case

* C-A / C-X increments/decrements a number
* . repeat last command
* = indent line

* r : replace character under cursor
* R : puts us under repalce mode
* Y : copies line of cursor

= Visual Mode =
* o : after selecting some text, press o to switch cursor to start/end
used to expand selection
* O : toggle betwen start and end of line of selected block
used to expand selection in block visual mode

* <c-v> : block visual mode


= Saving Duplicate File =
* :w fileName : saves the contents to fileName, but keeps the current file in buffer
* saveas fileName : saves the buffer to fileName, and opens it in buffer

= Shortcuts in INSERT mode =
* <c-h> : backspace
* <c-w> : backspace a word
* <c-u> : backspace whole line
* <c-v><special-character> : to write special character
e.g. <c-v><esc> gives: 
e.g. <c-v><cr> gives: 
e.g. <c-v><u1234> gives unicode character: ሴ
* <c-o> : accepts one command in NORMAL mode right after pressing <c-o>, then swites bach to NORMAL mode.
eg. writing text<c-o><j>
continue writing text
* <c-r> : accepts register to put at current location
e.g. Hello <c-r><"> continue writing

* u : undo
* U : undo whole line
* r : redo
* $ : go to end of line
* s/S : substitute char/line
* D : delete line
* x/X : delete char under cursor or before it
