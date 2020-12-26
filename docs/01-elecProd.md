---
layout: default
title: Electronics Production
nav_order: 2
---

# Electronics Production
---

## PCB Fabrication

Printed Circuit Board or PCB are used to configure all the electronic components of a device together. The traces of a circuit board connects all of the electrical signals from one junction to another. In our last module, we used an Arduino to help us assemble our circuit. Now going up a level higher, we learnt how to build our own PCB. This means we have the flexibilty to design and customise our microcontroller board for better product integration.
<br>
<center><img src="https://github.com/aloethere/EP1001/blob/gh-pages/images/pcb%20intro.jfif?raw=true" width="300"/>
<br>
<sub><em>A PCB of an electronic device.</em></sub></center>

There are a few methods of pcb manufacturing out there. Here, we will be only focusing on milling them on a CNC machine. This are generally the steps on how to create your custom PCB:

**Step 1: CAD**<br>
To design our schematics, we are using [EAGLE](https://www.autodesk.com/products/eagle/overview?plc=F360&term=1-YEAR&support=ADVANCED&quantity=1) as our software. EAGLE lets PCB designers make circuit boards by editing their schematics before printing it out. You can check out more of this topic on my [Electronics Design](https://aloethere.github.io/EP1001/docs/02-elecDesign/) page.


**Step 2: CAM**<br>
After designing the circuit, we will have to generate the G-code based on the board layout. G-code is the language of CNC machines. It instructs the machine on how and where to move. There are two ways to go about this. 

1. Using [mods](https://fabfoundation.github.io/mods/)
- Prepare image file. (png/svg)
- To set parameters: right click to begin > programs > open programs > G-code: mill 2D pcb.

<img src="https://github.com/aloethere/EP1001/blob/gh-pages/images/mods%20overview.png?raw=true" width="400"/><br><sub><em>Mods Community interface.</em></sub>

1. Using EAGLE
- Generate using EAGLE's pcb-gcode ULP (User Language Programme).
- Set parameters. 
<br>
<sub>I elaborated more on the [Electronics Design](https://aloethere.github.io/EP1001/docs/02-elecDesign/) page.</sub>

Before milling, we can check the simulation with [CAMotics](https://camotics.org/).

**Step 3: Milling**<br>
After generating the G-code, you can now prepare the board for milling. You should have 2 files ready to load; etch(traces) and mill(outline). Familiarise yourself with the CNC machine you are using. In Fablab SP, we are using the [STEPCRAFT 420](https://www.stepcraft.us/shop/product/20450-stepcraft-d-420-cnc-machine-self-assembly-kit-211?category=26) and [UCCNC](https://www.cncdrive.com/UCCNC.html) for the CNC control software.

Some G-code lines that are useful to know (example):  
F60.000 - Move at a feed rate of 60  
Z-0.050 - Z-coordinate depth of -0.05  
X10.903 - Move to this X-coordinate  
Y1.9556 - Move to this Y-coordinate  

**Step 4: Assembly**<br>
With your freshly milled pcb board, you can now solder the components together. Refer to your schematic to assign the parts and orientation correctly. Use a multimeter to inspect for shorts between VCC and GND.

# Assignment: Make an in-circuit programmer by milling and stuffing the PCB
---

## Building a FabTinyISP Programmer

ISP (In-system Programming, also called in-ciruit serial programming) Programmers is used to program microcontrollers while being installed in a complete system, rather than requiring the chip to be programmed prior to installing it in the system. This allows the microcontrollers to be re-programed without being removed from the target board. 

Here are some articles explaining more about it:
<br>[https://en.wikipedia.org](https://en.wikipedia.org/wiki/In-system_programming).
<br>[http://www.ethernut.de](http://www.ethernut.de/en/tools/in-system-programming.html).

The PCB that i'm making is based on the NAme's FabTinyISP. This board was specifically designed to be made in a Fablab. More about it [here](http://fab.cba.mit.edu/classes/863.16/doc/projects/ftsmin/index.html)

First, i save the png files in my computer. 

<img src="https://github.com/aloethere/EP1001/blob/gh-pages/images/traces.png?raw=true" width="300"/>
<br>[Traces 1000 dpi](http://fab.cba.mit.edu/classes/863.16/doc/projects/ftsmin/fts_mini_traces.png){: .btn .mr-1 }
<br><img src="https://github.com/aloethere/EP1001/blob/gh-pages/images/outline.png?raw=true" width="300"/>
<br>[Outline 1000 dpi](http://fab.cba.mit.edu/classes/863.16/doc/projects/ftsmin/fts_mini_cut.png){: .btn .mr-1 }

I will be generating the G-code in mods community. Import the traces file and set the parameters. This is the recommended setting for STEPCRAFT 420.

<img src="https://github.com/aloethere/EP1001/blob/gh-pages/images/recommended%20setting%20for%20stepcraft.png?raw=true" width="600"/>
<br><img src="https://github.com/aloethere/EP1001/blob/gh-pages/images/import%20traces%20mods.png?raw=true" width="184" height="500"/>
<img src="https://github.com/aloethere/EP1001/blob/gh-pages/images/traces%20parameters%20mods.png?raw=true" width="220" height="500"/>
<br><sub><em>Setting up parameters in Mods Community</em></sub>

Then, click the Calculate button to download the G-code. Do the same for the Outline with its correct settings. These are the files that I generated. It should end with <em>.nc</em>.

[fts_mini_traces.png.nc](https://github.com/aloethere/EP1001/blob/gh-pages/source/fts_mini_traces.pngsite.nc){: .btn }
<br>[fts_mini_cut.png.nc](https://github.com/aloethere/EP1001/blob/gh-pages/source/fts_mini_cut.pngsite.nc){: .btn }

Now, you will need to prepare a few things at the cnc milling station. They are:<br>
1. Files ready in a thumbdrive
2. Blank circuit board. We use copper clad plate.
3. Bits and end mills
4. Double-sided tape and masking tapes
5. Wrench to tighten spindle

Hold down the copper plate on the MDF board. I will be taping underneath with a double-sided tape and tape on its side to secure it down. Then, attached the end mill. Make sure it is secured tight.

<img src="https://github.com/aloethere/EP1001/blob/gh-pages/images/taped%20board.png?raw=true" width="300"><br><sub><em>My attached copper baord</em></sub>

<img src="https://github.com/aloethere/EP1001/blob/gh-pages/images/1mm%2030deg.png?raw=true" width="300"/><br><sub><em>0.1mm 30 deg V bit for etching</em></sub> 

<img src="https://github.com/aloethere/EP1001/blob/gh-pages/images/0.8%20mm%20bit.png?raw=true" width="300"/><br><sub><em>0.8 mm end mill for cutting outline</em></sub>

Load the file in UCCNC. Set the X and Y origin. Then calibrate the Z-axis. Select Start cycle.

<img src="https://media.giphy.com/media/CRA6Jxehr7jp2eHpRk/giphy.gif" width="400"/><br><sub><em>Calibrating Z-axis on a flat surface with a touch plate</em></sub>

<img src="https://media.giphy.com/media/vfPikxySa4hsiivEE3/giphy.gif" width="200"/>
<img src="https://github.com/aloethere/EP1001/blob/gh-pages/images/cutting%20the%20outline.jpeg?raw=true" width="300"/><br><sub><em>Milling in operation</em></sub>

<img src="https://media.giphy.com/media/2m8gV2mPMlBYtIMlCw/giphy.gif" width="400"/><br><sub><em>What you should see on the laptop</em></sub>

To cut the outline, leave the origin point at the same place. Calibrate the Z-axis again. And change the bit to 0.8mm end mill. 

I prepared the componets and start soldering. 

<img src="https://github.com/aloethere/EP1001/blob/gh-pages/images/soldering.jpeg?raw=true" width="=300"/><br><sub><em>Soldering</em></sub>






### Things that could happen

Bit breaks. Therefore always give attention to your milling process. We could control the speed setting to prevent it from breaking. Immediately stop operation if it happens.

<br><img src="https://github.com/aloethere/EP1001/blob/gh-pages/images/what%20could%20go%20wrong.png?raw=true" width="300">