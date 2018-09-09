= powershell =

Powershell is a command line interface (or shell).
It isn't a scripting language.
Posershell gives access to .NET Framework

File extension: .PS1

$ pwsh-preview
To launch in arch-linux
> $PSVersionTable
To check version

== terms ==
A `cmdlet` is a native PowerShell command-line utility. These are written in .NET Framework language like C#.
A `function` can be similar to a cmdlet, but are written in Powershell's own scripting language.
A `workflow` is a special kind of function, that ties into Powershell's workflow execution system.
An `application` is any king of external executable, including command line utilities like  ping and ipconfig.
`Command` is a generic term that we use to refer to any or all of the preceding terms.


== help ==
> update-help
to download help files form internet
> help Get-Service
> HELP **log**
search help using wildcards
> HELP Get-EventLog -full

== parameters ==
Parameters are passed by name using `-ParamName value` or by position
> Get-EventLog Security -computer server-R2,DC4,Files02
Powershell treats comma separated values as array
If values contain space, then it must be enclosed in quotations (single or double)
> Get-EventLog Security -computer (Get-Content names.txt)
get parameter values from a file containing a value per line
> HELP Get-EventLog
> HELP **log**
in help, optional parameters are in square brackets []
If only parameter name (and not type) is enclosed in square brackets, it is positional parameter (meaning you need not name it while calling command)
> Get-EventLog -comp abc
No need to type full parameter name, type enough to distinguish
Parameters can also have aliases for example -ComputerName has aslias -Cn

== cmdlets ==
cmdlets follow verb-nound pattern in their names. Run `Get-Verb` to see allowed verbs.
* Get-Content
reads the contents of a file
* Get-ChildItem /home
get child folders
* Show-Command Get-EventLog
run command using gui
* Test-Connection google.com
works like ping

== support for external commands ==
You can add cmdlets of SQL Server, Exchange Server etc to powershell.
You can use native commands like ping, grep, etc.

== alias ==
an alias is a nickname for a command
> get-alias -Definition "Get-Service"
> gsv
> help gsv
> New-Alias
> Export-Alias
> Import-Alias

== sources ==
https://github.com/PowerShell/PowerShell
