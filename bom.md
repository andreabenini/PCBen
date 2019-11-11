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
- NEMA 23 stepper motor (Y Axis)
    - Minebea-Matsushita motor corporation
    - P/N 78800 Rev.C
    - 23KM-K207-03V
    - 6 Wires  motor
- #1 GT2 fixed timing pulleys, inner: 8mm. 20 Teeth
- Closed loop GT2 6mm belt (20 Teeth), 110mm


## Software
- **GRBL v1.1** from [github official page](https://github.com/gnea/grbl), built with Arduino `v1.8.10`
    downloaded Linux Distro package repository. Compiled and loaded from Arduino IDE, see software
    configuration information
