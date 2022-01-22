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

* [EasyEDA Team Join Link](https://easyeda.com/join?type=team&key=a8cff0828559b8c0c103ff8028b2fc9b&inviter=f44dc2b5d0fc4c0b95bf8ff13d97caba&team_uuid=40db8f0feac14e18a53d8ee68cab71db) (Not necessary)
* [Searching for Parts](https://jlcpcb.com/parts) (Not necessary)

### Parts

* [BD9306 Step-up Converter](https://www.es.co.th/Schemetic/PDF/BD9306AFVM.PDF)
* [RQ6E055 NMOS](https://www.es.co.th/Schemetic/PDF/RQ6E055BN.PDF) (Use RQ6E050 footprint, community contributed)
* `UWT1E221MNL1GS` is a Nichicon [![220 uF](https://latex.codecogs.com/svg.image?220%5Cmathrm%7B%5C%20%5Cmu%20F%7D)](#) electrolytic capacitor.
* For ceramic capacitors and SMD resistors, use 0805 or 0603 footprints.
* For Schottky diode, use SMC footprint

### BOM

* BD9306 https://www.es.co.th/detail.asp?Prod=017615577
* RQ6E055 https://www.es.co.th/detail.asp?prod=017609453
* 220uF capacitor https://www.es.co.th/detail.asp?Prod=028901795
* 47uH inductor http://www.es.co.th/detail.asp?Prod=128600057
* Schottky diode https://www.es.co.th/detail.asp?Prod=023503891

### Resistors Model (Not necessary)

* `0603WAF6202T5E` is a [![62 kOhm](https://latex.codecogs.com/svg.image?62%5Cmathrm%7B%5C%20k%5COmega%7D)](#) resistor.
* `0603WAFxyzwT5E` is a [![`xyz` times 10^`w` Ohm](https://latex.codecogs.com/svg.image?xyz%5Ctimes10%5E%7Bw%7D%5Cmathrm%7B%5C%20%5COmega%7D)](#) resistor.
* [Detailed Information](http://www.es.co.th/Schemetic/PDF/THICKFILMCHIP-R.PDF)

### Capacitor Model (Not necessary)

* `CC0603KRX7R9BB104` is a [![100 nF](https://latex.codecogs.com/svg.image?100%5Cmathrm%7B%5C%20nF%7D)](#) capacitor.
* `CL21A226MAQNNNE` is a  [![22 uF](https://latex.codecogs.com/svg.image?22%5Cmathrm%7B%5C%20%5Cmu%20F%7D)](#) capacitor.

# Summary of Week 1

## Initial Plan and Changes

Initially, the instructor planned to use a board (TTGO) with built in LIPO charger, but it seems that the learners are more familiar with an Arduino UNO R3 board. So, we will cut out the battery and use a power-bank instead. For the EasyEDA website, the collaboration doesn't work. The plan will be changed to one learner do the PCB instead.

The manufacturing of PCB in China is paused for every companies due to Spring Festival holidays; there will be no appropriate SMD assembly solution. We have to choose companies in Thailand instead.

The computer classroom is available 30 minutes late (with the same ending time). The room should be changed to other room instead.

## Class Management

For the class management, it seems like separating the functions into six groups can help with the speed. Each learner doesn't have to learn much as expected. The downside of this is too large group (sensors) doesn't have much task to do. To join the knowledge together, we will have a discussion session at the second and third week. 

For speed wise, a single instructor cannot "effectively" handles the whole situation with different duties. Perhaps for next class, we will reduce the number of duties and add some additional works to the "free" learners.

## Learner Challenges

The learners faced with struggles as expected:

* Simple physical NMOS can be a challenge, comparing to "virtual world"
* The "readings" from datasheet is not sufficient to successfully code something
  * One learner asked how much should we read a datasheet, and the answer was "as much as you think it is sufficient." However, after realizing, the answer should be "as much as you can get that thing to work, within their limits."
  * The basic pulsing function of the dust sensor was missed when reading the datasheet.

These problems confirm the instructor's personal thought that this is an effective learning method. If the learners simply copy and paste the codes, or follow the visualized connections, they are not facing with the challenges and will not push them forward (no eager to learn). This is like learning how to swim by watching videos without actually "swimming." The class (aimed as a safe-zone that failures can happen) is like creating a safe "swimming pool" with lifeguards and let them dive in. After a few "drownings," at least some of the learners should get the "eager to learn." One learner asked if he can take something back to learn, which is a good thing.

## Duties

* Sensors: sensors connection and study their principles
  * Connections are studied, but it is not in a stable state when implemented
  * May have to study the principles more thoroughly
* Actuators: build an NMOS circuit to control fan
  * NMOS circuit built
  * Things to test furthers: pulsing the input pins, NMOS gate current limit
* Voltage Conversion: build a step-up converter
  * Preliminary build done; PCB not done
* Programming: send command to test screen, buzzer, sensors and actuators (all tested individually)
  * Only some modules completed
* PCB designs: design fan control switch (consult from actuators), voltage conversion (consult from voltage conversion)
  * Fan control switch and voltage conversion not done yet
* Soldering: solder the pins of microcontroller and others, work with PCB designs to design where to put which component
  * Practiced soldering; results are as expected (acceptable joints after fixing and guidance, no injury)
  * Seems like one learner that didn't choose to solder know something about soldering and asked for solder flux. Perhaps he can share his techniques with the class.

# Work Plan for Week 2

TODO
