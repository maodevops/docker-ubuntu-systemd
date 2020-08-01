# Docker Ubuntu Systemd

[![build status](https://img.shields.io/docker/cloud/build/maodevops/ubuntu-systemd)](https://hub.docker.com/repository/docker/maodevops/ubuntu-systemd)

Ubuntu image that has systemd enabled.

## Branches

Each branch in the repository is used for building a specific version.

| Branch | Ubuntu Version | FROM Docker image tag |
| ------ | -------------- | --------------------- |
| master | latest         | latest                |
| 20.10  | 20.10          | 20.10                 |
| 20.04  | 20.04          | 20.04                 |
| 18.04  | 18.04          | 18.04                 |

## Usage

### Run it

```bash
docker run -d \
  --tty \
  --privileged \
  --volume /sys/fs/cgroup:/sys/fs/cgroup:ro \
  --name maodevops-ubuntu20.04-systemd \
  maodevops/ubuntu-systemd:20.04
```

### Enter it

```bash
docker exec -it maodevops-ubuntu20.04-systemd /bin/bash
```

### Remove it

```bash
docker rm -f maodevops-ubuntu20.04-systemd
```
