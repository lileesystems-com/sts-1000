# Dockerfile for container diag shell
FROM ubuntu:bionic-20210118

# refer to https://docs.docker.com/engine/install/ubuntu/#install-from-a-package
# https://download.docker.com/linux/ubuntu/dists/bionic/pool/stable/amd64/docker-ce-cli_18.09.9~3-0~ubuntu-bionic_amd64.deb
COPY docker-ce-cli_18.09.9~3-0~ubuntu-bionic_amd64.deb /tmp/

# install sshd/docker-cli/sudo
RUN set -eux;  \
  apt-get update; \
  apt-get --no-install-recommends install -y \
    openssh-server \
    sudo \
    /tmp/*.deb; \
  mkdir -p /var/run/sshd;

# install additional tools (optional)
RUN set -eux;  \
  apt-get --no-install-recommends install -y \
    vim curl netcat tcpdump \
    net-tools iputils-ping iproute2 traceroute \
    psmisc;

# cleanup
RUN set -eux;  \
  apt autoremove -y; \
  apt-get clean;

# instrument sudoer user docker / pwd ChangePassword!!!
RUN set -eux;  \
  useradd -m -s /bin/bash -p '$6$leT7jWYW$BCTEQxrl1nlIC9/U0zQTbCBa/eRKS5QxdsJmLkrWWPi1ZOKst8jzeomUwxppZpJG8FiPls2DQc1Q8rgVl/7Yn/' docker; \
  usermod -G sudo -a docker;

# ssh service port
EXPOSE 22
# ssh daemon
CMD ["/usr/sbin/sshd", "-D"]

