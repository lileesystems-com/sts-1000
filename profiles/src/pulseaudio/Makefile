# Copyright (c) 2020 by Lilee Technology, Ltd.
# All rights reserved.
#
# Makefile for creating LileeOS PulseAudio container service profile

TARGET?=.
SRC=pulseaudio.env pulseaudio.yml
target=$(TARGET)/pulseaudio.zip

all: $(target)

$(target): $(SRC)
	zip $(target) $(SRC)

clean:
	rm -f $(target)
