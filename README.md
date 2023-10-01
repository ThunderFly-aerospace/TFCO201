# TFCO201 - ThunderFly airborne CO2 concentration sensor

[![Kicad](https://github.com/ThunderFly-aerospace/TFCO201/actions/workflows/kicad_outputs.yml/badge.svg?branch=TFCO201A)](https://github.com/ThunderFly-aerospace/TFCO201/actions/workflows/kicad_outputs.yml)

The TFCO201 CO2 gas sensor offers flexible integration options. It can be directly connected to a Pixhawk autopilot with PX4 firmware or used as a sensor for the [TF-ATMON monitoring system](https://www.thunderfly.cz/tf-atmon.html).

Sensors mounted on UAVs can be used for a variety of purposes. Basically, TFCO201 can measure CO2 concentrations in parallel with air temperature and humidity, which can be used for meteorological purposes. It could also be used to determine the presence of wildfires.

![TFCO201A top view](/doc/gen/img/TFCO201-top.png)

![TFCO201A bottom view](/doc/gen/img/TFCO201-bottom.png)


## Where to get it?

The TFHT01 is commercially available from [ThunderFly s.r.o.](https://www.thunderfly.cz/). For a commercial quotation, contact us by email at info@thunderfly.cz or shop at our [Tindie store](https://www.tindie.com/products/thunderfly/).


## Parameters

| Parameter | Value | Description |
|-----------|-------|-------------|
| Sensing element | [SCD41](https://sensirion.com/media/documents/E0F04247/631EF271/CD_DS_SCD40_SCD41_Datasheet_D1.pdf) | Other possible sensors SCD40, SCD42 |
| Typical accuracy | ± (50 ppm + 5% of reading) | 400 ppm – 2’000 ppm  |
| Humidity measurement accuracy | ± 9 % RH | -10 °C – 60 °C, 0 %RH – 100 %RH  |
| Temperature measurement accuracy | ± 1.5 °C | -10 °C – 60 °C |
| Repeatability | ± 10 ppm |  |
| Operating temperature range| -10 °C – 60 °C |  |
| Operating humidity range| 0 %RH – 100 %RH | |
| I2C connector | 4-pin JST-GH | The second connector could be installed on the opposite side |
| I2C address | 0x62 | can be changed by using the [TFI2CADT01](https://github.com/ThunderFly-aerospace/TFI2CADT01) |
| Storage temperature range| -20 °C - +40 °C |  |
| Operational input voltage | 3.6 - 5.4V | Overvoltage internally protected by zener diode |
| Mass | 3 g | PCB, without cabling |
| Dimensions | 30 x 15 x 6.5 mm |  PCB |
| Weather resistance | IP40 | External connectors fully occupied.  |


## Applications

### Atmospheric sounding

The TFCO201 sensor could be used for [direct atmospheric sounding](https://en.wikipedia.org/wiki/Atmospheric_sounding). Here is an example of measured data taken by [TF-G2 autogyro](https://www.thunderfly.cz/tf-g2.html).

## Schematics

[![Schematics](/doc/gen/TFCO201-schematic.svg)](doc/gen/TFCO201-schematic.pdf)

## Usage in PX4
~~The sensor is currently supported by the PX4 autopilot. Multiple sensors can be connected to one autopilot. The measured data are immediately sent to the ground station and they are also logged in the onboard ulog file.~~
