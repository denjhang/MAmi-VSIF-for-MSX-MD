# MAmi-VSIF for MSX+MD
 The open source hardware implementation of the VSIF standard can be completed using the red FT232 module that can be easily purchased on Alex. No complicated welding is required. The current hardware supports both MSX and MD devices.    
 The currently supported software is VGM player and MamidiMEMO. For details, see here:   
 https://github.com/110-kenichi/mame  
## Connect to 1ChipMSX (clone)  
The latest version of the vgmplay program fully supports 1ChipMSX's PSG+OPLL+SCC1, but it needs to be used in a certain order to be used normally. First use mini usb to connect to the FTDI module, then open vgmplay. At this time, first check whether the words "usb serial port (com7)" appear in the device manager. If not, you need to install the driver.  
![image](https://github.com/denjhang/MAmi-VSIF-for-MSX-MD/blob/main/Setting/COM%20Port.png)  
After the computer correctly recognizes FTDI, the next step is to open your 1ChipMSX, and then use sofarun to open VGMPlay_msx.rom and run the rom according to the default settings.  
At this time, msx will have a black screen background with "MAMI VGM Sound Driver", and then you can see that the OPLL and SCC of your 1ChipMSX have been correctly recognized and the device location is displayed. At this time, plug the DB9 female connector of VSIF into the JoyPort2 of 1ChipMSX, and the connection is successful without pressing any buttons.  
![image](https://github.com/denjhang/MAmi-VSIF-for-MSX-MD/blob/main/Setting/OCM%20Screen.png)  
Then set the VSIF Checker according to the picture method. After the setting is completed, you can drag the vgm file into the VSIF Checker playlist. If the playback is very stuck, you need to adjust the FTDI CLK. I recommend adjusting it to 7/5/5. The playback speed is related to the length of the USB cable. It is not recommended to use a USB cable that is too long.    
![image](https://github.com/denjhang/MAmi-VSIF-for-MSX-MD/blob/main/Setting/1ChipMSX%20Setting1.png)    
It is best to use a new mini usb cable and avoid using old or rusty cables. Theoretically, the shorter the length of the USB cable, the faster the VSIF data transfer rate.  
