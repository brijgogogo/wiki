= bash =
- case sensitive

- when we execute a script from a bash shell, it runs in a new process

== shebang ==
#!/bin/bash
- first line of the script
#! - shebang
/bin/bash : path to the interpreter (program) that should be used to run (or interpret) the rest of the lines in the file
- There must be no spaces before the # or between ! and path of the interpreter.
- You can ommit shebang line, but it is good to include as the script may be called from elsewhere as well
- bash script.sh : run bash by passing script as arugment

== comments ==
# comments

== calling script ==
./script.sh
When you just type a name of the command, Bash tries to find it in a series of directories stored in a variable called $PATH (separated by : ). It doesn't consider sub directories or your current directory. So you need to put "./" to execute the script in your dir.

- calling other script
./another_script.sh

* [[variables]]
* [[functions]]

== common checks ==
if [ -d "$directory" ]; then
  # if directory exists
fi

if [ ! -d "$directory" ]; then
  # if directory doesn't exists
fi


if [ -L "$link" ]; then
  # if symlink
fi


if [ -z ${var+x} ]; then
  # var is unset
fi


== exiting ==
exit [n]
cause the shell to exit with a status of n
If n is omitted, the exit status is that of the last command executed.




== sources ==
https://ryanstutorials.net/bash-scripting-tutorial/bash-script.php#how



