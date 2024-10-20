# Warning 
The corresponding Android version has not yet been developed, and the Android version in this repository is the version of the original repository
## Build
go version 1.20 only (support win7)
cd root directory of the socure code and execute
```
make
```

build specified os and arch.  
All GOOS values:
```
"aix", "android", "darwin", "dragonfly", "freebsd", "hurd", "illumos", "ios", "js", "linux", "nacl", "netbsd", "openbsd", "plan9", "solaris", "windows", "zos"
```
All GOARCH values:
```
"386", "amd64", "amd64p32", "arm", "arm64", "arm64be", "armbe", "loong64", "mips", "mips64", "mips64le", "mips64p32", "mips64p32le", "mipsle", "ppc", "ppc64", "ppc64le", "riscv", "riscv64", "s390", "s390x", "sparc", "sparc64", "wasm"
```

For example linux+amd64
```
export GOPROXY=https://goproxy.io,direct
go mod tidy
CGO_ENABLED=0 env GOOS=linux GOARCH=amd64 go build -o openp2p --ldflags '-s -w ' -gcflags '-l' -p 8 -installsuffix cgo ./cmd
```


