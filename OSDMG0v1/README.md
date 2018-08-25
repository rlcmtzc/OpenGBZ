# First Version of my opensource DMG Board

**Author:** rlcmtzc12 *(Based on rlcmtzc12 design)*  
**Tested:** Yes and working  
**BOM-file:** Included  
**Build:** [Build](https://www.sudomod.com/forum/viewtopic.php?f=43&t=6388)

## Description:

This board has an integrated charging and Boost circuit. The Boost circuit is based on the MT3608 step up IC. (Datasheed found [here](https://www.olimex.com/Products/Breadboarding/BB-PWR-3608/resources/MT3608.pdf)) The outputvoltage is set to around 5.2 Volt. The Boost circuit can be switched on with a powerswitch. I have tested the boostcitcuit with 1,4 A which works fine but the IC gets a little bit warm. I also tested it with 2A which is the max outputcurrent from the Datasheed which works but the IC get really warm so I wouldnd suggest that. On 1 - 1,2A the IC isn´t even warm so it works perfectly fine in this range. The charging circuit of the Battery is based on TP4056 IC which can charge a single lithium-ion battery with up to 1A (Datasheed found [here](https://www.e-gizmo.net/oc/kits%20documents/TP4056-1A%20Li-ion%20Battery%20Charger/TP4056-1A%20Li-ion%20battery%20charger%20Manual.pdf)). Also I integrated the FS312G-F IC which protect the Battery from overcharge, overdischarge and overcurrent (Datasheed found [here](https://www.ic-fortune.com/upload/Download/FS312F-G-DS-12_EN.pdf)). The board will be charged with an usb type c connector. On the board is place for an standard PAM module which then connect to place for a volumewheel and the aux-port. On the front there are the standard buttons (Up, Down, Left, Right, Start, Select, A, B, X, Y)  

## Get Project:
[Here](https://easyeda.com/editor#id=|1b6bda1489604f5b8086fe82ce4b43ba|fd54b8f932f541aa9ddfa8aae15e51a3) you can edit and change the Project online. Or the attached Altium-files include everything. (I don´t have the more common Eagle files for this Project maybe someone can adapt them to Eagle)
## Images:

![](https://github.com/rlcmtzc/OpenGBZ/blob/master/OSDMG0v1/images/bottom_new.PNG)
![](https://github.com/rlcmtzc/OpenGBZ/blob/master/OSDMG0v1/images/top_new.PNG)
![](https://github.com/rlcmtzc/OpenGBZ/blob/master/OSDMG0v1/images/pcb_stack_front.jpg)
![](https://github.com/rlcmtzc/OpenGBZ/blob/master/OSDMG0v1/images/pcb_back.jpg)
![](https://github.com/rlcmtzc/OpenGBZ/blob/master/OSDMG0v1/images/pcb_back_soldered.jpg)

## BOM

In this Directory there is also an BOM-file with all the componends needed for this Board (BOM-file for [LCSC](https://lcsc.com/user/bom))
