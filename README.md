# Description

This repository is a fork of minimalistic SSD1306 I2C driver:
`https://github.com/iliapenev/ssd1306_i2c`

Which is based on Adafruit SSD1306 Arduino library.

# This fork

It is intended to provide the same functionality but without
relaying on RaspberryPi device and libraries.

# Dependencies

Insread of WiringPi it uses WiringX library: https://wiringx.org/

- Use `wiringPiI2C.h` instead of `wiringx.h`
- Replace `wiringPiI2CSetup()` with `wiringXI2CSetup()`
- Replace `wiringPiI2CWriteReg8()` with `wiringXI2CWriteReg8()`

Also WiringX needs `I2C_DEV` to be set when working with multiple
I2C interfaces.

Some other functuins are modified to be compatible with GCC build
directly on the device.
