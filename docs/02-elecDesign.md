---
layout: default
title: Electronics Design
nav_order: 3
---

# Electronics Design
---
## Designing a PCB using EAGLE

To create our own circuit board, we have to use a CAD tool to design the schematic and drawing its layout. Autodesk EAGLE is a software that helps us do just that. 

In EAGLE, there are two windows called SCH and BRD. We can switch between the schematic and board button to design a pcb.<br><img src="https://github.com/aloethere/EP1001/blob/gh-pages/images/elecDesign%20img/sch%20brd%20button.png?raw=true">    <img src="https://github.com/aloethere/EP1001/blob/gh-pages/images/elecDesign%20img/sch%20icon.png?raw=true">  

# Assignment: Redraw an [echo hello world board](http://academy.cba.mit.edu/classes/embedded_programming/index.html#echo) (add at least a button and led)
---

I will be making an echo board using the ATtiny85 chip. This is the datasheet summary for ATtiny85 found on Microchip website.
<iframe src="https://ww1.microchip.com/downloads/en/DeviceDoc/Atmel-2586-AVR-8-bit-Microcontroller-ATtiny25-ATtiny45-ATtiny85_Datasheet-Summary.pdf" width="80%" height="500px"></iframe>

To get started, I will need to download and install the component library. The library I'm using is [fab.lr](https://gitlab.fabcloud.org/pub/libraries/electronics).

<img src="https://github.com/aloethere/EP1001/blob/gh-pages/images/fab.lr%20step1.png?raw=true" width="330">
<img src="https://github.com/aloethere/EP1001/blob/gh-pages/images/fab.lr%20step%202.png?raw=true" width="330"><img src="https://github.com/aloethere/EP1001/blob/gh-pages/images/fab.lr%20step%203.png?raw=true" width="330">
<br><sub><em>Steps to download fab.lr</em></sub>

In my file manager, I place the downloaded fab.lr (named eagle_fab) in the EAGLE library.

<img src="https://github.com/aloethere/EP1001/blob/gh-pages/images/elecDesign%20img/save%20to%20eagle%20lib.png?raw=true" width="330"> 

Now for me to use it, at the EAGLE control panel, go to the directory and select the library. A green dot indicates that it is in use. 

<img src="https://github.com/aloethere/EP1001/blob/gh-pages/images/elecDesign%20img/fab%20libr%20in%20use%20in%20eagle.png?raw=true" width="330">

Create a new project.

We will have to add and connect components in the schematic window first. To add components, select the add parts icon <img src="https://github.com/aloethere/EP1001/blob/gh-pages/images/elecDesign%20img/add%20parts%20icon.png?raw=true">. You can either look through the listed libraries for a component to add or you can type it into the box above the "drop" button.

<img src="https://github.com/aloethere/EP1001/blob/gh-pages/images/elecDesign%20img/how%20to%20add%20parts.png?raw=true" width="500">

### Editing the schematic

1. Add in the right components for your board.
2. Use NET tool to wire our parts together. <img src="https://github.com/aloethere/EP1001/blob/gh-pages/images/elecDesign%20img/net%20icon.png?raw=true" width="20">
3. Use NAME tool to identify our components/name our nets. <img src="https://github.com/aloethere/EP1001/blob/gh-pages/images/elecDesign%20img/name%20icon.png?raw=true" width="20">
4. Use VALUE tool to set resistors resistance or capacitors capacitance. <img src="https://github.com/aloethere/EP1001/blob/gh-pages/images/elecDesign%20img/value%20icon.png?raw=true" width="20">
5. Verify the design using ERC. 
6. Go to board view to position our components and route traces.

Refer to this Sparkfun link for detailed explanation on wiring up schematic on EAGLE. [https://learn.sparkfun.com/tutorials/using-eagle-schematic](https://learn.sparkfun.com/tutorials/using-eagle-schematic)

<img src="https://github.com/aloethere/EP1001/blob/gh-pages/images/elecDesign%20img/completed%20schematic.png?raw=true" width="500">
<br><sub><em>This is a screenshot of my completed schematic</em></sub>

### Editing the Board

When we move to Board view, the components that we have just wire will be jumbled up. We will have to re-arrange the traces accordingly, up to the user's design.

1. Move individual components around. Rotate to figure out the simplest pathway.
2. Route all the traces. Or use the autorouter feature.
<br><img src="https://github.com/aloethere/EP1001/blob/gh-pages/images/elecDesign%20img/autorouter.png?raw=true" width="150">

3. Use DRC to select wire dimension. 
<br><img src="https://github.com/aloethere/EP1001/blob/gh-pages/images/elecDesign%20img/drc.png?raw=true" width="200">
<img src="https://github.com/aloethere/EP1001/blob/gh-pages/images/elecDesign%20img/drc%20p2.png?raw=true" width="200">

4. Create a border under the milling layer. (blue)

It it safe to say, to cnc a pcb in fablab, use this parameters to determine width of traces:
* 10mil / 0.25mm for *very fine traces*
* 16mil / 0.4mm  for *traces*
* 32mil / 0.8mm  for *board outline*

<img src="https://github.com/aloethere/EP1001/blob/gh-pages/images/elecDesign%20img/completed%20board%20design.png?raw=true" width="450"><br><sub><em>Finalised board design before generating Gcode</em></sub>

### Export board design

Select the LAYER icon located on the top left of the screen. <img src="">

From here you may use EAGLE's pcb-gcode setup or export a high resolution png image. Since EAGLE has a setup to generate Gcode, i'll would like to try exporting my board design directly from EAGLE software.

Run pcb-gcode ULP. <img src="">









 







