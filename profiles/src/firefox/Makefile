# Copyright (c) 2021 by Lilee Technology, Ltd.
# All rights reserved.
#
# Makefile for creating LileeOS Container diag shell service profile

SRC=firefox.env firefox.yml global.yml
target=$(TARGET)/firefox.zip

all: $(SRC)
	zip $(target) $(SRC)

clean:
	rm -f $(target)
