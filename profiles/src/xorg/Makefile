# Copyright (c) 2020 by Lilee Technology, Ltd.
# All rights reserved.
#
# Makefile for creating LileeOS X Server container service profile

SRC=xorg.env xorg.yml
target=$(TARGET)/xorg.zip

all: $(SRC)
	zip $(target) $(SRC)

clean:
	rm -f $(target)
