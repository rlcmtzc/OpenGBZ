# First Version of my opensource DMG Board

**Author:** rlcmtzc12 *(Based on rlcmtzc12 designe)*  
**Tested:** Yes and working  
**BOM-file:** Included  
**Build:** [Build](https://www.sudomod.com/forum/viewtopic.php?f=43&t=6388)

## Description:

This board has an integrated charging and Boost circuit. The Boost circuit is based on the MT3608 step up IC. (Datasheed found [here](https://www.olimex.com/Products/Breadboarding/BB-PWR-3608/resources/MT3608.pdf)) The outputvoltage is set to around 5.2 Volt. The Boost circuit can be switched on with a powerswitch. The charging circuit of the Battery is based on TP4056 IC which can charge a single lithium-ion battery with up to 1A (Datasheed found [here](https://www.e-gizmo.net/oc/kits%20documents/TP4056-1A%20Li-ion%20Battery%20Charger/TP4056-1A%20Li-ion%20battery%20charger%20Manual.pdf)). Also I integrated the FS312G-F IC which protect the Battery from overcharge, overdischarge and overcurrent (Datasheed found [here](https://www.ic-fortune.com/upload/Download/FS312F-G-DS-12_EN.pdf)). The board will be charged with an usb type c connector. On the board is place for an standard PAM module which then connect to place for a volumewheel and the aux-port. On the front there are the standard buttons (Up, Down, Left, Right, Start, Select, A, B, X, Y)

## Images:

![](https://github.com/rlcmtzc/OpenGBZ/blob/master/OSDMG0v1/images/bottom_new.PNG)
![](https://github.com/rlcmtzc/OpenGBZ/blob/master/OSDMG0v1/images/top_new.PNG)
![](https://github.com/rlcmtzc/OpenGBZ/blob/master/OSDMG0v1/images/pcb_stack_front.jpg)
![](https://github.com/rlcmtzc/OpenGBZ/blob/master/OSDMG0v1/images/pcb_back.jpg)
![](https://github.com/rlcmtzc/OpenGBZ/blob/master/OSDMG0v1/images/pcb_back_soldered.jpg)

## BOM

In this Directory there is also an BOM-file with all the componends needed for this Board (BOM-file for [LCSC](https://lcsc.com/user/bom))
