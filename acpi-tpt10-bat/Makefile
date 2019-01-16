#KERNEL_BUILD_DIR=/lib/modules/$(shell uname -r)/build
#KERNEL_BUILD_DIR=/sdcard/tpt10/linux-sunxi/
#/sdcard/tpt10/linux-4.10.10/
#KERNEL_BUILD_DIR=/home/chip/Code/Thinkpad10-linux/acpi-tpt10-bat/build

KERNEL_BUILD_DIR=/lib/modules/$(shell uname -r)/build

# acpi-tpt10-battery-m += tpt10-bat.o acpi-tpt10-battery.o

obj-m += acpi-tpt10-battery.o

all:
	make -C $(KERNEL_BUILD_DIR) M=$(PWD) modules

clean:
	make -C $(KERNEL_BUILD_DIR) M=$(PWD) clean