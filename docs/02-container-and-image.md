# Container and Image

## Container
In general, container act like a sandbox for executing the application. It can run on the virtual machine or within the bare metal. Besides, it's more lightweight compared with the virtual machine, which makes it became the standard way for running application.

## Image
Before you can run the container, you need to create or specify the docker image first. You can create an image by specifying `Dockerfile` and determine what package should installed, what environment variables included, or what command needs to run in the container? After the image has been created,  you can share the images to the public image registry like docker hub just like share source code in Github.

Next: [Hello World](03-hello-world.md)