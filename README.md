# orangepipc-i2c-dev

Android userspace IIC/I2C Driver for OrangePi PC.

This is to help others in the forum that having trouble to compile `Homlet Linux and Android` by themself.

These modules and utils are compiled using `homlet lichee` kernel source, so make sure your
Android kernel is based on that source.

## How to install:
- Copy whole files to your Android using `adb`

```
    # this will load the `module`
    insmod i2c-dev.ko

    # make sure the module is loaded (it should show `i2c-dev`)
    lsmod

    # Depend on your uboot setting, you should have `/dev/i2c-0` and `/dev/i2c-1` on your `/dev/`

    # plug your i2c device

    # run `i2cdetect` in `tools/` folder

    i2cdetect -y 0

    i2cdetect -y 1
```

## Some Issues That I Found:

When you module loaded properly (no error on `dmesg` or `insmod`) but `i2cdectect` does not show anything,
it probably due to faulty device, wiring or the base board (I have one defect board that cost me hours on troubleshooting)




