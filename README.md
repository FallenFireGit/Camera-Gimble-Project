# Camera-Gimble-Project

## General Info

The original intent of this project was to make an actual camera gimbal for my phone; however, halfway through, I realized this isn't like other Hack Club events, where they give you a grant to buy the parts (unless I am mistaken). Therefore, I think this doesn't qualify as a hardware project because I don't have the MCU I designed this with (which is the one that must be used to support battery charging), nor do I have the actual battery or step-up converter to turn the 3.3V of the battery to 5V for the servos (unless I am mistaken again). Also, in HackaTime, you may realize I have had this project under two different names. I didn't intend to make a camera gimbal at first. I just knew I wanted to do some stuff with servos (which was gonna be an arm), but I only have two servos, and they are cheap ones with a lot of backlash. 

Anyways, here is (hopefully) a realistic model of a camera gimbal that someone in the future can take inspiration from if they ever want to design one themselves. Also, I am well aware that the way I made this in OnShape with multiple part studios is not optimal. I honestly don't know what was going through my mind when doing that because I usually only make one. 

Since I wasn't sure if this was a hardware project or just a CAD one at first, I wasn't sure what I had to do, since this way of journaling is relatively new to me. I'm used to the journaling where you just jot down what you did every session on Hack Clubs' website, not on GitHub. When I realized this (which was probably too late), I uploaded some of the Gimbal models that you can see in version history. 

## Building The Project

If you actually aim to build this project (which I unfortunately can't 😭), here is what you will need. 
- XIAO SEED Studio ESP32 board (that supports battery charging) https://www.seeedstudio.com/Seeed-Studio-XIAO-ESP32S3-Plus-p-6361.html?srsltid=AfmBOoqqyYVmSLK2Ie5a3UQ1yRn1snNzlU1zQbV4qhLG1D35R6y5OIkH
- 5V Step-Up Voltage Regulator (This was the one I was gonna use, but don't have. If you can find one for cheaper that fits the same role, go for it) https://www.melopero.com/shop/components/pololu5vstepupvoltageregulatoru3v50f5/
- Analog 2-axis Thumb Joystick with select button https://www.adafruit.com/product/512
- OLED display module 128x32 pixels https://www.amazon.com/MakerFocus-Display-SSD1306-3-3V-5V-Arduino/dp/B079BN2J8V?th=1
- Some sort of IMU CAD model uses this one https://www.adafruit.com/product/3886
- Two servos, in this case, the MG996R High Torque Servos
  Preferabbly all screws are longer than 30mm (depending upon use cases, obviously shorter ones for securing the IMU or servos to around 20mm, just depends on what you've got lying around)
- Eight M5 screws with something to secure them for the servos
- 4 M3 screws with something to secure them (4 long ones)
- 12 M2.5 screws with something to secure them (8 long ones)
- Two high-strength servo screws
- Glue (can be any form of glue, just make sure it is strong to secure the handle to the UI)
- 3D printer

### Slicer Settings

- I just used the preset settings (with supports on) in the Bambu Slicer using a standard 0.4mm nozzle. Nothing fancy unless you're printing anything but PLA.

### Assembly Instructions

1) First, solder all connections to the MCU (depends on what GPIO pins you use, just keep it consistent). Remember that all the 3.3Vs connect to the 3.3V and that the 5V for the servos connect to the end of the step-up
2) Bolt down the pitch servo and the IMU (that way you don't have issues with wiring later)
3) Run those wires through the dedicated CABLES hole and feed them through everything. Secure the XIAO at the bottom of the handle
4) Put in the Joystick and OLED first, and finally the yaw servo.
5) Secure everything once more with the screws and close up the housing for the main UI box.
6) Glue the handle to the UI box
7) screw the servo screws in and anything else that is not screwed in.


