# Dockerfile for Pulseaudio
FROM alpine:3.12

RUN apk add --no-cache \
	dbus-x11 \
	libdaemon popt soxr libconfig avahi mpg123 expect; \
    apk add --no-cache alsa-lib alsa-utils \
	pulseaudio pulseaudio-dev pulseaudio-zeroconf \
	pulseaudio-alsa pulseaudio-utils \
	alsa-plugins-pulse; \
    rm -f /etc/pulse/*

ADD paconfig /paconfig
ADD init /init

CMD ["/init"]
