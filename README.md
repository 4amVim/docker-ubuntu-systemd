# Ubuntu 22.04 LTS Docker Image with systemd

[![Build](https://github.com/eniocarboni/docker-ubuntu-systemd/actions/workflows/build.yml/badge.svg?branch=main)](https://github.com/eniocarboni/docker-ubuntu-systemd/actions/workflows/build.yml) [![GPL License](https://img.shields.io/badge/license-GPL-blue.svg)](https://www.gnu.org/licenses/) [![Donate](https://img.shields.io/badge/Donate-PayPal-green.svg)](https://www.paypal.me/EnioCarboni)

Ubuntu 22.04 LTS Docker container with systemd, useful for tests with `ansible` especially with `molecule`

## Tags

  - `22.04`, `jammy`, `latest` on main branch
  - `20.04`, `focal`  on main branch
  - `18.04`, `bionic` on 18.04 branch
  - `16.04`, `xenial` on 16.04 branch


## How to Build

  * Verify if [Docker is installed](https://docs.docker.com/install/).
  * Run on main branch: `docker build -t docker-ubuntu-systemd:22.04 -t docker-ubuntu-systemd:latest .`
  * Run on 20.04 branch: `docker build -t docker-ubuntu-systemd:20.04 -t docker-ubuntu-systemd:focal .`
  * Run on 18.04 branch: `docker build -t docker-ubuntu-systemd:18.04 -t docker-ubuntu-systemd:bionic .`
  * Run on 16.04 branch: `docker build -t docker-ubuntu-systemd:16.04 -t docker-ubuntu-systemd:xenial .`
  * Verify image: `docker images`

## How to Use

  * `docker pull eniocarboni/docker-ubuntu-systemd:latest` (or use the image you built earlier).
  * `docker run --detach --privileged --volume=/sys/fs/cgroup:/sys/fs/cgroup:ro --name jammy-systemd eniocarboni/docker-ubuntu-systemd:22.04`
  * `docker run --detach --privileged --volume=/sys/fs/cgroup:/sys/fs/cgroup:ro --name focal-systemd eniocarboni/docker-ubuntu-systemd:20.04`
  * `docker run --detach --privileged --volume=/sys/fs/cgroup:/sys/fs/cgroup:ro --name bionic-systemd eniocarboni/docker-ubuntu-systemd:18.04`
  * `docker run --detach --privileged --volume=/sys/fs/cgroup:/sys/fs/cgroup:ro --name xenial-systemd eniocarboni/docker-ubuntu-systemd:16.04`


View the run container with

  * `docker ps`

Enter in the container with:

  * `docker exec -it <container_id> bash`

Kill container with:

  * `docker kill <container_id>`

Remove container with:

  * `docker image rm -f <container_id>` 

## Author

Created in 2022 by Enio Carboni

## License

GNU GENERAL PUBLIC LICENSE (see [LICENSE](LICENSE) file)
