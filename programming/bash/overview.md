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
 
== test command ==
test EXPRESSION
[ EXPRESSION ]
[[ EXPRESSION ]]

FILE operators:
- -e : checks whether file exists regardless of the type
- -f : returns true only if the file ia a regular file (not a directory or a device)
- -d : checks whether a file is a directory or not
- -x: file exists and is executable
- -w: file exists and is writable
 
e.g:
FILE=/etc/resolv.conf
if [ -f "$FILE" ]; then
	echo "$FILE exist"
fi

# file does not exists
if [ ! -f "$FILE" ]; then
   ....
fi

- -a : check multiple conditions
if [ -f /file1 -a -f /file2 ]; then
fi

if [ -f /file1 && -f /file2 ]; then
fi

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



