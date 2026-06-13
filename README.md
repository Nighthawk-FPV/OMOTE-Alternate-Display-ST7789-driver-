FOLLOW THESE DIRECTIONS AT YOUR OWN RISK! 

If steps aren’t taken during the PCB ordering process (changing the display connector) you will need to do some SMD rework to change out the connector on your own PCB. This is tricky and can take a few tries to get right and not bridge the little pins on the display connector. Should you choose to continue, I’d recommend you get some extra display connectors while you’re ordering your displays!

Required Parts List:
Display (select: capacitive touch and get the “ZIF connector for display” as this will replace the current display connector): https://www.buydisplay.com/2-8-inch-tft-lcd-display-capacitive-touch-screen-st7789v-spi-240x320

Display connector Top Contact (extras/if not ordered with the display): https://www.buydisplay.com/50-pin-0-5mm-pitch-top-contact-zif-connector-fpc-connector

6 pin breakout (for touch controller): https://www.amazon.com/dp/B0DS6M7NKK?ref=ppx_yo2ov_dt_b_fed_asin_title&th=1

Wire (for connecting the breakout to the PCB, 5 connections needed would recommend each connection get its own color): https://www.amazon.com/dp/B0DS6M7NKK?ref=ppx_yo2ov_dt_b_fed_asin_title&th=1


Tools I used: 
Soldering iron: https://www.amazon.com/FNIRSI-HS-02A-Soldering-Temperature-Electronics/dp/B0F8HBFQ7S/ref=sr_1_7?crid=SBCJUD88EAZZ&dib=eyJ2IjoiMSJ9.dijywYSNZLDRud-kl9yYaML7F1jOFnOoP4Q5z4GRXM7YYCFckFun7E3lmCa37O7t9uP-l_0RAcG6aASSX0s7EELTlJc5DIs4gHqv3knZZGNi1MajqLVkeOn461Q0x9cfrulK4jzDFJcwGs06pj-BpThsOfrGmtqkLFsnFVZPj9MdRLXpE_bxVNvbbJlaEktgSHSriPtqxfmL0ZraeNL9rKNA2rFnMsxTpxCCNoP8MIc0iKJ-F_trYoA5Fu5pKKb0-qsT7LxgtftSUpZ2RwIpOP1ot8WsbW-1waIYb9_7c34.IBErJoTsbfRDBfAaUp2niWD2bNySsLdxvN5h3I0-D7Y&dib_tag=se&keywords=fnirsi+soldering+iron&qid=1781389809&sprefix=fnirsi%2Caps%2C232&sr=8-7

SMD Rework capability (this can be a hot air gun, hotplate etc. I used this hotplate with great success): https://www.amazon.com/dp/B082H12PPT?ref=ppx_yo2ov_dt_b_fed_asin_title

Solder paste: https://www.amazon.com/dp/B0BNKKRYK9?ref=ppx_yo2ov_dt_b_fed_asin_title&th=1

Tweezers (any small metal-tip tweezers should work)


Assembly Instructions
If you did not get the buttons populated on the bottom side or you are using a hot air gun, you can skip the next step.

If you are using a hotplate, desolder and remove the power button (on the top of the remote) so the part of the PCB with the display connector will lay flat on the hotplate.

Set the hotplate to 300C and wait for it to get to temp. Place the PCB on the hotplate (connector up) making sure the part with the display connector is touching the hotplate and wait for the solder to melt (periodically bumping the connector to see if it moves). Carefully remove the display connector with metal tweezers being careful not to bump any other components as they are all melted now.

Once the display connector is removed, take the PCB off the hotplate and let it cool for a bit. 

Once the PCB is cooled, put solder paste on all the pads for the connector (being careful to not put very much on the main pins as too much will wick the solder up and short pins on the connector). 

Place the new display connector on the PCB making sure it is sitting in the right place for all the pins to touch properly.

Set the hotplate to the appropriate temperature for your solder paste and place the PCB on the plate once it reaches the proper temperature and wait for the solder paste to melt. You may need to bump the connector into the right place once the solder paste melts.

Make sure there are no shorted pins on the connector.

Now that the new display connector is soldered in place, plug the display into the connector and upload the new code to make sure the connector works before you move on (see code section below).

Solder wire to the 6 pin breakout board. 

Solder the wires to the corresponding locations on the PCB (if you purchased the ones in the amazon link, you can use the pinout below along with the image titled "PCB Labeled"):
    Pin 1 on breakout = Power
    Pin 3 on breakout = Reset
    Pin 4 on breakout = SCL
    Pin 5 on breakout = SDA
    Pin 6 on breakout = Ground

Wire manage and remove plastic in the remote plastic to accommodate the new wire and board.


Code Instructions

Replace the following files with the provided files.

OMOTE-Firmware-main\hardware\ESP32\tft_hal_esp32.cpp

OMOTE-Firmware-main\hardware\ESP32\tft_hal_esp32.h

Good Luck!
