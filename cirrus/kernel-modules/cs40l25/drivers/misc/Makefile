cirrus_cs40l2x-objs = cs40l2x.o cs40l2x-tables.o
obj-$(CONFIG_HAPTICS_CS40L2X_INPUT) += cirrus_cs40l2x.o

KERNEL_SRC ?= /lib/modules/$(shell uname -r)/build
M ?= $(shell pwd)
CUSTOM_INCLUDE ?= -I$(shell pwd)/include/

KBUILD_OPTIONS += CONFIG_HAPTICS_CS40L2X_INPUT=m \
		  ccflags-y='$(CUSTOM_INCLUDE)'

modules modules_install clean:
	$(MAKE) -C $(KERNEL_SRC) M=$(M) $(KBUILD_OPTIONS) W=1 $(@)
