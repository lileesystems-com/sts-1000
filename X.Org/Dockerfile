# Dockerfile for Xorg Server
FROM alpine:3.12

RUN apk add --no-cache xorg-server \
	xf86-input-keyboard xf86-input-mouse \
	xf86-video-vmware xf86-input-vmmouse \
	xterm \
	xset \
	xf86-video-intel

ADD xorg.conf.d /etc/X11/xorg.conf.d

CMD /usr/bin/Xorg -nolisten tcp
