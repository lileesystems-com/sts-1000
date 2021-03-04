# Copyright (c) 2021 by Lilee Technology, Ltd.
# All rights reserved.
#
# Makefile for creating LileeOS Container diag shell service profile

TARGET:=.
SRC=bionic.env bionic.yml global.yml lilee.env
target=$(TARGET)/bionic.zip

all: $(target)

$(target): $(SRC)
	zip $(target) $(SRC)

clean:
	rm -f $(target)
