

===

https://medium.freecodecamp.org/an-in-depth-introduction-to-docker-on-aws-f373ff97da0e
https://aws.amazon.com/docker/

===


https://tuhrig.de/difference-between-save-and-export-in-docker/

https://tuhrig.de/flatten-a-docker-container-or-image/

https://windsock.io/diminishing-the-powers-of-a-container-workload/

https://tuhrig.de/how-to-know-you-are-inside-a-docker-container/


https://tuhrig.de/layering-of-docker-images/

https://www.voyagersearch.com/using-aws-batch-to-generate-image-thumbnails-for-voyager

https://medium.com/@gotraveltoworld/use-docker-to-develop-the-aws-lambda-python-3-6-525007907369

https://medium.com/@alenkacz/whats-the-difference-between-runc-containerd-docker-3fc8f79d4d6ehttps://medium.com/@alenkacz/whats-the-difference-between-runc-containerd-docker-3fc8f79d4d6e

A container built on one architecture will not run on another.
Way back when with Docker “you could run a container anywhere you want, as long as it is the x86_64 CPU architecture on Linux.” Now Docker runs on other architectures and Operating Systems besides Linux on x86-64: IBM Z (s390x), IBM Power, ARM, ARM64. Also Docker on Windows is supported and Docker for Windows can run Windows containers and Linux Containers (https://docs.microsoft.com/en-us/virtualization/windowscontainers/deploy-containers/linux-containers 2). Linux cannot run Windows containers.

Docker containers built for those architectures can only on the Docker installed on those architectures.
Many of the Docker Official Images have images that run on multiple Architectures.
Nginx is one.

https://hub.docker.com/_/nginx 2

And Docker came out with a new image manifest type V2 called the “Fat Manifest” or manifest list.
An image builder can create a docker image for each platform they support, push the images to a repository and then create a “Fat Manifest” and push that to the repository. The Fat Manifest lists the architectures that the docker image will run on. The Fat Manifest makes it easy for a user to pull the image.
