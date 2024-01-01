# cable-organizer

Improved remix of the "Cable Organizer" by Papos98 on Thingiverse.

License [CC BY-NC-SA](https://creativecommons.org/licenses/by-nc-sa/4.0/)

## Changes and Features

- changed hinge joint tolerance to 0.4 mm, allows the arm snap to close more tightly

- basic organizer, with the clip mounting hole changed to suit a #6 flat-head wood screw

- Uplift Desk mountable version, supports an M8 mounting hole, placed off-center to allow clearance between the hinge and desktop

- blank template version of the basic clip exported as a STEP file to promote geometric editing in CAD tools

## FreeCAD Model

The FreeCAD model is available so that you can make changes to the base model if desired.  Please note that minimal experience with FreeCAD will be required to make changes.  You can find excellent basic FreeCAD tutorials on YouTube (look up MangoJelly for a comprehensive and enjoyable set).

### Model Parameters

To change model dimensions see the "master-dimensions" spreadsheet located inside the CAD model.  You can freely change:
  - the cable opening (default is 20mm) and
  - the hinge tolerance (default is 0.4mm) to suit your preferences or print accuracy

### Wood Screw Mount

For the wood screw-mounted version of the clip body ("clip-body-wood-screw"), you can locate the hole feature, open it in FreeCAD, and change it to some other other screw size, if desired.

### Hinge Body Chamfer

The chamfer on the main body, around the hinge joint, is important to prevent the hinge joint from fusing to the hinge body during printing, especially at sub-millimeter tolerances.  If you change model parameter dimensions above, make sure that you can still see the chamfer, and if it is missing, you may need to re-select the chamfer edges in the "main-body" part.

This is related to the topological naming problem in current versions of FreeCAD, which causes edges to be renamed after a geometric change to a body.  In this case, the chamfer feature is assigned to specifically-named edges.  If the names of those edges change as a result of recalculated geometry, the chamfer will become invalid.  There is ongoing work in FreeCAD to alleviate this issue, so it may become a non-issue in future versions of the tool.

### Exporting

The model is built in two parts, the "snap-arm" and one of the specialized main-body parts (clip-body-wood-screw, or lip-body-uplift-m8).  The "snap-arm" body is generic, and should be suitable for any of the specialized clip types.  Specialized versions of the clip body change the location and size of the mounting hole.  Current mody specializations include:
- "clip-body-wood-screw": sized for a #6 wood screw in a counter-bore hole, located in the body center
- "clip-body-uplift-m8": sized for an M8 machine screw, with the hole located off-center, 20mm from the clip hing-side, to allow clearance between the desktop and the clip hinge.

To export the clip, select the "snap-arm" body, and either the "clip-body-uplift-m8" or the "clip-body-wood-screw" body, and export.  It's important that both bodies are selected, since the snap arm is printed "inside" the specialized main-body model.
