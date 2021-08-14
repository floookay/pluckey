![plucky_logo](./assets/pluckey_logo.png)

The plucky is an ergodox like split keyboard with moderate columnal stagger and a horizontal space key.  
I took inspiration from splitkbs Kyria and bishborias Ergodox design.

![sunny picture](https://gist.githubusercontent.com/floookay/ea7313862e407c9b5aaea3d6ed3ce233/raw/4c37d31cb414b9a7709810434a3b68f4b9b9c0dc/skeleton%2520sunshine.jpg)

## layout

The following physical layouts are supported:  
![supported layouts](https://gist.githubusercontent.com/floookay/ea7313862e407c9b5aaea3d6ed3ce233/raw/0a37fe682f76bbaa55cbc56527e4666bedbf5761/layout%2520possiblities.png)  
And this is the default keymap as of now:  
![keymap](https://gist.githubusercontent.com/floookay/ea7313862e407c9b5aaea3d6ed3ce233/raw/0a37fe682f76bbaa55cbc56527e4666bedbf5761/layout.png)  
[Keyboard-Layout-Editor](http://www.keyboard-layout-editor.com/#/gists/13c9d00bd0c0c9e3fe3b3d8d98672ef9) [(raw)](https://gist.github.com/floookay/13c9d00bd0c0c9e3fe3b3d8d98672ef9)

## pcb

![PCB rev1.1](https://gist.githubusercontent.com/floookay/ea7313862e407c9b5aaea3d6ed3ce233/raw/4c37d31cb414b9a7709810434a3b68f4b9b9c0dc/pcb_rev1.1.jpg)

The pcb is reversible and supports pcb mount MX style switches.  
It was designed using KiCAD and the following external libaries: [keebio-parts](https://github.com/keebio/Keebio-Parts.pretty) and [foostans kbd library](https://github.com/foostan/kbd)  
In order to assemble a pair you'll need the following hardware:

| amount | part                 | description             |
|--------|----------------------|-------------------------|
| 66/68  | key switches         | MX style                |
| 66/68  | diodes               | SMD or THT 1N4148(W)    |
| 2      | mini USB ports       | MX-54819-0519           |
| 2      | TRRS jacks           |                         |
| 2      | tact switch          |                         |
| 2      | pro micros           |                         |
| 2      | micro usb connectors | or two micro usb cables |
| 8      | short wires          |                         |

Additionally I'd recommend getting a pair of hotswapable headers for both pro micros.

**assembly:**  
Start by soldering the diodes, the headers, trrs jack and the mini usb port to the same side of the pcb. Make sure to clip the pins beforehand so they're flush on the other side.  
Now you can align your plate and solder in the switches.  
Plug the micro usb connector into the pro micro and align it according to the pinout on the solder mask. Depending on which headers you chose you might want to add electrical tape to the pro micro that's upside down so it doesnt touch the switch pins. Also nothe that you might have to solder on the controller at an angle if you're going with the default headers in order to be able to plug in the usb cable.  
Solder the wires to the micro usb connector (or cut open your existing cables) and solder the other side to the port headers according to the pinout on the solder mask.

<details>
<summary>more pictures</summary>

![b-side](https://gist.githubusercontent.com/floookay/ea7313862e407c9b5aaea3d6ed3ce233/raw/7f041ae9f5dfb2b95120871c1e2e58ef65b90ba4/pcb_rev1.1_backside.jpg)  
![pcbs soldered](https://gist.githubusercontent.com/floookay/ea7313862e407c9b5aaea3d6ed3ce233/raw/4c37d31cb414b9a7709810434a3b68f4b9b9c0dc/pcbs%2520soldered.jpg)  
</details>
<br>

## case

### monolith

![monolith](https://gist.githubusercontent.com/floookay/ea7313862e407c9b5aaea3d6ed3ce233/raw/4c37d31cb414b9a7709810434a3b68f4b9b9c0dc/monolith.jpg)  
The monolith case is a tray mounted design and 3d printable in two pieces: case and (optional) plate  
It was designed using FreeCAD (and some SolidPython until it got too complex for me) so please feel free to configure the case to your liking. It's fairly parametric set up so depending on what you want to achieve you'll have a few starting points.
In order to assemble the case you'll need the following additional hardware:

| amount | part                 |
|--------|----------------------|
| 8      | M2 4mm screws        |
| 8      | M2 4mm spacers       |

**assembly:**  
After you soldered the PCB you can assemble the case. At first you're going to have to merge the spacers with the posts of the case. To do this heat up your soldering iron, position a spacer with a tweezer and press the spacer down with the tip of your soldering iron (make sure it's clean before this step). Do this with the other spacers, align the plate and pcb and fixate it with the screws.

<details>
<summary>more pictures</summary>

![inside](https://gist.githubusercontent.com/floookay/ea7313862e407c9b5aaea3d6ed3ce233/raw/7f041ae9f5dfb2b95120871c1e2e58ef65b90ba4/monolith.png)  
![usage position](https://gist.githubusercontent.com/floookay/ea7313862e407c9b5aaea3d6ed3ce233/raw/7f041ae9f5dfb2b95120871c1e2e58ef65b90ba4/monolith%2520positioned.jpg)  
![closeup](https://gist.githubusercontent.com/floookay/ea7313862e407c9b5aaea3d6ed3ce233/raw/7f041ae9f5dfb2b95120871c1e2e58ef65b90ba4/monolith%2520left%2520top.jpg)  
![backside](https://gist.githubusercontent.com/floookay/ea7313862e407c9b5aaea3d6ed3ce233/raw/7f041ae9f5dfb2b95120871c1e2e58ef65b90ba4/monolith%2520left%2520back.jpg)  
![bottom](https://gist.githubusercontent.com/floookay/ea7313862e407c9b5aaea3d6ed3ce233/raw/7f041ae9f5dfb2b95120871c1e2e58ef65b90ba4/monolith%2520botched%2520underside.jpg)
</details>
<br>

### skeleton

![skeleton](https://gist.githubusercontent.com/floookay/ea7313862e407c9b5aaea3d6ed3ce233/raw/4c37d31cb414b9a7709810434a3b68f4b9b9c0dc/skeleton%2520raw.jpg)  
The skeleton case is a simple open case for the pluckey pcb.  
The FreeCAD models are included in case you want to adjust the angle for example.  
All you need to do to assemble this case is to clip in the PCB. All you need to do to assemble this case is to clip in the PCB. If you're using encoders you'll have to cut the pins flush.

<details>
<summary>more pictures</summary>

![usage](https://gist.githubusercontent.com/floookay/ea7313862e407c9b5aaea3d6ed3ce233/raw/7f041ae9f5dfb2b95120871c1e2e58ef65b90ba4/skeleton%2520office.jpg)  
![closeup](https://gist.githubusercontent.com/floookay/ea7313862e407c9b5aaea3d6ed3ce233/raw/7f041ae9f5dfb2b95120871c1e2e58ef65b90ba4/skeleton%2520left%2520closeup.jpg)  
![countryside](https://gist.githubusercontent.com/floookay/ea7313862e407c9b5aaea3d6ed3ce233/raw/7f041ae9f5dfb2b95120871c1e2e58ef65b90ba4/skeleton.jpg)  
</details>
<br>

## plate

If you want to print and use a plate I'd suggest you print the tolerance tester first (and maybe decrease the tolerances a bit).  
After you know the right margin for your printer you can adjust it in the plate model and export your plate in the desired layout.

## firmware

flash QMK from my fork [floookay/qmk_firmware](https://github.com/floookay/qmk_firmware/tree/pluckey)  
*&rarr; I'll add it to the official repo soon™ (once I'm fully done)*

## misc

> What where your goals behind designing this keyboard?

One thing I wanted to improve/avoid were keys that needed to be stabilized but at the same time have wider space keys to rest my thumbs on.

Another thing I wanted to achieve with this design was to be fairly flexible in terms of keycaps that can be used.  
Personally, I like the wider ergodox style modifier keys but keycap compability is unfortunatelly not that great beyond blank uniform caps.  
That's why I made the PCB compatible with all 1u keycaps that are offered in ortho keycap sets.

> What's next?

An acrylic sandwich-style case variant.  
I'm also thinking about making a pcb variant for low profile Choc switches with choc spacing.

> What's the story behind the name?

I named the keyboard Pluckey after one of my favorite Animal Crossing villagers „Plucky“. The first letter of the logo represents Pluckys eye.
