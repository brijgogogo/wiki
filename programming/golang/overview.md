= go-lang =

Created by Ken Thompson, Rob Pike, Robert Griesemer
https://github.com/golang/go

- Strong, static type system
- C-inspired systax
- Multi-paradigm : Procedural, Object oriented
- Garbage Colleciton
- Fully compiled
- Rapid compilation
- Single binary output*

# Phisophy/Values
- Simplicity
- Network aware
- Concurrent apps
- out-of-the-box experience (Standard Libary provides all core features)
- cross-platform (Linux, OS X, Android, ...)
- Backward compatibility


- variable initialization
i := 1
- only postfix increment operator (no prefix increment operator as it reduces code reeadability)
It is a statement, not expresstion (can't be used like println(i++) - for better readability)
i++
println(i)



- loop with incrementor
  for i := 0; i < 5; i++ ..
- loop till condition
  for i < 5
- infinite loop
  for ...
- loop over collection
  for user := range users


- net and net/http packages
  To create web servers using only standard library
- goroutines
  For creating concurrent tasks
- channels
  To safely communicate between concurrent tasks

* [[go_cli]]
* [[go_packages]]
* [[go_modules]]
* [[pointers]]
* [[struct]]
* [[arrays]] slice
* [[maps]]
* [[functions]]
* [[methods]]
* [[interfaces]]
* [[errors]]
* [[readers]]



* sudo pacman -S go : install extra/go


# Web Frameworks
- https://github.com/julienschmidt/httprouter

# ORMs
- https://gorm.io/docs/connecting_to_the_database.html


%% GO toolset uses an environment variable called GOPATH to find GO source code

== Go Toolset ==
%% export GOPATH='/hom/vik/Docs'
$ go version
$ go help
$ go run main.go
%% The go run command takes the subsequent files (separated by spaces), compiles
%% them into an executable saved in a temporary directory, and then runs the
%% program.
$ godoc fmt Println

== Go Packages ==
Packages: reusable pieces of code (shared libraries).

- package "main" - compiles it as executable program
- func main - function name, when used inside package main, it serves as the application entry point

* fmt
%% format: implements formatting for input and outp


== sources ==
https://wiki.archlinux.org/index.php/Go
https://tour.golang.org/list
