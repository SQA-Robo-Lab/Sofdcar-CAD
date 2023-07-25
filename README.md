# Sofdcar CAD Repository
Contains all relevant CAD files that were created in the context of or as need for the sofdcar project

## Folders
### LinesPrintTemplate
Svg templates for printing different types of lines fo the car to follow.
Are compatible with each other to allow for any track layout desired

Manufacturing: Print
- Use specified paper size (A4 if not specified)

### PiCarX
All Cad files for modifying the PiCarX to work with our hardware stack.
I.e. allow for the bigger battery, the Arduinos (Nano and Uno/Mega) and the ESP to be placed atop

#### HBridgeMount
Mount for the H-Bridge motor driver board to be mounted underneath the base of the PiCarX.
Allows the motor to svivel to access the connections.

Manufacturing: 3D-Print
- Print "Top" Part of sviveling pillar
- Then print "Bottom" part, pause the print before the axle is expanding and insert the "Top" part to interlock them

#### NewMegaBox
"Rack" box for mounting the battery, Arduino Nano, ESP and Arduino MEGA to the PiCarX.
Original drawing in `NewCarBox.FCStd`, cross-sections of parts to cut in seperate svg files
(New variant of steered car)

Manufacturing: Lasercut + Glue
- Use 3mm Material
- `AssembledLaserFile.svg` already contains all parts closely packed, ready to cut
- Glue all parts into a box except the "CoverPlateAkku" and the "TopPlate" to access the battery and Arduino Nano on the lower levels
- Slide in the "CoverPlateAkku" from the back

#### OldUnoBox
Box to house the battery and a breadoard with Arduino Nano, ESP and motor driver as well as the Arduino UNO on top.
(Old variant of steered car)

Manufacturing: Lasercut + Glue
- Use 3mm Material
- Cut 2 copies of the Top/Bottom Plate (top middle)
- Cut 2 copies of the front/back part (bottom left)
- Cut 4 copies of the side part (bottom right)
- Glue all parts together into a box except the top plate to access the battery

## File Types
### pdf (gitignored by default)
- Most common type: 2D Export of some other drawing
- Software: Any PDF viewer

### svg
- Most common type: 2D Vectorgraphics, drawn or exported
- Software: [Inkscape](https://inkscape.org/)

### FCStd
- Most common type: (Parametric) 3D CAD drawing
- Software: [FreeCAD](https://www.freecad.org/)

### stl (gitignored by default)
- Most common type: Export of a 3D object from a CAD drawing
- Software (edit): [FreeCAD](https://www.freecad.org/) or [Blender](https://www.blender.org/)
- Software (3d-print): Any slicer (e.g. [PrusaSlicer](https://github.com/prusa3d/PrusaSlicer))