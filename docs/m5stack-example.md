# Gas Meter example

This page documents a PGE gas meter reader build and includes:
- all parts needed
- a working configuration
- a 3D printed weather resistant case, with ..
- a mounting solution

This is what it looks like:


### Design Notes

I chose to combine the esp32 and sensor into one package and run a USB-C power
cable to the meter rather than a [data cable](https://github.com/tronikos/esphome-magnetometer-water-gas-meter?tab=readme-ov-file#wiring).  This means:

- You need the gas meter in range of wifi.
- You need to run a usb-c cable between the power meter and a USB power source.

The benefits:
- There are no electrical noise issues .. you can run a power cable as long as you like.
- There is only one case required
- No soldering is required.


### Parts

- [M5Stack NanoC6](https://shop.m5stack.com/products/m5stack-nanoc6-dev-kit): a 2 core ESP32 with wifi 6.  It's tiny and fits inside the case.
- [Adafruit MMC5603](https://www.adafruit.com/product/5579).  I saw **many** Amazon comments on magnetometers with incompatibility issues, getting a different part than what was ordered etc.  I believe the MMC5603 is the most sensitive of the options and Adafruit is a trusted supplier.
- [Adafruit Grove to STEMMA QT Cable](https://www.adafruit.com/product/4528).  This makes is solderless.
- USB-C Power cable long enough to reach a power source.
- USB power source
- Wire for mounting (see below)


### Case

I designed a weather resistant case.  It has a number of features:

- A double wall design than directs water out
- You can mount the case permanently and the insert is removable.  Very helpful to service it etc.
- It has space to wrap excess cabe inside.
- It has a mounting solution.


This guide shows you to read a PGE meter and includes:

- hardware list of component

 This is a complete


This is a complete
This [ESPHome](https://esphome.io) package allows reading your water meter or gas meter using the QMC5883L or QMC5883P or HMC5883L or MMC5603, a triple-axis magnetometer.

TLDR; Add this to your ESPHome device configuration:

```yaml
substitutions: