Now it's time to deal with some software to create a working toolchain and produce a stable image
later on. I assume you already have one of the latest Arduino IDE installed in your computer, I'm
currently using `v1.8.10` but your favorite version should work fine too.
This guide won't cover Arduino or GRBL installation, please refer to relative sites for further details:
- [Arduino website](https://www.arduino.cc/) for installing the Arduino IDE on your desktop
- [GRBL firmware](https://github.com/gnea/grbl) for downloading original GRBL firmware

Here I'm covering just what I did to install and compile the firmware, further modifications and updates
are reported as ready made binary/hex updates through website software section.

### Compiling and Loading GRBL software on Arduino
- Download latest zip from https://github.com/gnea/grbl/archive/master.zip and unzip it somewhere
    - Get **grbl** folder from your unzipped location and copy it to arduino '_libraries_' dir.
        - linux: /usr/share/arduino/libraries/ (mostly, but it depends on your distro)
        - OSX: ~/Documents/Arduino/libraries/
        - windows: My Documents\Arduino\libraries\
    - or copy it wherever you've installed your Arduino IDE
- On Arduino IDE
    - Refer to Arduino website or GRBL fimware wiki pages to understand how to setup usb/serial
      ports, speed, device, ...   In my case I'm using an `Arduino Uno` on `/dev/ttyUSB0`, here
      are few links for reference (and credits)
        - https://www.arduino.cc
        - https://github.com/gnea/grbl/wiki/Compiling-Grbl
    - Select menu option **Sketch** / **Include Library** / **Add .ZIP Library** And select the
      directory where you've copied the grbl library (_in my case: /usr/share/arduino/libraries_)
    - Now you can see it loaded if it's shown in **Sketch** / **Include Library** under the
      _Contributed Libraries_ section
    - Open `grblUpload` Arduino example, compile it and upload to your board
        - **There's no need to customize the firmware yet, just take it as it is without mods**
        - Menu **File** / **Examples** / **grbl** / **grblUpload** and a new window will open,
          do not modify the example in any way if you're not understanding what you're doing
        - Press **Ctrl+R** (or menu `Sketch` / `Verify/Compile`) to build the uploader.
          Ignore `Low memory available, ...` message, that's not a real error, it's just a warning
        - Press **Ctrl+I** (or menu `Sketch` / `Upload`) to upload your newly compiled firmware

Your Arduino is now loaded and ready to be used.

> **Optional:**<br>
> You can even skip the `Arduino IDE` section and use `avrdude` with ready made `grbl.hex` file
  if you don't want to get in the way with the Arduino IDE stuff, take a look at
  https://github.com/gnea/grbl/wiki/Flashing-Grbl-to-an-Arduino for details


### Ready made `grbl.hex` file
In the newly added [software section](../../software/) I've added latest `grbl.hex` compiled firmware
if you're interested
