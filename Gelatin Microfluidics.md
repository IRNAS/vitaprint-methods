# Gelatin Microfluidics
## Introduction

Due to the required high proximity of cells to blood vessels the fabrication of vascular structures has enormous impact on the engineering of tissues and organs. However, the required resolution and structural integrity is yet to be reached, thus, the fabrication of thick vascular tissues is still the main challenge to solve in tissue engineering.
This protocol is a modification of the freeform reversible embedding of suspended hydrogels (FRESH) method for the fabrication of freeform perfusable microfluidics inside a gelatine matrix, which can be used in the construction of vascular grafts, for the purposes of tissue and organ engineering.
The FRESH method for the preparation of the gelatine matrix, which allows precise deposition of material inside a gelatin matrix, and consequently the fabrication of almost any shape or form, has been adapted after Hinton et al. 2015. The method was already shown to produce vascular tissues, our adaptation however, gives higher control over the resolution of the matrix and consequently allows for the fabrication of thinner vessels (internal diameter as low as 210μm).

## Table of Contents
- [Workflow](#WORK)
- [Equipment and Tools](#EQUIP)
- [Chemicals](#CHEM)
- [Procedure](#PROCEDURE)
- [Notes and Tips](#TIPS)
- [References](#REF)


## Workflow <a id="WORK"></a>
<img src="https://user-images.githubusercontent.com/14543226/28706272-d824b230-7373-11e7-9c01-42fccb26888b.png" alt="table" width="150" height="450">

## Equipment and Tools <a id="EQUIP"></a>
- Laser cutter (4mm plexi glass)
- CNC mill (1mm drill, chamfering drill)
- waterproof tape + scissors
- Vitaprint extruder mounted on a CNC system
- 5mL Syringes
- gauge needles (G21 or G27)
- magnetic stirrer + magnet
- pipette
- fridge
- heat block or chamber
- beakers
- paper towels
- pen ink


## Chemicals <a id="CHEM"></a>
- gelatine from porcine skin (Sigma-Aldrich)
- xanthan (Herbana)
- CaCl2 (Sigma-Aldrich)
- pen ink (Pelikan 4001)
- distilled water

## Procedure <a id="PROCEDURE"></a>

### Step 1: Mould Building

1. Laser cut the mould out of plexiglass/acrylic plastic (file filename).
2. Drill the inlet and outlet holes using a CNC mill (file filename).
3. Seal the bottom with waterproof tape

<img src="https://user-images.githubusercontent.com/14543226/28706742-cf21a678-7375-11e7-9848-f72e33ddacc5.jpg" alt="table" width="400" height="300">
Picture 1: Finished mould, sealed with waterproof tape


### Step 2: Filament Preparation
1. Prepare a 0.5% w/w xanthan solution by adding xanthan to distilled water in a beaker. 
2. Stir with magnetic stirrer for at least 6h. Make sure all bubbles are removed and the xanthan solution is fully homogenized. This ensures a consistent print.
4. Add ink (3 drops / 20 mL) and homogenize with magnetic stirrer. This helps with channel perfusability.
5. The solution can be stored for ~ 2 weeks at 6°C.

### Step 3: Matrix Formation (adapted from Hinton et al., 2015)
1. Grind up gelatine in a coffee grinder for 5-10 min and sieve it through a < 140 µ mesh. Mesh sizes can be adjusted according to the needed smoothness of the matrix.
2. In a beaker, prepare a 5% gelatine solution in 50 mM CaCl2. Add the gelatine slowly to prevent lump formation (lumps can cause inconsistencies in the print). The 50 mM CaCl2 solution needs to be prepared with distilled water and freshly every day.
3. Mix the gelatine solution on the magnetic stirrer for ~15 min, until the gelatine has soaked and all the lumps have dissolved.
4. Wait until the undissolved gelatine has set (picture 2), remove the supernatant and add the same amount of fresh 50 mM CaCl2 solution.

<img src="https://user-images.githubusercontent.com/14543226/28706841-447cb368-7376-11e7-8706-8f426c26a426.png" alt="table" width="400" height="400">
Picture 2: Layer of set gelatine.

5. Mix the gelatine solution on the magnetic stirrer for 2 min, then repeat the procedure under 4.) 1-2 more times (the supernatant has to be clear, not yellowish).
6. Remove excess liquid from the gelatine with a paper towel. An optimal gelatine slurry consistency is such, that upon tilting the beaker, the gelatine slurry moves very slowly, but does not stay still. 50 mM CaCl2 can be added, if too much liquid was removed previously.
7. Use a needle to fill the inlet and the outlet of the mould with the xanthan solution and pour the gelatine slurry into the mould.

### Step 4: Printing the Filament
1. Fill the syringe with 0.5% xanthan, making sure there are no air bubbles. Screw on the needle (we used G21 or G27 needles with 0.51 mm and 0.21 mm inner diameters, respectively) .
2. Mount the syringe onto the extruder.
3. Position the mould on the printer, so that X0 Y0 Z0 is in the lower left corner of the top face.

<img src="https://user-images.githubusercontent.com/14543226/28706918-8efe77aa-7376-11e7-9654-e5d538319f21.png" alt="table" width="400" height="250">
Picture 3: Mould scheme, indicating print starting point, thickness and inlet/outlet diameter

4. Start the print.

### Step 5: Post-Print Procedure
1. Right after the print, wait a few minutes for the xanthan to fully crosslink (darker edges and a lighter inside can be seen - picture 4).

<img src="https://user-images.githubusercontent.com/14543226/28706993-e0d0ea22-7376-11e7-903f-555d6acc9a44.png" alt="table" width="400" height="400">
Picture 4: Before (LEFT) and after (RIGHT) xanthan crosslinking.

2. For the crosslinking of gelatine, heat the print for ~ 5 min to 30°C and then to 42°C, until all the gelatine has completely melted.
3. Cool the print at room temperature (maximum 24°C - it will not solidify enough otherwise), for a minimum of 0.5 h (if the gelatine cools too fast, there is not enough time for it to gel). Once cooled enough for the filament to be stable, cool in the fridge (~6°C) until the gelation fully solidifies.
4. To start perfusion through the printed channel, firstly gently clean the channels in the mould with a needle (G21 - G27), then slowly inject a small amount of pure ink on one side and keep injecting if the ink flows through the channels. Otherwise, gently push the syringe piston up and down (like "simulating a heart"), watching that the channel does not burst.

VIDEO

## Notes and Tips <a id="TIPS"></a>
You can use this method to fabricate perfusable channels in any mould. Moulds can be designed and manufactured in different ways (such as 3D printed, CNC-milled etc.). Make sure your xanthan trace starts at the inlet and ends at an outlet. 

- sharp edges in the channel trajectory disrupt the ink flow
- ...

## References <a id="REF"></a>
1. Hinton, T., Jallerat, Q., Palchesko, R., Park, J., Grodzicki, M., Shue, H., Ramadan, M., Hudson, A. and Feinberg, A. (2015). Three-dimensional printing of complex biological structures by freeform reversible embedding of suspended hydrogels. Science Advances, 1(9), pp.e1500758-e1500758

