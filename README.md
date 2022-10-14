# QLC+ 4.12.6 and MagicQ 3D Visualizer via ArtNet on the same Wi-Fi network

## A guide on how to control your fixtures with QLC+ 4 and use the MagicQ built-in visualizer

### Software used:

• QLC+ 4.12.6

• MagicQ 1.9.2.8

### Situation: 

• MB Pro connected on wifi router, IP address 192.168.xxx.xxx

## STEPS

### STEP 1

Prepare your show on QLC+ with all the fixtures you need. I made a new fixture for this show which is an LED Par which has 7 DMX channels (Dim, RGBW, Special, Strobe). I have 9 fixtures and 1 smoke machine.
I will have 7ch x 9 fixtures, plus 1ch for the smoke machine.


<img width="348" alt="1" src="https://user-images.githubusercontent.com/74735686/195824197-4f2db0bd-923f-43cf-9ab6-ecdc68a770d2.png">


### STEP 2

Prepare the same exact show on MagicQ. 
I made a new fixture with the same channels and channel names on MagicQ and i patched all the fixtures to the same channels.
Put all the "Merge" fields of the fixtures to "In" ( -> IMPORTANT STEP, otherwise the fixtures will respond only the the MagicQ faders)

<img width="904" alt="2" src="https://user-images.githubusercontent.com/74735686/195824314-3826b01b-7fd4-4a92-9d01-b26f540848de.png">


After you've prepared the show, move all your fixtures to your specific needs by going to Patch -> View Vis -> Vis Heads and changing the XYZ (and XYZ rot) parameters.

<img width="896" alt="2bis" src="https://user-images.githubusercontent.com/74735686/195825916-f6ce1128-8583-4df2-a7ff-829b188cd001.png">

### STEP 3

Set QLC+ Art-Net output, go to I/O, select ArtNet on address 192.168.xxx.xxx and check the "Output" box.

<img width="438" alt="3" src="https://user-images.githubusercontent.com/74735686/195824822-7ef78716-445a-4189-8bc5-f46687fbfd12.png">

Open the settings for the ArtNet output and make sure that the universe is set to 0.

<img width="579" alt="4" src="https://user-images.githubusercontent.com/74735686/195824888-78589f20-5fff-4171-9fa9-6e44d01300c1.png">

### STEP 4

Go to MagicQ -> Setup -> View DMX I/O and then check universe 1.
Just to be safe, so you'll not get an "En Cflt" error, put the "Out Type" to "None".
Make sure that "In Type" is set to ArtNet and that the "In Uni" is set to  Art 0.

<img width="719" alt="5" src="https://user-images.githubusercontent.com/74735686/195825142-3e136322-fbc1-42eb-a03d-438c22439936.png">

### STEP 5

Go to MagicQ -> Setup -> View Settings -> Network, click (just once, do not double-click) on IP address, write "192" and press enter, that way the IP will be set to 192.0.0.0 and the subnet mask to 255.255.255.0


![6](https://user-images.githubusercontent.com/74735686/195825241-cef9a702-b5d6-464d-b387-4ab7d31f3e03.gif)


### STEP 6

All is done! Go to "VIS" on MagicQ.
By changing your parameters on QLC+ you should be able to see your light show on the MagicQ built-in visualizer.

![7](https://user-images.githubusercontent.com/74735686/195825267-ecc4be87-7579-48da-8a43-076926e06474.gif)


Unfortunately I was not able to set the standalone MagicVis app with this method as you can only select an address from the given list in the preferences, but well, the MagicQ method works and that's all I need!

## Credits:

### QLC+ -> https://www.qlcplus.org/
### ChamSys MagicQ -> https://chamsyslighting.com/
