export ARCH:=arm
export CROSS_COMPILE:=$(HOME)/arm-cross-comp-env/arm-raspbian-linux-gnueabi/bin/arm-linux-gnueabihf-
# path du kernel utilisé au lab1 (possiblement différent pour installation custom)
export KERNEL_SRC:=$(HOME)/rPi/linux-rpi-4.19.y-rt

obj-m += setr_driver_polling.o setr_driver_irq.o

all:
	printenv
	make -C $(KERNEL_SRC) M=$(PWD) modules

clean:
	make -C $(KERNEL_SRC) M=$(PWD) clean
