= Tmux - Terminal multiplexer =

== Session ==
* $ tmux
* $ tmux new -s database (start a named session)
* C-b d/D (tmux detach) (to detatch from current session)
* $ tmux ls (list sessions)
* $ tmux attach -t 0 (attach to a session)
* $ tmux rename-session -t 0 database
* C-b $ (rename current session)
* $ tmux switch -t session_name
* Switch between sessions:
  * C-b (          previous session
  * C-b )          next session
  * C-b L          ‘last’ (previously used) session
  * C-b s          choose a session from a list
* C-b:kill-session (to kill the current session)
* tmux kill-session -t target-session
* tmux kill-session -a (destroys all, except current one)
* tmux kill-session (kills last connected session, when run out of tmux)
* tmux kill-server (kills all sessions)

== Panes ==
* C-b % (split a pane - left-right)
* C-b " (split into top-bottom)
* C-b <arrow key> (move in panes)
* C-b o (go to next pane, cycling through)
* C-b ; (go to previously used page)
* exit (or C-d) (to exit a pane)
* C-b C-o (switch panes) (move up)
* C-b { or  } (switch current pane with previous or next pane)
* C-b q (show numeric values of pane)
* C-b ! (break current pane into a separate window)
* C-b C-<arrow> (resize pane)

== Windows ==
* C-b c (tmux new-window) (create new window)
$ tmux  select-window -t :0-9
* C-b w (list windows)
* C-b & (kill window)
* C-b , (rename current window)
$ tmux rename-window
$ tmux split-window
$ tmux split-window -h
C-b 1 ...      switch to window 1, ..., 9, 0
C-b 9
C-b 0
C-b p          previous window
C-b n          next window
C-b l          ‘last’ (previously used) window
C-b w          choose window from a list

""""""""""""""""""""""
" General
""""""""""""""""""""""
C-b ? (to list available commands)
C-b z/Z (zoom into a pane and back)
$ tmux swap-pane -[UDLR] (prefix + { or })
$ tmux select-pane -[UDLR]
$ tmux select-panle -t :.+
$ tmux source-file ~/.tmux.conf
$ prefix : (brings up command prompt)
  :source-file ~/.tmux.conf
* C-b t (show time)
* Any command can be executed as tmux something or C-a :something (or added to ~/.tmux.conf)



###############
# Tmux Resurrect
##################
prefix + Ctrl-s - save
prefix + Ctrl-r - restore

https://github.com/tmux-plugins/tpm
https://github.com/tmux-plugins/tmux-resurrect
https://github.com/tmux-plugins/tmux-continuum
https://gist.github.com/andreyvit/2921703
* http://www.hamvocke.com/blog/a-quick-and-easy-guide-to-tmux/
