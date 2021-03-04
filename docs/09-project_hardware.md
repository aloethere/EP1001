---
layout: default
title: Hardware
nav_order: 11
parent: Project
---

# The Hardware
---

## Tank tracks

My first step was to design the tracks for WALL-E. Since WALL-E has a triangular shaped tracks, I attempted to position the 3 lego wheels together and fit the rubber treads for the left and right side. From there, I estimated a fixed position where the 3 wheels would be and laser cut acrylic to hold them together. The acrylic acts as a supporting frame for the positioned wheel rims. This step took a few tries to get my rubber track drive treads fit well together without it being too tight or too loose. 

<img src="https://github.com/aloethere/EP1001/blob/gh-pages/images/project/treads2.png?raw=true" width = "250">
<img src="https://github.com/aloethere/EP1001/blob/gh-pages/images/project/treads.jpg?raw=true" width = "250">
<br><sub><em>Animated WALL-E has a treads with changeable shapes using tensioner and lift system</em></sub>

<img src="https://github.com/aloethere/EP1001/blob/gh-pages/images/project/wheel-%20acrylic.png?raw=true" width = "250">

[tracks_frame.dxf](https://github.com/aloethere/EP1001/blob/gh-pages/files/laser%20cut%20track%20supoort%20new%20v4.f3d?raw=true){: .btn }

While finalising my acrylic design, I also realised that it would be better if i trim the lego wheels to be narrower in width. This is so that the wheels in between looks flushed. So i sawed them on each sides. I use a total of 6 wheel rims. I also attached some washers so there could be less friction when the wheels are rotating.

<img src="https://github.com/aloethere/EP1001/blob/gh-pages/images/project/wheel%20trimmed.jpeg?raw=true" width = "250">
<br><sub><em>Trimmed lego wheels (only 1 side)</em></sub>

<img src="https://github.com/aloethere/EP1001/blob/gh-pages/images/project/wheel-washer2.jpeg?raw=true" width="250">
<img src="https://github.com/aloethere/EP1001/blob/gh-pages/images/project/wheel-washer1.jpeg?raw=true" width="250">
<br><sub><em>Super glued washer both sides</em></sub>

I later messed up some of the given wheels. So I 3d printed my own. The 3D printed wheels are flushed as well and feature a hexagon hole for *this thing* to act as my axle. I printed 2 pieces and both are placed for the top position of the triangle, which will then connect straight to my continuous servo.

<img src="https://github.com/aloethere/EP1001/blob/gh-pages/images/project/Female-Hex-Hexagonal.jpg?raw=true" width = "100">
<br><sub><em>*The thing*</em></sub>

<img src="https://github.com/aloethere/EP1001/blob/gh-pages/images/project/wheel-3d%20print.jpeg?raw=true" width = "250">
<img src="https://github.com/aloethere/EP1001/blob/gh-pages/images/project/wheel-3d%20print.png?raw=true" width="250">
<img src="https://github.com/aloethere/EP1001/blob/gh-pages/images/project/wheel%20and%20support.jpeg?raw=true" width="250">

[3dprint_wheelhex.stl](https://github.com/aloethere/EP1001/raw/gh-pages/files/3d%20print%20lego%20wheels%20hexegon%20v2.stl){: .btn }

## Body

The rest of WALL-E's body stucture are based on [chillibasket's WALL-E replica on thingiverse](https://www.thingiverse.com/thing:3703555). The dimension and designs are life-sized so I went to scale it down to 60% of it's original file. To do this, I downloaded the STEP files on thingiverse and modify accordingly on Fusion 360. Most of the modification is to delete unwanted features, re-size the screw holes and group parts in pne print.

**Bottom** 
<iframe src="https://ichat754.autodesk360.com/shares/public/SH56a43QTfd62c1cd9685532433c7c358afe?mode=embed" width="540" height="380" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>
[3dp_body-bottom.stl](){: .btn }

- Custom part to link bottom to tracks

**Front**
<iframe src="https://ichat754.autodesk360.com/shares/public/SH56a43QTfd62c1cd96811d2b3882f03bf3e?mode=embed" width="540" height="380" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>

[3dp_body-front.stl](https://github.com/aloethere/EP1001/raw/gh-pages/files/body-front.stl){: .btn }

- Resize the battery level detection area to put in led bar strip. (Not implemented at the end, used to arrange wires)

<iframe src="https://ichat754.autodesk360.com/shares/public/SH56a43QTfd62c1cd968cf32895136ca45ea?mode=embed" width="540" height="380" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>

[3dp_body-frontdoor.stl](https://github.com/aloethere/EP1001/raw/gh-pages/files/body-front-door%20.stl){: .btn }

- Nothing

**Back**
<iframe src="https://ichat754.autodesk360.com/shares/public/SH56a43QTfd62c1cd9685e1bd83f49a45bf1?mode=embed" width="540" height="380" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>

[3dp_body-back.stl](){: .btn }

- Cut out space to hold battery.
- Note: Still not enough space.

**Sides, right & left**
<iframe src="https://ichat754.autodesk360.com/shares/public/SH56a43QTfd62c1cd968df956dfd15fe8c56?mode=embed" width="540" height="380" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>

[3dp_body-right.stl](https://github.com/aloethere/EP1001/raw/gh-pages/files/body-right%20MGservo.stl){: .btn }

[3dp_body-left.stl](https://github.com/aloethere/EP1001/raw/gh-pages/files/body-left%20MGservo.stl){: .btn }

- I checked the alignment by importing other components. Made sure it all fits together and modified accordingly
- Includes servo bracket, arm hinge, motor, body-bottom, acrylic frame and linkage.
- Added holes for motor and screws.
- Reposition engraved area for force-fitted servo arm brackets

**Top**
<iframe src="https://ichat754.autodesk360.com/shares/public/SH56a43QTfd62c1cd968101d51db1d201d3e?mode=embed" width="640" height="480" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>

- Created an on/off switch area
- Should hv check the screw hole position that connects to arm bracket
- Redesigned to 3 button holes. Idea was to add in sounds when button pressed. Not implemented.
- In final design, I change a different on/off switch model. So I drilled a hole to fit that.

## Arms
<iframe src="https://ichat754.autodesk360.com/shares/public/SH56a43QTfd62c1cd96894478f97a80e5124?mode=embed" width="540" height="380" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>

[3dp_arm.stl](){: .btn }
<br>[3dp_fingers.stl](https://github.com/aloethere/EP1001/raw/gh-pages/files/hand-fingers%20.stl){: .btn }
<br>[3dp_arm-hingeinner.stl](https://github.com/aloethere/EP1001/raw/gh-pages/files/arm-hinge-inne.stl){: .btn }
<br>[3dp_arm-hingeouter.stl](https://github.com/aloethere/EP1001/raw/gh-pages/files/arm-hinge-outer.stl){: .btn }
<br>[3dp_arm-hingeaxle.stl](){: .btn }
<br>[3dp_hand-bracket.stl](https://github.com/aloethere/EP1001/raw/gh-pages/files/hand-bracket.stl){: .btn }
<br>[3dp_hand-axle.stl](){: .btn }


- Joined barrel and piston part. Added screw hole to minimise axle movement.
- Arm hinge outer extrude. longer.
- Arm hinge inner not scaled down to fit arm servo.
- Arm bracket for servo, not scaled down.

## Neck
<iframe src="https://ichat754.autodesk360.com/shares/public/SH56a43QTfd62c1cd968d0d8dbebc814d4d1?mode=embed" width="640" height="480" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>

[3dp_neck-top.stl](){: .btn }
<br>[3dp_neck-bottom.stl](){: .btn }
<br>[3dp_neck-bottomaaxle.stl](){: .btn }

- Not implementing motorised neck movement since when scaled down, servo does not fit.
- So, Joined the neck top parts together as one.
- Neck Bottom left and right are glued after inserting axle

## Eyes















