= bash =
Bash (which stands for Bourne again Shell) is the name of the shell program that interprets our text input and converts it into commands for the computer to run.

* The prompt is what Bash uses to signal that it is waiting for your next command.


* Multi-line execution
For readability sake, users can separate a length command into multiple lines by appending a backslash after each line
user@host:~$ mkdir -p January February March April \
May June July August September October November \
December

* Multiple commands per line
For readability sake, users can use semicolons to indicate the end of a command within a single line. This allows the user to list and execute multiple commands upon hitting Enter:
user@host:~$ mkdir -p January; mkdir -p December

* Multiple conditional commands per line
The use of double-ampersands between commands will also allow the execution of multiple commands in a single line. However, unlike semicolons, if the first command fails, the second command will not run:
user@host:~$ cd some_directory_that_may_exist && rm -f *

* Literal text strings with quotes
The use of quotes (single or double) allows the user to enclose a text string as a literal value. For example, the following will create a single directory named 'Documents and Settings'
user@host:~$ mkdir 'Documents and Settings'
Without quotes, the same command would create three directories: Documents, and, and Settings
user@host:~$ mkdir Documents and Settings

However, if a double-quoted string encloses a special character, such as the dollar-sign that denotes a variable, the shell will expand the variable to its value:

user@host:~$ some_number=42
user@host:~$ echo 'There are $s bottles of beer'
There are $some_number bottles of beer
user@host:~$ echo "There are $some_number bottles of beer"
There are 42 bottles of beer




= sources =
http://www.compciv.org/bash-guide/
