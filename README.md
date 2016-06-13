# golang
All gocode stuff

- go setup
- go structure
- go packages


DOCUMENTATION
- https://godoc.org/

TUTORIAL / SAMPLES
    - https://github.com/GoesToEleven/GolangTraining
    - https://golang.org/ref/spec#Declarations_and_scope
	- http://www.golang-book.com/books/web/01-02

BLOGS
    - http://dave.cheney.net/
    - https://appliedgo.net/

FORUM
    - https://forum.golangbridge.org/

ORGANISATION
    - https://golang.org/doc/code.html#Organization


WORKSPACE
    development
        goroot                                          # manually created base-structure
            bin/                                        # command executables
            pkg/                                        # packages objects
            src/
                github.com/ApolloTitanGolang/hello      # sources (github) hello - repository
                github.com/ApolloTitanGolang/stringutil # sources (github) stringutil - repository
            doc/                                        # documentation (github) doc - repository
                github.com/ApolloTitanGolang/doc

Environment
    set paths in go libraries in preferences (set goroot and gopath)

OPERATIONS

- make the goroot-folder the golang folder
    mkdir goroot
    export GOPATH=$HOME/Development/goroot
    go env

- add the bin
 	export PATH=$PATH:$GOPATH/bin

- set the import paths (e.g. the github-account)
    mkdir -p $GOPATH/src/github.com/ApolloTitanGolang

- make first program folder
    mkdir $GOPATH/src/github.com/ApolloTitanGolang/hello

- create hello.go file
	vi hello.go
	ESC :wq

- build and install
    go install github.com/ApolloTitanGolang/hello

- run (from anywhere, if bin is in the PATH)
	hello

- package
	mkdir $GOPATH/src/github.com/ApolloTitanGolang/stringutil
	vi reverse.go							                    # create file
	go build github.com/ApolloTitanGolang/stringutil
	or go build 							                    # (if already in the package’s folder)
	go install							                        # place the package in the pkg directory