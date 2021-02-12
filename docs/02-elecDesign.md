---
layout: default
title: Electronics Design
nav_order: 3
---

# Electronics Design
---
## Designing a PCB using EAGLE

To create our own circuit board, we have to use a CAD tool to design the schematic and drawing its layout. Autodesk EAGLE is a software that helps us do just that. 

In EAGLE, there are two windows called SCH and BRD. We can switch between the schematic and board button to design a pcb.<br><img src="https://github.com/aloethere/EP1001/blob/gh-pages/images/elecDesign%20img/sch%20brd%20button.png?raw=true"><img src="https://github.com/aloethere/EP1001/blob/gh-pages/images/elecDesign%20img/sch%20icon.png?raw=true">  

# Assignment: Redraw an [echo hello world board](http://academy.cba.mit.edu/classes/embedded_programming/index.html#echo) (add at least a button and led)
---

I will be making an echo board using the ATtiny85 chip. This is the datasheet summary for ATtiny85.
<iframe
src="https://github.com/aloethere/EP1001/commit/865b8fd4f021c088d82ff23923f95c0d5d2c2139#diff-1468b0e5a2d190799b958870bca4f151f4387c32c433fab987086b7a6edcf210"></iframe>

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
<br><img src="https://github.com/aloethere/EP1001/blob/gh-pages/images/elecDesign%20img/drc.png?raw=true" width="300">
<img src="https://github.com/aloethere/EP1001/blob/gh-pages/images/elecDesign%20img/drc%20p2.png?raw=true" width="300">


<img src="https://github.com/aloethere/EP1001/blob/gh-pages/images/elecDesign%20img/completed%20board%20design.png?raw=true" width="450">








 







