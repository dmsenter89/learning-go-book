# Learnig Go - Book Examples

This repo houses code associated with me learning through Bodner's book on Go. 

## Go Setup
A binary release of Go for all platforms is available at the [official website](https://go.dev/dl/). 
If you're on Ubuntu, chances are your repo's version of Go is out-of-date, so I used the version from
the website instead. As of this writing, that's version 1.18.1. Direct download for the linux tar is
available [here](https://go.dev/dl/go1.18.1.linux-amd64.tar.gz). Install instructions are available 
[here](https://go.dev/doc/install). A short version:

```sh
# remove old Go, if it exists
sudo rm -rf /usr/local/go 

# download current version of Go
wget https://go.dev/dl/go1.18.1.linux-amd64.tar.gz
# extract new download to /usr/local
sudo tar -C /usr/local -xzf go1.18.1.linux-amd64.tar.gz
rm go1.18.1.linux-amd64.tar.gz # delete the tar file
```

At this point, all that is left is making sure that Go is added to your path, e.g. by adding it
to your `$HOME/.profile` or bashrc. Or run

```sh
export PATH=$PATH:/usr/local/go/bin
```

directly. Bodner also recommends setting the Go Path by adding the following to `$HOME/.profile`:

```sh
export GOPATH=$HOME/go
export PATH=$PATH:$GOPATH/bin
```

A few additional go tools that he recommends adding:

```sh
# goimports: improves your import statements
go install golang.org/x/tools/cmd/goimports@latest 

# golint: a linter
go install golang.org/x/lint/golint@latest

# delve: a debugger
go install github.com/go-delve/delve/cmd/dlv@latest
```

## The Book
Bodner, Jon. _Learning Go: An Idiomatic Approach to Real-World Go Programming._ First edition, O’Reilly, 2021.

This book is available for reading at O'Reilly Online. Check your university library for digital access.
