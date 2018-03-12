docker-wix-stable
===========

This repo provides wine and Wix Installer for Docker containers.


*NOTE* Any wine commands should be routed through xvfb. This will emulate an X
server, so that wine will not complain about not being able to find an X
server.

## How to use

1 - Create wine docker image

``` sh
docker build -t ubuntu14.04-wine:latest -f Dockerfile.wine .
```

2 - Create wix docker image

``` sh
docker build -t wix_msi:latest -f Dockerfile.wix .
```

3 - Test wix docker container

``` sh
docker run wix_msi:latest wine /wix/wix/candle.exe --help
```
