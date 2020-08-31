# Dockerfile for Pulseaudio

FROM alpine:3.12
RUN apk add --no-cache dbus-x11
RUN apk add --no-cache libdaemon popt soxr libconfig avahi mpg123 expect
RUN apk add --no-cache alsa-lib alsa-utils
RUN apk add --no-cache pulseaudio pulseaudio-dev pulseaudio-zeroconf
RUN apk add --no-cache pulseaudio-alsa pulseaudio-utils
RUN apk add --no-cache alsa-plugins-pulse

RUN rm -f /etc/pulse/*

ADD paconfig /paconfig
ADD init /init

CMD ["/init"]
