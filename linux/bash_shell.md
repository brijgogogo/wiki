= bash =

* [[bashrc_vs_bash_profile]]

* /usr/bin/bash
* chsh -s /bin/bash.
* ~/.bashrc : configuration settings

== history ==
* ~/.bash_history:  contains commands you typed
* !# : replace # with number of command you want to run
* history -r : clear current session history
* !! : re-execute last command
* !!:p : echo last command
* !?<search_string> : execution last command matching search string, like !?echo
* !$ : reuse options from the last command, like ls /bin, then cd !$
* !:- : last command without the last argument
* C-R : reverse search history, C-C to cancel
* echo "!!" > script_file.sh : save last long command that wan run into a script
* Esc + . : inserts last argument of last command
* Esc + * : inserts the auto-completion command line results

