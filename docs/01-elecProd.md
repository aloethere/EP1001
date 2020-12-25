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

This are generally the steps on how to create your own PCB:

**Step 1: CAD**<br>
To design our schematics, we are using [EAGLE](https://www.autodesk.com/products/eagle/overview?plc=F360&term=1-YEAR&support=ADVANCED&quantity=1) as our software. EAGLE lets PCB designers make circuit boards by editing their schematics before printing it out. You can check out more of this topic on my [Electronics Design](https://aloethere.github.io/EP1001/docs/02-elecDesign/) page.


**Step 2: CAM**<br>
After designing the circuit, we will have to generate the G-code based on the board layout. G-code is the language of CNC machines. It instructs the machine on how and where to move. There are two ways to go about this. 

1. Using [mods](https://fabfoundation.github.io/mods/)
- Prepare image file. (png/svg)
- To set parameters: right click to begin > programs > open programs > G-code: mill 2D pcb.

<img src="https://github.com/aloethere/EP1001/blob/gh-pages/images/mods%20overview.png?raw=true" width="400"/><br><sub><em>Mods Community interface.</em></sub>
<br>
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

ISP (In-system Programming, also called in-ciruit serial programming) Programmers is used to program microcontrollers while being while installed in a complete system, rather than requiring the chip to be programmed prior to installing it in the system. This allows the microcontrollers to be re-programed without being removed from the target board. 

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

<img src="https://github.com/aloethere/EP1001/blob/gh-pages/images/recommended%20setting%20for%20stepcraft.png?raw=true" width="200"/>
<br><img src="/images/import traces mods.png" width="200"/>
<br><img src="/images/traces parameters mods.png" width="200"/>


Then, click the Calculate button to download the G-code. These are the files that I generated. It should end with <em>.nc</em>.
<br>[fts_mini_traces.png.nc](/source/fts_mini_traces.pngsite.nc){: .btn }
<br>[fts_mini_cut.png.nc](/source/fts_mini_cut.pngsite.nc){: .btn }


<img src="https://media.giphy.com/media/vfPikxySa4hsiivEE3/giphy.gif" width="300" height="200"/>



<img src="https://github.com/aloethere/EP1001/blob/gh-pages/images/recommended%20setting%20for%20stepcraft.png?raw=true" width="600"/>

<img src="https://media.giphy.com/media/vfPikxySa4hsiivEE3/giphy.gif" width="300" height="200"/>
<img src="https://media.giphy.com/media/2m8gV2mPMlBYtIMlCw/giphy.gif" height="200"/>