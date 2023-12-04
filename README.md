# TFCO201 - ThunderFly airborne CO2 concentration sensor

[![Kicad](https://github.com/ThunderFly-aerospace/TFCO201/actions/workflows/kicad_outputs.yml/badge.svg?branch=TFCO201A)](https://github.com/ThunderFly-aerospace/TFCO201/actions/workflows/kicad_outputs.yml)

The TFCO201 [carbon dioxide gas](https://en.wikipedia.org/wiki/Carbon_dioxide) sensor offers flexible integration options. It can be directly connected to a Pixhawk autopilot with PX4 firmware or used as a sensor for the [TF-ATMON monitoring system](https://www.thunderfly.cz/tf-atmon.html).

Sensors mounted on UAVs can be used for a variety of purposes. TFCO201 can measure CO2 concentrations in parallel with air temperature and humidity, which can be used for meteorological purposes. It could also be used to determine the presence of wildfires.

![TFCO201A top view](/doc/gen/img/TFCO201-top.png)

![TFCO201A bottom view](/doc/gen/img/TFCO201-bottom.png)

## Applications

In combination with the [TF-ATMON system](https://www.thunderfly.cz/tf-atmon.html), the sensor could be used in various applications. Here are a few examples. 

### Atmospheric sounding

The TFCO201 sensor could be used for [direct atmospheric sounding](https://en.wikipedia.org/wiki/Atmospheric_sounding). Here is an example of measured data taken by [TF-G2 autogyro](https://www.thunderfly.cz/tf-g2.html).

### Locating sources of atmospheric pollution (Urban Air Quality Monitoring)

A drone equipped with a CO2 sensor can primarily serve to monitor carbon dioxide levels in densely populated urban areas. This drone can collect data on CO2 concentrations across different parts of the city, aiding authorities in identifying and addressing areas with high emissions. This data can be utilized for green space planning, improving urban transportation, and informing residents about air quality.

### Ecosystem Change Observation 
A drone with a CO2 sensor can be used to monitor changes in CO2 levels in various ecosystems, such as forests, wetlands, or agricultural lands. This information is crucial for scientists studying the impact of climate change on different types of environments and aids in predicting future ecological changes or impact mitigation methods. 


### Industrial Emission Control 
Industrial areas often contribute significantly to total CO2 emissions. Using a drone equipped with a CO2 sensor can effectively monitor and map emissions from factories, power plants, and other industrial facilities. This data can be used for emission regulation and developing strategies to reduce the carbon footprint of industrial areas.

## Where to get it?

The TFHT01 is commercially available from [ThunderFly s.r.o.](https://www.thunderfly.cz/). For a commercial quotation, contact us by email at info@thunderfly.cz or shop at our [Tindie store](https://www.tindie.com/stores/thunderfly/).


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


## Schematics

[![Schematics](/doc/gen/TFCO201-schematic.svg)](doc/gen/TFCO201-schematic.pdf)

## Usage in PX4
~~The sensor is currently supported by the PX4 autopilot. Multiple sensors can be connected to one autopilot. The measured data are immediately sent to the ground station and they are also logged in the onboard ulog file.~~
