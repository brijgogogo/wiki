= VS Code =
Developed on Electron framework, powered by Microsoft's Monaco Editor and gets its intelligence from OmniSharp/Roslyn and TypeScript.
Visual Studio Code (VS Code) is folder-oriented: you open a folder in VS Code and that folder will be treated like the current “project”.

* yaourt visual-studio-code-bin

* Help > Welcome > Interactive Playground

* [[shortcuts]]

* font ligatures
https://github.com/tonsky/FiraCode
pacman -S otf-fira-code
"editor.fontLigatures": true,
"editor.fontFamily": "'Fira Code'"

* auto-save
"files.autoSave": "afterDelay",
"files.autoSaveDelay": 10000

== sections ==
1. activity bar:(on left) has 5 views:
Explorer:manage files
Searh/Find/Replace
Source Control
Debug: see breakpoints, varibles, call stack
Extensions
2. Site bar: contains view selected from the activity bar
3. Command Palette: Ctrl + Shift + P
4. Editor
5.

== Commands ==
* ext install

== extensions ==
* c# (Microsoft)
* vim (vscodevim)
* Ionide-fsharp
* prettier (Esben Petersen)
* settings sync
* eslint

* move extensions directory
mklink /D C:\Users\bsharma\.vscode\extensions c:\dev\.vscode\extensions

= sources =
vscodecandothat.com
awesome-vscode
Brian Clark : Youtube
