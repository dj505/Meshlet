# [Meshlet](https://5panel.dance/Meshlet)

Meshlet is an open-source and feature-packed LoRa mesh network node, designed to be compatible (but not affiliated) with the Meshtastic® project. It's made to be deployed just about anywhere you want it to be - you can plug in a solar panel and set it up outside, turn it into a pocketable every-day-carry node, wire it up to your car as a mobile repeater, or even just leave it on a windowsill attached to a BBS script/Meshsense/etc. 

**Table of Contents**
1. [Features](#features)
2. [Project Sponsor](#project-sponsor)
3. [Meshlet Docs](#meshlet-docs)

## Features
Features include, but are not limited to...
- USB C, with configurable charge rate limit (250mA, 500mA, 1A)
- LiPo/LiIon and LiFePo4 support
- ESD/TVS protection on the USB port
- Solar input (as well as constant DC input) from 3.3V to 18V, tolerant up to 25V
  - Flexible wiring methods, with dedicated JST PH footprints as well as pads to directly solder wires to!
  - Tested & working with as little as a cheap 80mm 5v solar panel, on an overcast Canadian winter day!
  - Unlike many boards that need a manual reset after too little sunlight drains the battery, the Meshlet should recover on its own!
- Smart power path management, thanks to the BQ25185. No need to worry about unnecessarily cycling the battery!
- JST 2.0 and Picoblade 1.5mm battery connector footprints, to hopefully fit whatever LiPos you've got laying around
- Low operating power, measuring as low as 2.8mA idle current draw (without WiFi)
- Active current/voltage monitoring and reporting on 3 channels over the mesh, via INA3221
  - Ch. 1: Battery
  - Ch. 2: USB & external power
  - Ch. 3: BQ25185 regulated battery output
- Up to 8MB onboard flash
- WIO-SX1262 LoRa radio
- BME280 temperature/humidity/barometric pressure sensor
- I2C expansion port
- Dedicated 3.3V regulators for all major components, each with its own self-resetting fuse, to ensure stable power
- "External notification" header for a MOSFET-driven 3.3V buzzer, LED, vibration motor, etc
- Raspberry Pi RM2 for optional WiFi (and Bluetooth, whenever the firmware supports it)
- Total footprint size of ~42*32mm, less than half the size of a credit card!

## Project Sponsor
This project is sponsored by [PCBWay](https://pcbway.com)! Absolutely massive thank you to them for helping make these projects possible for me.

If you're interested in DIY electronics, I'm sure you're familiar with the name. PCBWay is a manufacturing company specializing in circuit boards, but they also offer services for SMT assembly, CNC milling, 3D printing, sheet metal fabrication, and injection molding! They can manufacture all of the parts for your hobby project, in one convenient place, with fine-grained control over the entire manufacturing process.

I relied pretty heavily on their PCB manufacturing and SMT assembly services to get the final revision of the Meshlet project built & tested. In my past experience, their boards always come out beautiful and pretty near perfect, and these ones are no exception. Their engineers were in contact with me from start to finish, making sure that everything was correct and to spec throughout each step of the process. They sourced all of the parts based on the BOM I provided, ensured that each pick lined up with what I needed, and even sent confirmation photos before the assembly process to ensure that every part was placed & oriented properly. When I mistakenly selected two parts to fit a single footprint, they agreed with my request to ship me the extra parts that I had them order alongside the PCBs, for me to solder by hand if needed after I receive them!

Sponsors like this make a huge difference in allowing me to continue testing & iterating on projects like this one. Without this opportunity, it likely would have stopped at the first revision prototype! Thanks again to PCBWay for reaching out and organizing this opportunity. Please [check them out](https://pcbway.com), and definitely consider using their services for your next project! 

## Meshlet Docs
Assembly notes, firmware, and usage notes can all be found on [the Meshlet webpage.](https://www.5panel.dance/Meshlet/)


