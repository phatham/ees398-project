# Goal

* Make a prototype (complete PCB) of a certain product.

# Possible Topics

- Portable air purifier
- Hot coffee cooler

# Learning methods

- Learners will be divided into groups of 6-7 people
- Individual duties for each learner
  - Sensors (2, Commu. Eng.)
  - Actuators (1, Power Eng.)
  - Voltage Conversion (1, Power Eng.)
  - Programming (1)
  - PCB designs (1)
  - Soldering (0-1)
- Mostly learner-oriented with personalized explanations
- Instructor(s) provide physical/software resources and support, so there is no "proper lecture note"
- We all learn together, so there might be struggles; there is no "step-by-step guide"

# Work Plan

* Week 1: Sensors Communication, Actuator Communication, and PCB Design should be finished
  * Sensors: sensors connection and study their principles
  * Actuators: build an NMOS circuit to control fan
  * Voltage Conversion: build a step-up converter
  * Programming: send command to test screen, buzzer, sensors and actuators (all tested individually)
  * PCB designs: design fan control switch (consult from actuators), voltage conversion (consult from voltage conversion)
  * Soldering: solder the pins of microcontroller and others, work with PCB designs to design where to put which component
* Week 2: Program workflow should be finished
  * Sensors: finish sensors connections
  * Actuators: finish actuator module and try to connect with the microcontroller
  * Voltage Conversion: join actuators
  * Programming: do the workflow of the entire operation
  * PCB designs+Soldering: design the assembly of the air purifier and hot coffee cooler
* Week 3: Assembly
  * Sensors+Actuator: summarize the key ideas of sensors and actuators
  * Programing: debug the board after full assembly
  * PCB designs: do the assembly
  * Soldering: solder the PCB components

# Datasheets & References

## Sensors

* [Sharp GP2Y10 Dust Sensor](https://global.sharp/products/device/lineup/data/pdf/datasheet/gp2y1010au_e.pdf) (for portable air purifier)
* [MLX90614 Infrared Temperature Sensor](https://media.melexis.com/-/media/files/documents/datasheets/mlx90614-datasheet-melexis.pdf) (for hot coffee cooler)

## Voltage Conversion

* [XL6019 Step Up Converter](http://www.xlsemi.com/datasheet/XL6019%20datasheet-English.pdf)
* [Inductor Part](http://www.es.co.th/detail.asp?Prod=128600057)

## Actuators

* [Flyback Diode Discussion #1](https://electronics.stackexchange.com/questions/56322/do-i-need-a-flyback-diode-with-an-automotive-relay)
* [Flyback Diode Discussion #2](https://electronics.stackexchange.com/questions/313045/does-a-fan-need-a-flyback-diode)
* [Flyback Diode Discussion #3](https://electronics.stackexchange.com/questions/93452/correct-use-of-flyback-or-snubber-diode-across-motor-or-transistor)

## Programming

* [Adding Boards to Arduino Program](https://support.arduino.cc/hc/en-us/articles/360016119519-How-to-add-boards-in-the-board-manager)
* [Installing a Library](https://wiki.seeedstudio.com/How_to_install_Arduino_Library/)
* [ESP8266 Board](https://github.com/esp8266/Arduino)
* [OLED Library](https://github.com/adafruit/Adafruit_SSD1306)
* [GFX Library](https://github.com/adafruit/Adafruit-GFX-Library)

## PCB Designs

### PCB Design & Fabrication

* [EasyEDA Team Join Link](https://easyeda.com/join?type=team&key=a8cff0828559b8c0c103ff8028b2fc9b&inviter=f44dc2b5d0fc4c0b95bf8ff13d97caba&team_uuid=40db8f0feac14e18a53d8ee68cab71db)
* [Searching for Parts](https://jlcpcb.com/parts)

### Resistors Model

* `0603WAF6202T5E` is a 62 kOhm resistor.
* `0603WAFxyzwT5E` is a `xyz` times 10^`w` Ohm resistor.
* [Detailed Information](http://www.es.co.th/Schemetic/PDF/THICKFILMCHIP-R.PDF)
