# Copyright (c) 2021 by Lilee Technology, Ltd.
# All rights reserved.
#
# Makefile for creating LileeOS Container diag shell service profile

TARGET:=.
SRC=diagshell.env diagshell.yml global.yml
target=$(TARGET)/diagshell.zip

all: $(target)

$(target): $(SRC)
	zip $(target) $(SRC)

clean:
	rm -f $(target)
