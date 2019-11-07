# About
This projects aims to be a reference and a building blog for a low cost PCB milling machine created
with spare parts. A generic hobbyist machine range from _250$_ for a noname chinese clone and can go
up to _2000$_ for a semi-professional device. This project wants to create a generic device with
refurbished or spare parts and occasional manual tools, it's not intended as a pro tool but just
something you can easily use for creating your personal PCBs in your spare time.

Instead of spending money on low cost chinese imports it tries to be an experiment with readily
available parts and open source GRBL firmware. Open hardware nature of this project means to be a
reference and a discussion topic for creating an extensible tool for occasional PCB production.
If you don't want to deal with chemistry or time consuming steps to create just a simple Printed
Circuit Board this might be an interesting project.

Created with repurposed devices or salvaged hardware tries to keep up with low cost chinese clones,
improvements are driven by using cheap parts available in every common hardware store. No special
tools are required to create it: 3D printers, plasma cutters or milling machines are not needed.

This is not a generic milling machine but something expecially targeted for occasional PCB production,
Z-Axis needs to be precise enough for it doesn't need to be that tall. NEMA Motors, steel frame, end
stops, Arduino and a CNC shield are basic building blocs for this device; I haven't purchased any
of them because they're coming from previous projects or scavenged from abandoned / faulty hardware.

I don't have access to a plasma cutter to build a sturdy frame or a 3d printer to create perfect
linear guide rail or connections nor I don't want to waste money just for tinkering with something.
An improved/future version would probably use 3D printing and costly tools to keep up with the
quality but it's not a necessity yet. If you're looking for a professional machine you're in the
wrong place and you probably already know you need to spend big bucks on that.

## Building blocks
- OpenSource GRBL firmware
- Arduino + CNC shield for driving motors. I already have them lying around but you can
purchase something from common and well known usual chinese resellers for few bucks
- NEMA 23 motors, 17s are fine too but in my case that's what I've got for free from acient
  thermal printers. Steel frame doesn't really match with NEMA17 and moving parts but you can try it
- Raspberry Pi as host controller. Every USB host capable device supported by GRBL is fine but I have
  a lot of them all around. That's because I don't want to keep this machine costantly connected to a
  PC or a laptop
- Cheap ATX power supply. Not really needed because I'm using just few Amps @12V but it's really easy
  to recover a cheap one from dismantled PCs
- Manual tools and common parts from your local hardware store, nothing really complex there...

## Firmware and Software
- GRBL because it's easy to tweak
- RPi OS. I'm now using Arch Linux but Raspbian or other compatible distros are fine, your mileage may
  vary
- Scripting and utilities, built for automating GRBL related software and involved toolchain

