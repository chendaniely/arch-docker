# Arch related docker images

Collection of docker images for me to tinker with without ruining my own system.
It's also useful when putting together setup instructions since it's a pretty minimal set of packages.

# Build images

To build the images you can run `docker build`

```bash
cd base
docker build . -t archaur # the . refers to the folder that will tar-ed and sent to Docker daemon
```

You can also build them from the root repo directory

```bash
docker build -t archaur -f base/Dockerfile base
docker build -t archdevp -f dev-python/Dockerfile dev-python
```

# Run/deploy images

No compose file ... yet

```bash
docker run -t -d --name archaur archaur
docker run -t -d --name archdevp archdevp
```

# Remove images

See your running containers

```bash
docker ps -a
```

you can remove the images based on the Name

```bash
docker rm -f archaur archdevp
```
