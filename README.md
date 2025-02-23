# Rasgueado

<p align="center">
  <img src="Logo/Rasgueado_Logo.png" width="300">
</p>

## Overview

Rasgueado - A strumming technique associated with flamenco music. Also, replacement controllers for Kinesis Advantage 2 boards.

This project was inspired by work from the [KinT project](https://github.com/kinx-project/kint) and the [Pillz Mod project](https://github.com/dcpedit/pillzmod).

The goal of this project was really simple, I wanted Nice!Nanos and ZMK in my Kinesis Advantage 2 boards. I wanted to make this PCB as simple as possible, so it is really barebones - no LEDs, no plans for batteries, just plain simple ZMK goodness. If I want to use my boards unplugged from my computer, I plug them into an external battery bank. I like this approach better because of super long battery life, easier modularity, and not needing to source tiny batteries.

In addition to the main controller, there are replacement thumb PCBs as well as plate files. Why? I wanted hotswap thumb clusters and carbon fiber plates. So, voila there are now hotswap thumb cluster PCBs and thumb plates that can be made in carbon fiber or whatever other material you please. Nice.

## Usage

You can find the zipped gerbers (for the pcb) and dxf file (for the plates) to send off for manufacturing or clone this repo and make whatever changes you want.

If you are working on the Kicad files, you will need to setup your Kicad to reference the following libraries:

- [ai03-2725 MX_V2 library](https://github.com/ai03-2725/MX_V2)
- [ScottoKicad library](https://github.com/joe-scotto/scottokeebs/tree/main/Extras/ScottoKicad)

## Parts lists

These parts lists are just based off of what I used and are here to help point you in the right direction. Feel free to buy from different places.

### Main Controller

| Part                                             | Qty | Notes                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| ------------------------------------------------ | --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Nice!Nano V2                                     | 1   | The MCU. The brains behind the board. [Link](https://typeractive.xyz/products/nice-nano?_pos=1&_sid=3e0c6f7de&_ss=r)                                                                                                                                                                                                                                                                                                                                                           |
| EZ-Solder Machine Sockets and Headers (optional) | 1   | These are optional, but they make socketing the Nice!Nano a breeze. I won't build without them personally. Your call though. [Link](https://typeractive.xyz/products/ez-machine-sockets-and-headers?_pos=3&_sid=3e0c6f7de&_ss=r)                                                                                                                                                                                                                                               |
| Molex 39-53-2135                                 | 6   | Connector for flat cables of other boards to plug into main board. [Link](https://www.digikey.com/en/products/detail/molex/0039532135/3160262)                                                                                                                                                                                                                                                                                                                                 |
| SN74HC595N Shift Register                        | 1   | Shift registers are cool. They make not enough GPIO pins into more than enough GPIO pins. Praise be to the shift registers. [Link](https://www.amazon.com/dp/B0CBKJXP13?ref_=ppx_hzsearch_conn_dt_b_fed_asin_title_1&th=1)                                                                                                                                                                                                                                                     |
| Shift Register Sockets                           | 1   | Sockets your shift register. Sweeeeeet. [Link](https://www.amazon.com/dp/B00SWO3U1C?ref_=ppx_hzsearch_conn_dt_b_fed_asin_title_2)                                                                                                                                                                                                                                                                                                                                              |
| USB C panel jack (optional)                      | 1   | This gives you a place to attach and detach USB C cables to the keyboard. Is this optional? Yes. It is indeed optional if you want to directly attach a USB C cable to your MCU and run the risk of damaging it and deal with never swapping out the cable easily. It is indeed optional. It's just a bad option not to. You live life on the edge. Installing this does require dremelling some material from your case though. [Link](https://www.adafruit.com/product/4218) |

### Thumbs

| Part                        | Qty | Notes                                                                                                                                                                                                                                                                                                               |
| --------------------------- | --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Molex 39-53-2135            | 2   | Connector for flat cables of other boards to plug into main board. [Link](https://www.digikey.com/en/products/detail/molex/0039532135/3160262)                                                                                                                                                                      |
| Flat flex cables (optional) | 2   | These are just replacement flat cables. They were thinner and easier to work with than the stock ones. You can probably just reuse the stock cables, but I wanted to have extras. So... I did the sensible thing. I bought 30 "backups" [Link](https://www.digikey.com/en/products/detail/molex/0151680815/4143332) |
| 1N4148W SOD-123 diodes      | 12  | Diodes. They let signal go one way, but not the other. Without these there is only chaos. [Link](https://typeractive.xyz/products/smd-diodes?_pos=1&_sid=43b6f9089&_ss=r)                                                                                                                                           |
| Hotswap sockets             | 12  | Makes changing switches a breeze. That's hot. [Link](https://www.gateron.com/products/gateron-hot-swap-pcb-socket?VariantsId=10170)                                                                                                                                                                                 |
| Switches                    | 12  | 12 of whatever MX switches you want.                                                                                                                                                                                                                                                                                |

### Plates

They're reversible, so get two of them.

## Firmware

Link to the firmware repo [here](https://github.com/TBVanderley4545/zmk-config-rasgueado)

## Credits

- The MX footprint is from the [ai03-2725 MX_V2 library](https://github.com/ai03-2725/MX_V2)
- The 39-53-2135 footprint is from the [KinT project](https://github.com/kinx-project/kint)
- The Nice!Nano Footprint is from the [ScottoKicad library](https://github.com/joe-scotto/scottokeebs/tree/main/Extras/ScottoKicad)
- The SOD-123 Footprint is from the [ScottoKicad library](https://github.com/joe-scotto/scottokeebs/tree/main/Extras/ScottoKicad)

## Pictures

![IMG_0245](https://github.com/user-attachments/assets/e619c1c9-191e-42eb-ac16-865e68c547a2)

![IMG_0257](https://github.com/user-attachments/assets/fdcf931c-ce74-4b3b-b948-631788ee88d0)

![IMG_0258](https://github.com/user-attachments/assets/c8552a1e-dfa6-4be6-9a48-7b499c57ade7)

![IMG_0259](https://github.com/user-attachments/assets/5cdd2cc2-242c-4f23-ae66-abb1c9bf6cc9)

![IMG_0256](https://github.com/user-attachments/assets/15f40c14-028d-42bc-863d-983eac55b03c)

![IMG_0260](https://github.com/user-attachments/assets/a8b9f702-5422-4706-bb92-0b9e7d790a45)

