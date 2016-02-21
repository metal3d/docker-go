# docker-go

[![](https://badge.imagelayers.io/metal3d/go:latest.svg)](https://imagelayers.io/?images=metal3d/go:latest 'Get your own badge on imagelayers.io')

Alpine based docker image for golang version > 1.5.

Each version can be taken from my docker hub, eg. `docker pull metal3d/go:1.6`

As soon as I can, the "latest" version will be mapped to the latest go version. 

So, `docker pull metal3d/go` will pull "latest" version of go (1.6 at this time).

Images provides build-base (gcc, g++, libs...) and tools to "get" packages (git, bzr, mercurial, curl...)

# Instructions

The image uses that directories:

- `/go` is the GOPATH
- `/usr/lib/go` is GOROOT
- `$PATH` provides `GOPATH/bin` and `$GOROOT/bin`

ENTRYPOINT is "go", so you can call go commands directly:

```bash
$ docker run --rm metal3d/go version
go version go1.6 linux/amd64
```


# Why that image ?

Because I wanted a smaller image, at first. And because there were no docker 1.6 image when I did my build.


