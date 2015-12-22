# Installing Go on FreeBSD arm

Note: This guide assumes you have `wget` installed if you don't `pkg install wget`.

* `cd $HOME`
* `git clone https://go.googlesource.com/go`
* `wget https://dl.dropboxusercontent.com/s/z96jcop37238cil/go-freebsd-arm-bootstrap.tbz`
* `tar -xjf go-freebsd-arm-bootstrap.tbz`
* `cd go/src`
* `env GOROOT_BOOTSTRAP=$HOME/go-freebsd-arm-bootstrap GOARM=7 ./all.bash`


## Optional: Generate Bootstrap From Source
On a computer that already has Go 1.5 installed.

* `git clone https://go.googlesource.com/go $HOME/go`
* `cd $HOME/go/src`
* `env GOOS=freebsd GOARCH=arm GOARM=7 ./bootstrap.bash`
* `cd $HOME/go-freebsd-arm-bootstrap.tbz`
* `scp $HOME/go-freebsd-arm-bootstrap.tbz your_username@remotehost.edu:go-freebsd-arm-bootstrap.tbz`
