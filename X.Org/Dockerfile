# Dockerfile for Xorg Server

FROM alpine:3.12
RUN apk add --no-cache xorg-server
RUN apk add --no-cache xf86-input-keyboard xf86-input-mouse
RUN apk add --no-cache xf86-video-vmware xf86-input-vmmouse
RUN apk add --no-cache xterm
RUN apk add --no-cache xset

RUN apk add --no-cache xf86-video-intel

ADD xorg.conf.d /etc/X11/xorg.conf.d

CMD /usr/bin/Xorg -nolisten tcp
