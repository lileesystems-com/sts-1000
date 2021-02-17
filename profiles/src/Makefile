# Copyright (c) 2020 by Lilee Technology, Ltd.
# All rights reserved.
#
# Makefile for creating LileeOS container profiles.

subdirs=xorg pulseaudio bionic firefox diagshell
export TARGET=$(shell pwd)/..

all:
	for d in $(subdirs); do \
		$(MAKE) -C $$d; \
	done

clean:
	for d in $(subdirs); do \
		$(MAKE) clean -C $$d; \
	done

PHONY = $(strip $(subdirs))
