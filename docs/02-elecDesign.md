---
layout: default
title: Electronics Design
nav_order: 3
---

# Electronics Design
---
## Designing a PCB using EAGLE

To create our own circuit board, we have to use a CAD tool to design the schematic and drawing its layout. Autodesk EAGLE is a software that helps us do just that. 

In EAGLE, there are two windows called SCH and BRD. We can switch between the schematic and board button to design a pcb.<br><img src="https://github.com/aloethere/EP1001/blob/gh-pages/images/elecDesign%20img/sch%20brd%20button.png?raw=true">  

# Assignment: Redraw an [echo hello world board](http://academy.cba.mit.edu/classes/embedded_programming/index.html#echo) (add at least a button and led)
---

I will be making an echo board using the ATtiny85 chip. The datasheet can be found [here](http://www.atmel.com/images/atmel-2586-avr-8-bit-microcontroller-attiny25-attiny45-attiny85_datasheet.pdf.). To get started, I will need to download and install the component library. The library I'm using is [fab.lr](https://gitlab.fabcloud.org/pub/libraries/electronics).

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
2. Create connections between them.
3. Label our components name and their value. 
4. Verify the design using ERC. 
5. Go to board view to position our components and route traces.

<img src="https://github.com/aloethere/EP1001/blob/gh-pages/images/elecDesign%20img/completed%20schematic.png?raw=true" width="500">
<br><sub><em>This is a screenshot of my completed schematic</em></sub>

### Editing the Board

When we move to Board view, the components that we have just wire will be jumbled up. We will have to re-arrange the traces accordingly, up to the user's design.

1. Move individul components around. Rotate to figure out the simplest pathway.
2. Route all the traces. Or use the autorouter feature.
<img src="" >


3. Use DRC to select wire dimention. 
<img src="" >








 







