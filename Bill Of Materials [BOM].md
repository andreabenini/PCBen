# PCBen Bill Of Materials (BOM)
## Hardware
- Arduino, CNC shield, Pololu stepper drivers, usb cable.<br>
  those might be purchased individually or as a complete kit, for example Amazon has
  https://www.amazon.com/gp/product/B07HF391GN/ref=ppx_yo_dt_b_asin_title_o06_s00?ie=UTF8&psc=1
  but same stuff might be taken from Aliexpress, Banggood, DealeXtreme, ...<br>
  Individually you might need these materials:
    - Arduino Uno R3 _(ATmega328P clone)_. An arduino Mega is not needed for this project, massive
      computation is crunched on remote machine (Desktop PC, RPi, ...)
    - USB cable for the Arduino board (might be USB-A or microUSB depending on official or chinese
      cloned boards)
    - Arduino V3 Shield CNC stepper motors driver
    - __#4__ Pololu A4988 stepper motor driver carrier
- NEMA23 stepper motor
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


## Software
- **GRBL v1.1** from [github official page](https://github.com/gnea/grbl), built with Arduino `v1.8.10`
    downloaded Linux Distro package repository. Compiled and loaded from Arduino IDE, see software
    configuration information
