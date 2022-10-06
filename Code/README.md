# OctoBanger_TTL

This is a modified version of the arduino firmware used in the OctoBanger project developed by NorthOSoft (Cant find an actual name)
Original can be downloaded here -> http://buttonbanger.com/?page_id=164

The stock arduino firmware handled by the program uses a different pin assignment than we wanted to use, so we modified the firmware file to use our prefferred pins.

You can load this firmware onto the arduino directly by running the OctoBanger_TTL inside the arduino IDE and uplaoding it to the arduino. This firmware  doesnt effect the arduino bootloader so it can easily be reprogrammed for a future project without any special handling.

To change the firmware that the OctoBanger software loads when you use it, copy the files in the Hex directory and paste them into 
[PathToOctobanger]\Hex\ . This way if you use the octobanger software to upload the firmware it will use our wiring standard.

When going to upload the firmware to the arduino you will have a dropdown menu for which hex file to use youll want to select the ScareBanger.hex file there, and tell it to uplaod as an uno. To help avoid confusion you are able to delete all other files and folders from the [PathToOctobanger]\Hex\ directory without any issues.


The main reason for the differnt PinMap is to keep the I2C and SPI comm channels open so a project that was wired for use with the octobanger could be used for another without needing to undo the wiring.

Our Wiring Standard is as follows  
![image](https://user-images.githubusercontent.com/36548759/182006936-48e2ed6e-e023-42de-b006-9a3e8ec08fb1.png)
