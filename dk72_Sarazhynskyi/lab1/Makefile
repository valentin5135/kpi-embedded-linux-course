# (!) using paths with spaces may not work with Kbuild

 # this is what is used by Kbuild
 obj-m += mod1.o

 # directory containing Makefile for kernel build
 KBUILDDIR ?= ../linux-5.10.17

.PHONY: modules tidy

# recur to the original kernel Makefile with some additions
modules:
	$(MAKE) -C "$(KBUILDDIR)" M="$(PWD)" modules

tidy:
	$(MAKE) -C "$(KBUILDDIR)" M="$(PWD)" clean

