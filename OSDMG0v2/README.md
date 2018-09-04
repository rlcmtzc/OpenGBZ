# First Version of my opensource DMG Board

**Author:** rlcmtzc12 *(Based on rlcmtzc12 design)*  
**Tested:** Not yet  
**BOM-file:** Not yet   
**Build:** /  

## Description:

This board has an integrated charging and Boost circuit. The Boost circuit is based on the TPS61236P Boost IC. (Datasheed found [here](http://www.ti.com/lit/ds/symlink/tps61236p.pdf)) The outputvoltage is set to around 5 Volt. The Boost circuit can be switched on with a powerswitch. The charging circuit of the Battery is based on TP4056 IC which can charge a single lithium-ion battery with up to 1A (Datasheed found [here](https://www.e-gizmo.net/oc/kits%20documents/TP4056-1A%20Li-ion%20Battery%20Charger/TP4056-1A%20Li-ion%20battery%20charger%20Manual.pdf)). Also I integrated the FS312G-F IC which protect the Battery from overcharge, overdischarge and overcurrent (Datasheed found [here](https://www.ic-fortune.com/upload/Download/FS312F-G-DS-12_EN.pdf)). The board will be charged with an usb type c connector. On the board is place for an standard PAM module which then connect to place for a volumewheel and the aux-port. On the front there are the standard buttons (Up, Down, Left, Right, Start, Select, A, B, X, Y) All the Buttons are connected with an ATmega32u4. The Atmega32u4 can be programmed over the USB-C Port by switching a Button. The Code for the Arduino can be used from the [sudomod wiki](https://www.sudomod.com/wiki/index.php/Leonardo_/_Pro_Micro).
The difference to the first version is that this one has an integrated safe shutdown which is completely done on the hardwareside so you don´t need any script.
It works like following:  
First when you switch on the power a capacitor gets charged. When the capacitor is charged over a given treshold voltage a Mosfet switches on and allow voltage to the pi the capacitor charges on to 5V.
The capacitor is charged in a few miliseconds so there is no delay to turn the raspberry pi on. Next when you turn the switch off a transistor turns an pin to ground this pin is connected to the reset pin of
the pi so when this pin is set to ground the pi turns off. At the same time the capasitor slowly discharges over an resistor when the capacitor is under the thresholdvoltage the Mosfet turns off and so cut the power to the pi.
From turn off until the Mosfet cuts the power pass 15s with this resistor, this is enough time that the pi can shutdown. You also can change the Time by increasing/decreasing the resistor size/ capacitor size. So you only have to
connect a wire to the reset pin off the pi for this safeshutdown to work.

Some Simulationdata of the Boost IC:  
![](https://github.com/rlcmtzc/OpenGBZ/blob/master/OSDMG0v2/Images/efficency.PNG)  
(Keep in mind there is also heat, a lot of heat at 4A so you probably should not use it over 3A. I try to make the copperareas on the PCB quit big so they can work as heat sinks but of course they will not dissipate 5V@4A --> 20W)

Here are the Schematics. I splitted them in Eagle up for better overview:
![](https://github.com/rlcmtzc/OpenGBZ/blob/master/OSDMG0v2/Images/power-circuit.PNG)  
![](https://github.com/rlcmtzc/OpenGBZ/blob/master/OSDMG0v2/Images/Button-Audio.PNG)  

The finished PCB (The nameplacement could be done better):
![](https://github.com/rlcmtzc/OpenGBZ/blob/master/OSDMG0v2/Images/openGBZv2_top.png)  
![](https://github.com/rlcmtzc/OpenGBZ/blob/master/OSDMG0v2/Images/openGBZv2_bottom.png)  

## Get Project:
Just download the Eagle files.
