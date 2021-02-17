# Dockerfile for Firefox browser reference design
FROM multiarch/ubuntu-core:x86_64-focal

# install pulseaudio, firefox, and misc tools
RUN set -eux; \
  apt-get update; \
  apt-get --no-install-recommends install -y \
    pulseaudio pulseaudio-utils \
    firefox \
    x11-xserver-utils \
    net-tools isc-dhcp-client iputils-ping;

# cleanup
RUN set -eux;  \
  apt autoremove -y; \
  apt-get clean;

# launch firefox
CMD ["/usr/bin/firefox"]

