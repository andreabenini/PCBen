## Hardware
- C8962A - HP Deskjet 5150 Color Inkjet Printer  
  Taken from a trash can, fried motherboard and inkjet nozzle was clearly damaged. BTW it seems to be quite nice and
  solid device. Stainless steel chassis with a solid base, plastic gears are in good shape, some lubrication and
  cleaning is mandatory, minor hw restorations but overall seem to be fine.
  Black mark sensors and motors need few tests but I can see some potential from it. Price: **Free**.
- Arduino, CNC shield, Pololu stepper drivers, usb cable. I already had them in my lab.
  Price: **Free**  
  those might be purchased individually or as a complete kit, for example Amazon has  
  https://www.amazon.com/gp/product/B07HF391GN/ref=ppx_yo_dt_b_asin_title_o06_s00?ie=UTF8&psc=1  
  but same stuff might be taken from Aliexpress, Banggood, DealeXtreme, ...  
  Individually you might need these materials:
    - Arduino Uno R3 _(ATmega328P clone)_. An arduino Mega is not needed for this project, massive
      computation is crunched on remote machine (Desktop PC, RPi, ...)
    - USB cable for the Arduino board (might be USB-A or microUSB depending on official or chinese
      cloned boards)
    - Arduino V3 Shield CNC stepper motors driver
    - __#4__ Pololu A4988 stepper motor driver carrier
- Raspberry Pi, whatever version you want.  
    I already have an acient RPi v1, computing power is enough so there's no need for a powerful
    version, take whatever board you prefer, even a Zero is fine. A wireless adapter is a nice have
    in order to avoid ethernet cables. In my case I also added Asus USB-N10 wifi adapter,
    you can skip it if you already have a raspberry with builtin wifi on it.
- TFT touch screen for the Raspberry. A generic 26pin TFT display can be connected to 40 pin
    Raspberry board too (v2,3,4) so just take it your preferred one, mine is
    [this one](https://www.banggood.com/3_2Inch-320x240-Resolution-TFT-LCD-Touch-Screen-for-Raspberry-Pi-3-Model-B2-Model-BB-p-1370870.html?rmmds=search&cur_warehouse=CN)
    but the only requirement is the Raspberry compatibility.
- 5V DC 2A power supply, provides power to Arduino, CNC Shield and Raspberry Pi boards. Not purchased
    outside but refurbished from my spares. Price **Free**
- 24V DC 10A previously used in my lab for other purposes, now using it to provide power to NEMA motors.
    Price **Free**
- NEMA23 stepper motor (X Axis)
    - Model 23LM-C038-04, R 98-11, Minebea CO. LTD
    - P/N No. T8814
    - Driving with 12V (PC ATX Power Supply), unknown Amps requirements
    - 8 Wires motor (bipolar and unipolar modes), converted to bipolar mode with 4 wires serial cabling

        | Cable        | inner winding coupled to | Connect To          |
        | ------------ | ------------------------ | :------------------ |
        | **`orange`** | green                    |  _brown_            |
        | **`green`**  | orange                   |  **[A1]** `(red)`   |
        | **`blue`**   | brown                    |  **[A2]** `(blue)`  |
        | **`brown`**  | blue                     |  _orange_           |
        | **`red`**    | black                    |  _yellow_           |
        | **`black`**  | red                      |  **[B1]** `(green)` |
        | **`white`**  | yellow                   |  **[B2]** `(black)` |
        | **`yellow`** | white                    |   _red_             |
    - You don't strictly need _this_ motor, It's just a scrap one I had lying around
    - Repurposed from previous hardware, price: **Free**
- NEMA 23 stepper motor (Y Axis)
    - Minebea-Matsushita motor corporation
    - P/N 78800 Rev.C
    - 23KM-K207-03V
    - 6 Wires  motor
    - Repurposed from previous hardware, price: **Free**
- **#3** GT2 fixed timing pulleys, inner: 8mm. 20 Teeth. Source: Banggood, Price: ~(4-5)$ six-pack
- Closed loop GT2 6mm belt (20 Teeth), 110mm. Price (~2 $)
- **#2** 246x17mm drawer slides with ball bearings, picked up at a sale on a local hardware shop,
  they're not so accurate but when moved from a pulley they're quite effective. Price: 4.50€ each
- Aluminium angle bar, 90°, 10x40mm. ~1.5m. Something I already had around so I adapted the project
  to it but you can buy it nearly everywhere.
- M3 nuts and M3x40 bolts. I'm slightly adapting bolts length to match hardware when needed.
- Washers, various sizes, mainly used as guides for the GT2 belt.
- GT2 6mm belt, ~2m. Price: ~2.50$ from common well known chinese shops, free shipping.
- **#2** 20 teeth timing pulley for GT2 belt, bore 8mm. Price: 1.50$ each, free shipping.
- **#1** box 10pcs, 606ZZ ball bearings, bore 6mm. Price: 2.50$ for a set, free shipping.

## Software
- **GRBL v1.1** from [github official page](https://github.com/gnea/grbl), built with Arduino `v1.8.10`
    downloaded Linux Distro package repository. Compiled and loaded from Arduino IDE, see software
    configuration information
