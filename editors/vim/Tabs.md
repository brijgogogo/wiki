Tab
------------------------------
:tabedit file (open file in new tab)
:tabn, tabp (move between tabs)
:tabclose (close current tab)
:tabclose i (close i-th tab)
:tabonly (close all other tabs)
:tab split (copy the current window to a new tab of its own)
:tab ball         show each buffer in a tab (up to 'tabpagemax' tabs)
:tab help         open a new help window in its own tab page
:tab drop {file}  open {file} in a new tab, or jump to a window/tab containing the file if there is one
:C-w T (move window to a new tab)
gt            go to next tab
gT            go to previous tab
{i}gt         go to tab in position i
:tabs         list all tabs including their displayed windows
:tabm 0       move current tab to first
:tabm         move current tab to last
:tabm {i}     move current tab to position i+1

:tabn         go to next tab
:tabp         go to previous tab
:tabfirst     go to first tab
:tablast      go to last tab

If the file you are editing contains the name of another file, you can put the cursor on the name and type gf to edit the file (goto file). If you type Ctrl-W gf the file is displayed in a new tab.
