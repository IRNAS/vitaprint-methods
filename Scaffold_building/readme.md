# Scaffold building
## Introduction

The basic structures, often found in 3D bioprinting literature are so called "woodpile" structures or scaffolds. Basically, this is a 3D grid, which allows the cultivation of cells in the vertical direction and simultaneously sufficient perfusion with nutrient medium. Thus they are very useful for testing the cultivability of various cell types, however, due to their simple geometry, they are not suitable for very complex tissue structures, as these require more sophisticated design. The scaffolds are printed from various materials which are developed by the researchers themselves. However, as the geometry typically remains the same, it is also useful for evaluating material behaviour during and post printing, under cell-culture conditions, etc.

We have prepared a simple python-based algorithm to simplify the generation of g-code of woodpile scaffolds, which you will also find in the repository.

## Table of Contents
- [Workflow](#WORK)
- [General materials and tools](#MAT)
- [Gelatin-alginate](#GELALG)
  * [Specific materials](#mat1)
  * [Preparation of the composite](#prep1)
  * [Print settings and conditions](#print1)
  * [Important guidelines](#guide1)
  * [Post-processing](#post1)
- [Gluten](#GLUTEN)
  * [Specific materials](#mat2)
  * [Preparation of the material](#prep2)
  * [Print settings and conditions](#print2)
  * [Post-processing](#post2)

## Workflow <a id="WORK"></a>
![scaffold_fabrication](https://user-images.githubusercontent.com/17159617/28751961-8f8d0494-7514-11e7-8fc4-a5a56167933f.png)

## General materials and tools <a id="MAT"></a>
- distilled water
- glass beakers
- magnetic stirrer + rods
- microwave oven
- 5ml syringes
- blunt-end gauge needles (G21 or G27)
- Vitaprint extruder mounted on a CNC system

Printing materials
Here we describe the preparation of two scaffold materials:
- A gelatin-alginate composite for tissue engineering
- Gluten - a highly viscous material and a very affordable adhesive component

## Gelatin-alginate <a id="GELALG"></a>
Gelatin is a the thermal degradation product of collagen and is typically obtained by cooking animal connective tissues, of which collagen is the main component. Due to its origin, gelatin can mimick the composition of the average extracellular matrix well. It exhibits thermal gelation, thus a hydrogel made from gelatin can be used for manufacturing by heating (melting) and cooling (gelation). This is very handy for printing, however, the material itself is not stable at cell culture conditions (37°C) and will require post-processing by additional cross-linking when used for this purpose. This can be achieved by different approaches, either by using gultaraldehyde (very toxic, requires rigorous rinsing), transglutaminases, N-(3-dimethylaminopropyl)-N′-ethylcarbodiimide, etc.

Alginate is a polysaccharide found in brown algae and exhibits ionic cross-linking by interacting with calcium ions while in solution. When blended together with gelatin it gives mechanical stability to the structure when cross-linked. The polymer chains are however loosened significantly when in a natrium ion rich medium, which is common for cell-culture media.

### Specific materials <a id="mat1"></a>
- Gelatin from porcine skin (Sigma-Aldrich)
- Sodium alginate (Sigma-Aldrich)
- Calcium Chloride (Sigma-Aldrich)

### Preparation of the composite <a id="prep1"></a>
The printing material is composed of a 10% gelatin (w/w) and 1% alginate (w/w) in water and is prepared in the following manner for 20ml of printing material:

1. 18.8 ml of water are transferred to a beaker and rigorously mixed on a magnetic stirrer.
2. Very slowly and carefully, 0.2g of alginate are added to avoid the formation of lumps.
3. 2g of gelatin are added in the same manner and the mix is stirred for additional 5-10 min for the gelatin to soak in the solution.
4. The mixture is heated in a microwave and the heating is stopped immediately after the boiling point is reached.
5. The mixture is stirred for one more minute.
6. The beaker is placed in a vacuum desiccator to remove bubbles from the solution.
7. The solution is loaded into a 5ml syringe and mounted on the preheated extruder where it is let to reach printing temperature (at least 30min).

### Print settings and conditions <a id="print1"></a>
The settings for printing vary slightly, depending on the nozzle. Print settings for blunt-end G21 and G27 needles are shown in the table below and were determined experimentally at 20-22°C ambient temperature and for printed structures with a layer height equal to the nozzle diameter.

|     nozzle     | F [mm/min] | E [mm/10mm of path] | T [°C] |
|:--------------:|:----------:|:-------------------:|:------:|
| G21 (0.4mm ID) |   100-400  |         0.04        |  27-29 |
| G27 (0.2mm ID) |   100-400  |         0.01        |  28-29 |

Once the settings are adjusted, the g-code can be generated and run via CNC controller. We use PlanetCNC USB controller (https://planet-cnc.com/support/), as it allows extensive manual control. It is important to note that the user should be well versed in using his CNC system.

### Important guidelines <a id="guide1"></a>
- Before printing, decide on the surface/container where the print should take place (e.g. petri dish).
- After mounting the syringe and the nozzle, determine the (x,y,z) = (0,0,0) position. The z position is especially important and should lie approximately 1 layer height above the surface.
- Before running the g-code, enough material should be extruded from the syringe to reach the tip of the nozzle. This can be done manually, but we recomment it be pre-programmed in the g-code by adding skirts.

### Post-processing <a id="post1"></a>
After printing the scaffolds are transferred to a 10mM CaCl₂ solution to cross-link the alginate. In this manner they become stable during heating and when soaked into sterilization liquids (e.g. 70% alcohol).

![gelatin_algi](https://user-images.githubusercontent.com/17159617/28752369-5a1de374-751d-11e7-9e8f-f52496a5a8d3.jpg)
Figure 1: Simple gelatin-alginate woodpile scaffold, generated using the python g-code generator.

![gelalgi_nose](https://user-images.githubusercontent.com/17159617/28752372-5eb619d8-751d-11e7-98cb-d4af3b2cfd00.jpg)
Figure 2: Nose scaffold from the gelatin-alginate composite. G-code generated using attached Slic3r settings.


## Gluten <a id="GLUTEN"></a>
Gluten is a protein often found in cereal grains, especially wheat and is a common waste product in food production. Though there is more (food related) discussion about this material now, it has been known for centuries and was traditionally used as a glue. It is not only a good adhesive, but also its mechanical properties can be adjusted by modifying the polymer chains, making it either soft and elastic, or stiff as glass. Therefore it may become a very interesting component for digital manufacturing.

### Specific materials <a id="mat2"></a>
- gluten (Buxtrade GmbH)
- citric acid (optional, for modifying viscosity)

### Preparation of the material <a id="prep2"></a>
1. 5.5g of gluten granules are soaked in 4.5ml of water overnight (or for at least 6 hours).
2. The soaked material is heated to 60°C in a water bath and stirred until smooth.
3. The gluten solution is loaded into the syringe and mounted onto the extruder, which is preheated to 50°C and let to reach printing temperature (at least 30min).

### Print settings and conditions <a id="print2"></a>
Being extremely viscous and solidifying depending on temperature, clogging of the nozzle can happen very easily. Printing with a G21 (0.4mm ID) needle requires a rapid extrusion of 2.5mm with a feedrate of 100mm/min, immediately before printing. Our experimentally determined printing parameters were as follows:
E = 0.4mm/10mm of path
F = 400-600mm/min
h (layer height) = 0.3mm

In our experiments printing took place at 20-21°C ambient temperature. Printing guidelines should be followed as described above.

### Post-processing <a id="post2"></a>
Printed gluten scaffolds do not require extraordinary post-processing, as the structures become stable after drying. In this regard it is important to note, that a slow and even drying process is vital to prevent post-printing deformations of the structure. Woodpile scaffolds are easy to dry. They are placed into a petri dish with a few drops of water and loosely covered for at least two days.

![gluten](https://user-images.githubusercontent.com/17159617/28752373-620f7106-751d-11e7-8425-ce7338beaf13.jpg)
Figure 3: Simple woodpile scaffold from gluten.

## Samples
In the repository you will find g-code demo files, as well as Slic3r setting files for the gelatin-alginate nose scaffold.
