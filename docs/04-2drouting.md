---
layout: default
title: 2D Computer Controlled Machining
nav_order: 5
---

# 2D Computer Controlled Machining
---

## Large format CNC machining

<br><img src="https://github.com/aloethere/EP1001/blob/gh-pages/images/2dcnc/cncdef.png?raw=true" width = "450">

CNC machining is a subtractive manufacturing process. Here, I mainly learnt about 3-axis milling using the Versatil 2D CNC router in Fablab.

The file design can be prepared in a CAD software. Once the design is finalised, you can export the file as DXF and work on Vcarve Pro or go to the Manufacture workspace on Fusion360 to generate your Gcode.

From what I understood, CNC milling can be used on materials such as wood, foam and soft metals. I think its better to read up on the approved material for the machine you're using.

## Understanding how to operate CNC machine

<br><img src="https://github.com/aloethere/EP1001/blob/gh-pages/images/2dcnc/overviewcnc.png?raw=true" width = "350">

1. Put the stock on the bed. 
2. There are a few ways to strap in the material. Screw, clamp or use vacumm table.
3. There must be a sacrificial layer under your stock.
4. Import your Gcode on the program software. We using NC-EASY
5. Set X, Y and Z axis.
6. Switch on the dust collector.
7. Start. Be aware of your surroundings.

### Tooling

<img src="https://github.com/aloethere/EP1001/blob/gh-pages/images/2dcnc/tooling.png?raw=true" width = "450">
<br>flute: 
<br><img src="https://github.com/aloethere/EP1001/blob/gh-pages/images/2dcnc/flute.png?raw=true" width = "450">

### Speeds and feeds

Speeds: Spindle rotational speed
<br>Feeds: Machine linear speed. Also known as feedrate.
<br>Chipload: 
<br><img src="https://github.com/aloethere/EP1001/blob/gh-pages/images/2dcnc/chipload.png?raw=true" width = "200">
<img src="https://github.com/aloethere/EP1001/blob/gh-pages/images/2dcnc/chips.png?raw=true" width = "185">
<br>If chipload too small, could cause fire. More rubbing on the bit. 

**Formula:**
<br>Feedrate: spindle speed x spindle speed x flute

### Toolpath

- Nesting
- 2D or 2.5D
- Dogbone
- Tabs

### <span style="color:red"> Safety </span>
1. Wear protective equipment: Safety goggles and hearing protection.
2. Do not wear loose clothes,
3. Keep a safe distance from the bit


# Assignment: Make something big (Minimum 300mmx300mm)
---

I attempt to build an activity cube for toddlers. The faces will look like this. 
<iframe src="https://ichat754.autodesk360.com/shares/public/SH56a43QTfd62c1cd968e1fd6b895eaed415?mode=embed" width="640" height="480" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>

## The CAM process

From Fusion, dxf is exported to create my toolpath on VcarvePro. To do this, need to move the Z origin plane to the top face of the bodies.
<br><img src="https://github.com/aloethere/EP1001/blob/gh-pages/images/2dcnc/origin%20plane.png?raw=true" width = "330">

<img src="https://github.com/aloethere/EP1001/blob/gh-pages/images/2dcnc/origin%20plane2.png?raw=true" width = "330">
<br><img src="https://github.com/aloethere/EP1001/blob/gh-pages/images/2dcnc/dxf.png?raw=true" width = "350">

Then select "import vectors" under VcarvePro. On Vcarve pro, we need to set the instructions for the toolpath. In my design, there are 2 types of toothpath; Pocket and Profile. Selecting "profile" will cut through the material and "pocket" is not cutting all the way through. 

This area has to hv 2 separate pocket toolpath.

<img src="https://github.com/aloethere/EP1001/blob/gh-pages/images/2dcnc/problempocket.png?raw=true" width = "350">

The end mill I am using is 6mm.

This is the settings used for th 2d profile toolpath.
<br><img src="https://github.com/aloethere/EP1001/blob/gh-pages/images/2dcnc/2dprofiletoolpath.png?raw=true" width = "150">

Then, calculate the toolpath and preview to make sure they are moving as we wanted.

I check the wood stock width and make sure they are correct.

When satisfied, secure the stock wood on the sacrifiacial board using screws.
<img src="https://github.com/aloethere/EP1001/blob/gh-pages/images/2dcnc/sacrificial%20layer.png?raw=true" width = "250">

1. Launch the NC-Easy software
2. Import the Gcode.
3. To calibrate Z-axis, click "tool measure". Note: There is a default position for the calibration of the Z-axis. Place the z-axis height sensor.
<br><img src="https://github.com/aloethere/EP1001/blob/gh-pages/images/2dcnc/toolmeasure.png?raw=true" width = "250">
4. Set X and Y axis. Can use the handheld remote to
5. Power on the dust collector machine.
6. When everything is ready, press "Start" and "Ok".
7. Use vacumm to clean the chips created. 

Cutting looks nice. However, due to the sacrificial layer wood shown in the picture not fixed tightly the Z surface is not entirely flat. So this happenned. :(
<br><img src="https://github.com/aloethere/EP1001/blob/gh-pages/images/2dcnc/finishedcut.png?raw=true" width = "350">
<img src="https://github.com/aloethere/EP1001/blob/gh-pages/images/2dcnc/lookinggoodcutted.png?raw=true" width = "285">
<br><img src="https://github.com/aloethere/EP1001/blob/gh-pages/images/2dcnc/clamp%20not%20clamping.png?raw=true" width = "200"><img src="https://github.com/aloethere/EP1001/blob/gh-pages/images/2dcnc/z%20problem.png?raw=true" width = "350">


