
# QO-100 Satellite Communication Projects

This repository presents various configurations for the QO-100 satellite communication systems. These projects are designed to engage and inspire active involvement from the ham radio community, emphasizing ongoing innovation and enhancement. They aim to highlight the shared enthusiasm for creativity and construction in the field of amateur radio.

vy 73 de ADL805 

---

## 1. QO-100 Satellite Communication Setup - Proof-of-concept 1 - IC-9700 at OE8PPLs shack
The concept was crafted by Chris (OE8CKK) and Michi (OE8YML). Initially deployed at OE8PPLs Peter's ham shack, this proof-of-concept demonstrates the practicality of the design

![Concept for IC-9700](/drawings/qo100V1_200124.drawio.png)

## 1.1 Key Points

TRANSMIT
* Transceiver IC-9700 is used as a transmitter
* When the IC-9700 is in Sat-Mode, a microcontroller checks this and controls the coax relay to send the signal to the QO-100 box
* When the IC-9700 is not in Sat-Mode, normal operation continues
* In the QO-100 box, the 70cm signal is converted to a 13cm signal via SG Labs 13cm Transverter
* The output signal of the SG Labs Transverter is attenuated by 6db and sent to the SG Labs 13 cm PA
* The PA then fires about 43 dbm / 20 Watts over a short cable to the DC8PAT helical antenna
* The signal is thus beamed to QO-100

RECEIVE
* The signal is received with a Bullseye LNB
* This is powered via a Bias-T module
* It is then digitized by an RTL stick (cf. WebRX solution - same technology)
* Displayed on a PC with the software SDR Console (other software would also work)

## 1.2 Bill of material

| Part                                  | ~Price           | Comment                                                                                                                                                                                                                             |
|---------------------------------------|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ESP32 Microcontroller                 | 3-5€             | One could also use a different one like an Arduino, etc.                                                                                                                                                                            |
| Coaxial Relay                         | 110€             |                                                                                                                                                                                                                                     |
| SGLabs 13cm Transverter               | 190€             |                                                                                                                                                                                                                                     |
| SGLabs 13cm PA V2                     | 140€             | One could use V3 PA, but then the attenuator MUST BE -15 dbm                                                                                                                                                                        |
| -6dbm Attenuator                      | 6€               | use -15dbm if you use V3 PA                                                                                                                                                                                                         |
| DC Boost Converter                    | 6-10€            | if you buy a bunch of these they will get cheaper; to stabilize the output one can also use a capacitor (35V, 4700mF) parellel to power the PA                                                                                      |
| Bias-T                                | 10-15€           | if you buy a bunch of these they will get cheaper                                                                                                                                                                                   |
| RTL-Stick                             | 40€              | Every RTL Stick will do the trick                                                                                                                                                                                                   |
| Bullseye LNB                          | 40-50€           |                                                                                                                                                                                                                                     |
| DC8PAT Ice Cone                       | 100€             | If you DIY the ice cone you only have the material costs and 3d printer running costs. In addition you need a copper wire for the antenna part and a reflector (aluminium plate, foil, etc.)                                        |
| Wifi Box for QO-100                   | 70€              | You can use a different box. The goal is to position it as close a possible to the Antenna. So keep in mind to run the things under potential rough conditions. Also think about to remove guide the heat away from the components. |
| Material like cables, fuses           | 50€              | Coaxial cable, power cables, fuses etc. It is a rough estimation.                                                                                                                                                                   |
| Power Supply                          | already in shack |                                                                                                                                                                                                                                     |
| IC-9700                               | already in shack |                                                                                                                                                                                                                                     |
| PC                                    | already in shack |                                                                                                                                                                                                                                     |
| **Price (at the point of documentation)** | **~780€**            | **The more you have at home on tinker equipment and the more you DIY they cheaper it gets :D**                                                                                                                                          |

## 1.3 QO-100 Box

![QO100 BOX 1](/pics/qo100_1.jpg)
![QO100 BOX 2](/pics/qo100_2.jpg)
![QO100 BOX 3](/pics/qo100_3.jpg)
![QO100 BOX 4](/pics/qo100_4.jpg)

## 1.4 Microcontroller Code for conrolling the Coaxial Relay

TODO

## 1.5 Pics from the system in real life

TODO

## 2. QO-100 Satellite Communication Setup - Proof-of-concept 2 - Minimal Setup for portable sat

TODO

## 3. QO-100 QO-100 Satellite Communication Setup - Proof-of-concept 3 - Setup using Adalm Pluto

TODO