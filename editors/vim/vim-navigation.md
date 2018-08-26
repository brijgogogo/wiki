= Vim Navigation =
* I : insert at the beginning of line
* a / A append to next / append to end
* W : to the next space-separated word
* b, e : to the begin/end of the current word. (B / E for space separated only)
* nG : jump to line n * <c-o> : jump back
* <c-i> : jump forward
* <c-u> : go half screen up
* <c-d> : go half screen down
* <c-f> : go one entire screen forward
* <c-b> : go one entire screen backward
* gj or gk, g$, g0 : to move down/up/end/start on wrapped lines
* gf : opens the file with name under cursor
* fs : to go to first character s in line,
use ; to jump to nex match and , to jump back
* F : find backward in line
* t/T : works like f/F but puts cursot one char back
* vfs : to select till first character s in line
* * : search the word under cursor and jump to next match
* # : same as *, but searches backwards
* K : opens man page for the word under cursor
* J : joins two lines
* H : jump to the first line of the screen (home)
3H puts cursor 3 lines below the top of the window (affected by scroll off)
* M : jump to the middle line of the screen ("middle")
* L : jump to the last line of the screen ("low")
3L puts cursor 3 lines above the bottom of the window (affected by scoll off)
* zz : to instantly center the line where the cursor is located.
* zt : puts current line at top of screen (affected by scroll off)
* zb : puts current line at bottom of screen (affected by scoll off)
* gx : opens url in browser
* g; : go back to last change
* g, : go forward to last change
* { or }: move to previous/next blank line (or paragraph)
* . : repeat last command (text operation)
* [ or ]: in vimrc moves batween functions
* <C-I> or <C-O> : got to last and previous locations
