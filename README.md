# Python with requests

```
docker run python python3 -V | sed 's/Python //'
```

Dockerfile
```
FROM python:3-alpine

RUN pip3 install --root-user-action ignore requests
```

build multiarch images on Ubuntu with buildx and qemu-user-static

https://github.com/multiarch/qemu-user-static

```
docker run --rm --privileged multiarch/qemu-user-static:register
docker buildx build --platform linux/arm64 -t python .
```

```
docker run --rm python uname -m
aarch64
```

```
docker run --rm python python3 -V
Python 3.13.1
```
