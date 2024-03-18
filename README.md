# KerfTool
## Kerf Tool
Tool to measure the kerf of a laser cutter to an accuracy of 0.00005 mm, or 50 nm -- the wavelegth of microwave radiation. It's also accurate to more practical measurements.
"Kerf" is the width of a cut, typically the width of the saw blade, or in this case the width of the laser beam**.
Knowing the kerf of the cut (which changes with ever lawer cutter, with every material, and every color of every material) allows you to make more accurate cuts.

## Example Measurement
Cut this tool out of black acrylic. Cut another copy of this tool out of white acrylic. Follow the instructions on each tool, write down the measurement, then do it a few more times and take an average just in case.
Say you measured 0.18 mm for black and 0.15 mm for white. 

This is where it can get complicated. That measurement is the kerf of the entire laser beam, but you will almost never care about that... Maybe some tools want you to enter the entire kerf, but for others (like Inkscape) you only want 1/2 of the Kerf since you will only be using one side of the laser beam to cut something. Therefore you want 1/2 of that measurement, 1/2 kerf, which would be: 0.09mm kerf for black acrylic, 0.075mm for white acrylic.

Note: a lot of online help will refer to the half kerf as the "kerf," because they are artists I guess.

## Use of Measurement
Enter the approriate setting as the kerf in your laser cutter software for the material you want to cut
Or in Inkscape: set a "path effect" to **add** 1/2 kerf from the outside perimiter of objects and to **subtract** 1/2 kerf to the inside perimeter of holes you are cutting out. This means if you cut a donut shape, the outside of the donut is **larger** and te donut hole is **smaller**. When you cut it, the laser will remove a little more material and shrink the donut and enlarge the hole.
Cut it, then measure it with calipers to verify the kerf setting was correct.

\* Achieving this level of accruacy will reaquire a near-perfectly accurate tool to cut the Kerf Tool out of near-perfect material, preferably frictionless material, and operate the Kerf Tool in a near-perfectly clean environment on perfectly clean and symmetrical target, while wearing perfectly insulating gloves to prevent thermal expansion.

\** NOTE: unlike a saw, which essentially removes a vertical column of material, a laser removes a truncated conical section, as if the sawblade were tilted at an angle and then wrapped around a single point. For most cases, this is negligible and the kerf will basically act as a vertical cut. However, if you are cutting very fine details, say < 1mm teeth on a gear, those gear will mesh very differently if they are both right-side-up vs flipping one upsaide down.
