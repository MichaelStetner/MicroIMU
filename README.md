# MicroIMU
Gryo, accelerometer, and compass on a very small PCB

This project is inspired by [Pololu's MinIMU](https://www.pololu.com/product/2468/specs). The design was changed for our particular application: simultaneous recording of neural activity and body movements. To record body movements, the MicroIMU is attached to an animal. To minimize the animal's discomfort, the MicroIMU needs to be as small and light as possible. 
Alongside the MicroIMU, neural activity is recorded with sensitive analog electronics (not included in this repository). To protect the analog electronics, they must be shielded from intereference coming from the digital signals on the MicroIMU so the PCB contains power and ground planes.

Compared to MinIMU, MicroIMU has the following improvements:
* Smaller board size
* Reduced weight
* Power and ground planes
* Wider input voltage range: 2.5V-30V, up from 2.5V-5.5V


Here are the ways that this MicroIMU is less desirable than Pololu's MinIMU:
* 4 PCB layers, up from 2 (increases manufacturing cost) 
* 3.3V I2C communication, down from 5V (compatible with Arduino Due, but not Arduino Uno)
* Less stable power supply (fewer bypass capacitors)
* No external connections for VDD (3.3V) or SA0 (least significant bit of I2C address)

### Acknowledgements
* EAGLE libraries from openrobots-dev/Eagle
