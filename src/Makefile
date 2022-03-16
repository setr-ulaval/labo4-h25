export ARCH:=arm
export CROSS_COMPILE:=$(HOME)/arm-cross-comp-env/arm-raspbian-linux-gnueabihf/bin/arm-linux-gnueabihf-
# path du kernel utilisé au lab1 (possiblement différent pour installation custom)
# http://vision.gel.ulaval.ca/~cgagne/enseignement/SETR/H2019/labo1.html#compilation-et-installation-de-la-cha%C3%AEne-de-compilation
export KERNEL_SRC:=$(HOME)/rPi/linux-rpi-4.19.y-rt

obj-m += setr_driver_polling.o setr_driver_irq.o

all:
	printenv
	make -C $(KERNEL_SRC) M=$(PWD) modules

clean:
	make -C $(KERNEL_SRC) M=$(PWD) clean
