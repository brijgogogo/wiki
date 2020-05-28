= Go Modules =

Module: collection of Go packages stored in a file tree with a "go.mod" file at its root.


- Create go.mod file
$ go mod init example.com/hello
- List current module and all its dependencies
$ go list -m all
- Clean up (removes unused dependencies)
  go mod tidy
- list
  go list -m rsc.io/q...
- read docs
  go doc rsc.io/quote/v3


- go.sum file contains cryptographic hashes of the content of specific module versions.
- go.sum and go.mod should be checked into version control



https://blog.golang.org/using-go-modules



