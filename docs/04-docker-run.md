# Docker Run

## Execute the echo command in busybox container
You can type the following command:
```bash
# Format
# docker run [options] <image> <command>
docker run busybox echo "Hello from busybox"
```

Output response will look like:
```
Unable to find image 'busybox:latest' locally
latest: Pulling from library/busybox
ee153a04d683: Pull complete
Digest: sha256:9f1003c480699be56815db0f8146ad2e22efea85129b5b5983d0e0fb52d9ab70
Status: Downloaded newer image for busybox:latest
Hello from busybox
```

To verify existing images
```bash
docker images
```

Output response will look like:
```
REPOSITORY          TAG                 IMAGE ID            CREATED             SIZE
busybox             latest              db8ee88ad75f        5 weeks ago         1.22MB
hello-world         latest              fce289e99eb9        7 months ago        1.84kB
```

To verify running containers
```bash
docker ps
```

Output response will look like:
```
CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS               NAMES
```

To verify containers including the stopped ones
```bash
docker ps -a
```

Output response will look like:
```
CONTAINER ID        IMAGE               COMMAND                  CREATED             STATUS                      PORTS               NAMES
8363d62f8149        busybox             "echo 'Hello from bu…"   18 minutes ago      Exited (0) 18 minutes ago                       admiring_ramanujan
c6905638d5b3        hello-world         "/hello"                 45 minutes ago      Exited (0) 45 minutes ago                       stupefied_snyder
```

As you can see, we have two stopped containers and we can remove it by using the following command:
```bash
# Format
# docker rm <container_id> <container_id>
docker rm 8363d62f8149 c6905638d5b3
```

Besides leaving the container in the stopped state, we can run a container and throw away when finished by specifying `--rm` option:
```bash
docker run --rm busybox echo "Hello from busybox"
```