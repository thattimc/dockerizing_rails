# Docker Run

## Format
The docker run command line using the following format:
```bash
docker run [options] <image> <command>
```

Let say if you want to execute the echo command in busybox container. You can type the following command:
```bash
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