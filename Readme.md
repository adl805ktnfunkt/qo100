
# QO-100 Satellite Communication Project Summary

This document outlines the QO-100 satellite communication setup developed for the ham radio community ADL805. The concept was crafted by Chris (OE8CKK) and Michi (OE8YML), showcasing their expertise in amateur radio technology. The initial proof-of-concept was successfully deployed at the ham shack of Peter (OE8PPL), demonstrating the practical application of their design. The project has garnered considerable interest and support from the community, which actively engages in further development and refinement of the setup. This collaborative effort highlights the community's enthusiasm for tinkering and building innovative solutions in the ham radio domain.

---

# QO-100 Satellite Communication Setup


Key Points:
+) Transceiver IC-9700 is used as a transmitter
+) When the IC-9700 is in Sat-Mode, a microcontroller checks this and controls the coax relay to send the signal to the QO-100 box
+) When the IC-9700 is not in Sat-Mode, normal operation continues
+) In the QO-100 box, the 70cm signal is converted to a 13cm signal via SG Labs 13cm Transverter
+) The output signal of the SG Labs Transverter is attenuated by 6db and sent to the SG Labs 13 cm PA
+) The PA then fires about 43 dbm / 20 Watts over a short cable to the DC8PAT helical antenna
+) The signal is thus beamed to QO-100

+) The signal is received with a Bullseye LNB
+) This is powered via a Bias-T module
+) It is then digitized by an RTL stick (cf. WebRX solution - same technology)
+) Displayed on a PC with the software SDR Console (other software would also work)

![Concept for IC-9700](/drawings/qo100V1_200124.drawio.png)