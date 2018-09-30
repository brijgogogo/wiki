= Linux Processes =

* idea.sh &
to start application in background append ampersand [&] to the command:

If you already started the application, press [Ctrl]+[z] in terminal to suspend the application. To allow it to continue running without displahing standard output, type [bg] and press [Enter]. This is referred to as running the application in background.

* ps aux
%% list running processes

* ps auxf

* ps aux | sort -nk +4 | tail
%% display top 10 running processes sorted by memory usage
%% sorted by 4th field of output returned by ps

* use top/htop to see resource usage

* kill -KILL 12345
%% kill a process by process id
%% (use -KILL if it refuses to die)

* killall python
%% will kill all programs with given name

* kill -HUP
%% reload process
%% can be used with killall as well


* lsof | grep fileName
%% to see which process is using a file

* pgrep nvim
%% Returns list of PID of a process
%% add -a or -f to see more detail

* strace -p PID
%% shows all the system call that the process is making
* lsof -p PID
%% list the open files that the process has
* kill 1234
* killall -v process
= PS =

* ps l
%% see all running processes

* ps aux
* ps aux | grep firefox
%% search processes with firefox text

* pgrep firefox
%% returns PID of firefox process ordered chronologically

* kill -9 1234
%% kills the process by PID

* killall firefox
%% kills all firefox processes

* renice : alter priority of a process
It can assign a priority value between -20 and 19. The lower the number, the higher the priority.
renice 15 8899 : here 8899 is PID


== pstree ==
* pstree
list running processes in a tree (parent-child relationship) to see which process started other processes
* pstre -p
show pids
* pstree -np
sort by pid
* pstree user_name
show processes spawned by a user
* pstree -s 780
see parents of a proess you specify
