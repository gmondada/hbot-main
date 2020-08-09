# HBOT - Main Project

HBOT is a humanoid robot driven by RC servos.

Its design is derived from [Robonoid](https://www.youmagine.com/designs/humanoid-robot-robonoid-design-concept), which is derived from [Plen2](https://github.com/plenprojectcompany/PLEN2).

This design makes use of ES08MA II servos controlled by a custom STM32F4/ESP8266 based electronics.

![overview](https://raw.githubusercontent.com/gmondada/hbot-main/master/images/hbot-one-leg.jpg)

# Parts

## 3D Printed Parts

* [Head](face.stl)
* [Body](robonoid/bought-parts/Robonoid_BodyHudi.stl)
* [Back (PCB Holder)](pcb-holder.stl)
* [Shoulder](robonoid/bought-parts/project-humanoid-robot-robonoid-shoulder-by-zalophus-dokdo/Robonoid_ShoulderPitch_Left.stl)
* [Shoulder](robonoid/bought-parts/project-humanoid-robot-robonoid-shoulder-by-zalophus-dokdo/Robonoid_ShoulderPitch_Right.stl)
* [Arm](robonoid/bought-parts/project-humanoid-robot-robonoid-elbow-shoulder-by-zalophus-dokdo/Robonoid_ElbowShoulderRoll_Left.stl)
* [Arm](robonoid/bought-parts/project-humanoid-robot-robonoid-elbow-shoulder-by-zalophus-dokdo/Robonoid_ElbowShoulderRoll_Right.stl)
* [Hand](robonoid/bought-parts/project-humanoid-robot-robonoid-hands-by-zalophus-dokdo/Robonoid_Hand_Left.stl)
* [Hand](robonoid/bought-parts/project-humanoid-robot-robonoid-hands-by-zalophus-dokdo/Robonoid_Hand_Right.stl)
* [Hip](robonoid/bought-parts/project-humanoid-robot-robonoid-shoulder-by-zalophus-dokdo/Robonoid_HandWristShoulderPitchThighYawFoot_Left.stl)
* [Hip](robonoid/bought-parts/project-humanoid-robot-robonoid-shoulder-by-zalophus-dokdo/Robonoid_HandWristShoulderPitchThighYawFoot_Right.stl)
* [Hip to Thigh Junction](robonoid/bought-parts/project-humanoid-robot-robonoid-foot-thigh-by-zalophus-dokdo/Robonoid_FootRollPitchThighPitchRoll_Left.stl)
* [Hip to Thigh Junction](robonoid/bought-parts/project-humanoid-robot-robonoid-foot-thigh-by-zalophus-dokdo/Robonoid_FootRollPitchThighPitchRoll_Right.stl)
* [Thigh + Knee](robonoid/bought-parts/project-humanoid-robot-robonoid-knee-pitch-by-zalophus-dokdo/Robonoid_KneePitch_Left.stl)
* [Thigh + Knee](robonoid/bought-parts/project-humanoid-robot-robonoid-knee-pitch-by-zalophus-dokdo/Robonoid_KneePitch_Right.stl)
* [Leg](robonoid/bought-parts/project-humanoid-robot-robonoid-knee-by-zalophus-dokdo/Robonoid_Knee_Left.stl)
* [Leg](robonoid/bought-parts/project-humanoid-robot-robonoid-knee-by-zalophus-dokdo/Robonoid_Knee_Right.stl)
* [Ankle](robonoid/bought-parts/project-humanoid-robot-robonoid-foot-thigh-by-zalophus-dokdo/Robonoid_FootRollPitchThighPitchRoll_Left.stl)
* [Ankle](robonoid/bought-parts/project-humanoid-robot-robonoid-foot-thigh-by-zalophus-dokdo/Robonoid_FootRollPitchThighPitchRoll_Right.stl)
* [Left Food](robonoid/bought-parts/project-humanoid-robot-robonoid-foots-by-zalophus-dokdo/Robonoid_Foot_Left.stl)
* [Right Food](robonoid/bought-parts/project-humanoid-robot-robonoid-foots-by-zalophus-dokdo/Robonoid_Foot_Right.stl)

## Electronics

* [Schematics](https://github.com/gmondada/hbot-pcb/blob/master/doc/schematics.pdf)
* [PCB](https://github.com/gmondada/hbot-pcb)

## Misc

* [ES08MA II Servos](https://www.aliexpress.com/item/32676616118.html?spm=2114.12010615.8148356.1.693451a3jKN2M7)
* [Screws for rotating junctions](https://www.aliexpress.com/item/32980090161.html?spm=2114.search0104.3.2.71e0331fj3GsxM)
* [Screws for PCB mounting](https://www.aliexpress.com/item/32909008538.html?spm=a2g0s.9042311.0.0.27424c4dg2vKQ5)
* [Screws M2 x 20mm](https://www.aliexpress.com/item/32825288439.html?spm=a2g0s.9042311.0.0.27424c4dg2vKQ5)

# Warning

This design has several problems:
1. Servos are not powerful enough. Raising a leg is super difficult. We should use servos with a higher reduction ratio.
2. Servos are not protected. If you stop the robot in a position where a servo has to provide some significant tork, the servo will heat and burn. This happens very easily, when the robot falls down, for instance, and makes the design absoutely not safe to play with.
3. Servos position control loop is not suitable for loads with significant inertia and low friction. I had to artificially increase friction in order to avoid oscillations.

This project in not maintained anymore.

# License

Copyright (c) 2019 Gabriele Mondada.
Licensed under the [Creative Commons CC-BY 4.0 License](https://creativecommons.org/licenses/by/4.0/legalcode).

This work is derived from Robonoid by Zalophus Dokdo, of which concept is distributed under Creative Commons Attribution Share Alike.

The STL file of each Robonoid's part is available for download on pinshape.com. These files are licensed under CC - Attribution - Non-Commercial - No Derivatives. Download is not free, each single part must be purchased.

I wrote to the copyright owner to clarify why single parts have a different license that the main concept and what do it mean to prevent derivative work on single parts when this restriction does not apply on the whole concept. I never got any answer.

It seems clear that these parts can be purchased, downloaded, printed and used in an assembly. They can also be shared under CC - Attribution - Non-Commercial - No Derivatives. They cannot be modified to generate derivative parts but can be redesigned as a derivative work of the main concept.

These parts are available in this repo but if you want to support the Robonoid project, please consider purchasing them on pinshape.com.
