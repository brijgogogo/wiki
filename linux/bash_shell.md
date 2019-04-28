= bash =
Bash shell / Bourne-again shell - Brian Fox - 1989
It was initially written as a replacement for the Bourne shell.

* [[bashrc_vs_bash_profile]]

* /usr/bin/bash
* chsh -s /bin/bash.
* ~/.bashrc : configuration settings

* set -o vi
enable vi mode

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

= tips =
* Alt + .
Insert the last parameter(s) of the preceding command in your current command
* When executing a script with bash, use the -x option to output the script contents as it's being executed
