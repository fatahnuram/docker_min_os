# Minimal Running OS, dockerized

**Notes**: This repository is currently under development phase.

## Main purpose

**docker_min_os** exists to provide some **detachable minimal running OS** in a **container** environment (well, of course it's **dockerized**). The main purpose of this repository was to provide _minimal running OS_ that you can create anytime (which you call them _virtual machines_), but in a faster, lighter, smaller version by using _containers_.

## But, why?

Why bother using this images when you can use the official ones found in [DockerHub](https://hub.docker.com/)? For example, you can just create a minimal running OS by just running the official image like [Ubuntu 18.04](https://hub.docker.com/_/ubuntu), but why to choose this image?

_By default_, official OS images like [Ubuntu 18.04](https://hub.docker.com/_/ubuntu) **aren't detachable**. You can just run them in a single terminal session, but not for later. If you leave the terminal session, that container you created is stopped instead of running like any other OS. For that reason, by adding some simple tweaks (adding minimal HTTP server), we hope that we can make a **minimal**, but **detachable** version of OS you prefer.

## How to use

How to use this images is simple as only two steps needed. Just **pull** and **run**. No additional steps needed.

- Pull image you wanted from [DockerHub](https://hub.docker.com/), for example Ubuntu 18.04 image.

```bash
docker pull fatahnuram/ubuntu:18.04
```

- Run the container

```bash
docker run --name my-ubuntu --detach fatahnuram/ubuntu:18.04
```

After that, you can use the minimal OS by running `docker exec` to the container you created before.

```bash
docker exec -it my-ubuntu bash
```

## Support

Currently this repository only planned to support some versions of Ubuntu and CentOS image. You can check yourself to see what kind of images that are supported by navigating this repository.
