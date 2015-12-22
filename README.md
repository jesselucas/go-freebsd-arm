# Installing Go on FreeBSD arm

Note: This guide assumes you have `wget` installed if you don't `pkg install wget`.

* `cd $HOME`
* `git clone https://go.googlesource.com/go`
* `wget https://dl.dropboxusercontent.com/s/z96jcop37238cil/go-freebsd-arm-bootstrap.tbz`
* `tar -xjf go-freebsd-arm-bootstrap.tbz`
* `cd go/src`
* `env GOROOT_BOOTSTRAP=$HOME/go-freebsd-arm-bootstrap GOARM=7 ./all.bash`
