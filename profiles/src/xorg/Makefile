# Copyright (c) 2020 by Lilee Technology, Ltd.
# All rights reserved.
#
# Makefile for creating LileeOS X Server container service profile

TARGET:=.
SRC=xorg.env xorg.yml
target=$(TARGET)/xorg.zip

all: $(target)

$(target): $(SRC)
	zip $(target) $(SRC)

clean:
	rm -f $(target)
