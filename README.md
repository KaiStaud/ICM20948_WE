# Modifications for STM32
This fork modifies wollewald's library for Invensense's ICM 20948 to be used with STM's STM32 HAL Library.
The modified library is tested with an STM32G474 Nucleo Board, the IMU (mounted on an Adafruit breakoutboard)is connected to I2C1 via its QWIIC Connector.
The project needs to be converted to a "C++ Project" and main.c needs to be converted to main.cpp.

I will expand the library to support Interrupt and DMA functionality in future.

# ICM20948_WE
An Arduino library for the ICM-20948 9-axis accelerometer, gyroscope and magnetometer. It contains many example sketches with lots of comments to make it easy to use.

I have not implemented DMP features and most probably I won't do that in future. That would exceed the time I can invest. 

You can find a documentation in my blog:

https://wolles-elektronikkiste.de/icm-20948-9-achsensensor-teil-i (German)

https://wolles-elektronikkiste.de/en/icm-20948-9-axis-sensor-part-i (English)

If you find bugs please inform me. If you like the library it would be great if you could give it a star.

If you are not familiar with the ICM20948 I recommend to work through the example sketches.

When you wire the ICM-20948 you need to consider that VDD is 3.3 volts, but VDDIO is only 1.71-1.95 volts (see data sheet). For a 5V MCU board, I used a level shifter and addtional resistors to GND.

Known issue:
* If you upload sketches, the magnetometer occasionally does not respond. If you disconnect from power and then reconnect it will work. I experienced the issue only after uploads.
