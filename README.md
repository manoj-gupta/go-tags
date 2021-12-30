-  Go tags usage

-  Overview
In Go, a `build tag` is an identifier added to code that determines when the file should be included in a package during the build process. This allows to build different versions of Go application from the same source code.

In this example, `build tags` are used to generate different executable binaries that offer `free`, `pro`, and `enterprise` feature sets of the same application.

- -  Usage:

```
ubuntu@ubuntu:~/go/src/github.com/gocode75/gotags$ go build
ubuntu@ubuntu:~/go/src/github.com/gocode75/gotags$ ./gotags
> Free Feature - 1
> Free Feature - 2
ubuntu@ubuntu:~/go/src/github.com/gocode75/gotags$ go build -tags pro
ubuntu@ubuntu:~/go/src/github.com/gocode75/gotags$ ./gotags
> Free Feature - 1
> Free Feature - 2
> Pro Feature - 1
> Pro Feature - 2
ubuntu@ubuntu:~/go/src/github.com/gocode75/gotags$ go build -tags "enterprise pro"
ubuntu@ubuntu:~/go/src/github.com/gocode75/gotags$ ./gotags
> Free Feature - 1
> Free Feature - 2
> Enterprise Feature - 1
> Enterprise Feature - 2
> Pro Feature - 1
> Pro Feature - 2
ubuntu@ubuntu:~/go/src/github.com/gocode75/gotags$ 
```


- -  Official documentation

* [Build Constraints](https://pkg.go.dev/go/build- hdr-Build_Constraints)