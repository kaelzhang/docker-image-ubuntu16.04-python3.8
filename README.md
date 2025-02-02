# Docker Image: ostai/ubuntu-python

Docker Images for creating Ubuntu based images with specific python versions.

For now, it only supports Ubuntu 16.04 with Python 3.8 (3.8.20)

Since Python 3.8 was deprecated on a lot of platforms, this docker image compiled Python 3.8.20 from source code.

## Pull

```sh
docker pull ostai/ubuntu-python:16.04-3.8
```

## Usage

```Dockerfile
FROM ostai/ubuntu-python:16.04-3.8

RUN ...

CMD ["python3.8", "/usr/src/app/start.py"]
```

## For Developers

```sh
make build
```

### Build with a Certain Version

```sh
UBUNTU_VERSION=20.06
PYTHON_SHORT_VERSION=3.9
PYTHON_VERSION=3.9.10

docker build \
-t ostai/ubuntu-python:$UBUNTU_VERSION-$PYTHON_SHORT_VERSION \
--build-arg UBUNTU_VERSION=$UBUNTU_VERSION \
--build-arg PYTHON_SHORT_VERSION=$PYTHON_SHORT_VERSION \
--build-arg PYTHON_VERSION=$PYTHON_VERSION \
.
```
