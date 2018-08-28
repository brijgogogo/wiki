== batch scripting basics ==
:: use .cmd extensions for batch files (.bat is outdated)

== comments and echo ==
:: use REM (remark) for comments, but they are printed if echo is on
:: use :: to add remarks in batch file. Unlike REM, it is not printed whether ECHO is off or on
:: :: is a hack, uses the label operator : twice, which is almost always ignored (FOR loop will error out with :: style comments)
rem batch script
@echo off
:: by default the batch interpreter will print out each command before it's processed
:: to avoid printing a command, prefix it with @. @ is a special operator to suppress printing of the command line.
:: to avoid printing throughout the program, run @echo off
:: You restore printing with: ECHO ON

== arguments ==
:: %0 is the invoked file name
:: %n is the argument. %1 is first argument, %2 is second argument, so on

== exapnding ==
:: ~ expands the given variable
echo %~0

:: run script with argument "hello"
:: below will print it by removing surrounding quotes ("")
echo %~1

:: expands %0 to a fully qualified path name
echo %~f0
:: drive letter
echo %~d0

:: path only (without drive)
echo %~p0

:: combine ~d, ~p
echo %~dp0

:: only extension
echo %~x0

:: ~n is the file name (without extension)
echo %~n0

:: short name
echo %~s0

:: ~t is the timestamp of file
echo %~t0

:: ~z is the size of file
echo %~z0

:: file attributes
echo %~a0

:: %cd% is also available in command prompt
echo %CD%

:: %!dp0 is available only in batch file
echo %~dp0



* [[variables]]
