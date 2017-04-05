KDIR = /usr/src/linux-so2

all: kbuild ram-disk-test

kbuild:
	make -C $(KDIR) M=$(shell pwd)

ram-disk-test: LDFLAGS=-m32 -static
ram-disk-test: ram-disk-test.c

clean:
	make -C $(KDIR) M=$(shell pwd) clean
	-rm -f *~
