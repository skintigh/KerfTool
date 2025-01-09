# KerfTool
## Kerf Tool
Tool to measure the kerf of a laser cutter to an accuracy of 0.0005 mm, or 500 nm* -- the wavelegth of bluish-green light. It's also accurate to more practical measurements.

"Kerf" is the width of a cut, typically the width of the saw blade, or in this case the width of the laser beam**. But for a laser cutter you care about the **half-kerf**, see below.

Knowing the kerf of the cut (which changes with every laser cutter, with every material, with every color of every material, and even with different batches of that color of material, and I suspect can also vary with the power setting used and maybe the cut speed) allows you to make more accurate cuts.

## Some Examples
Let's say you cut this tool out of black acrylic. Then cut another copy of this tool out of white acrylic. Follow the instructions on each tool, write down the measurement, then do it a few more times and take an average of your readings for each color just in case.

Let's say you measured 0.18 mm for black and 0.15 mm for white. 

This is where it can get complicated. That measurement is the whole kerf of the entire laser beam, but you will almost never care about that... Maybe some software tools want you to enter the entire kerf, but for others (like Inkscape) you only want 1/2 of the Kerf since you will only be using **one side** of the laser beam to cut along the edge of something, or put another way: the circle of the beam will be centered on the line you are cutting with half on one side and half on the other. Therefore you want 1/2 of that measurement, 1/2 kerf, which would be: 

0.09mm kerf for black acrylic, 0.075mm for white acrylic.

Note: a lot of online help/blogs/videos will refer to the half kerf as the "kerf," because they are artists I guess ;)

## Use of Measurement
Enter the approriate setting as the kerf in your laser cutter software for the material you want to cut.

Or in Inkscape: set a "path effect" to **add 1/2 kerf to the outside** perimiter of objects and to **subtract 1/2 kerf from the inside** perimeter of holes you are cutting out. This means if you cut a donut shape, the outside of the donut is **larger** (to make up for material that will be burned away) and the donut hole is **smaller** (to account for the laser cutting away more than just the exact line). When you cut it, the laser will remove a little more material and shrink the donut and enlarge the hole back to the original lines.

Cut your kerf-adjusted part, then measure it with calipers to verify the kerf setting was correct.

## Acknowledgements
I started this tool by mimicking an existing tool that... I will name and link once I find it in my notes... sorry.



\* Achieving this level of accruacy will require a near-perfectly accurate tool to cut the Kerf Tool out of near-perfect material, preferably frictionless material, and operate the Kerf Tool in a near-perfectly clean environment on perfectly clean and symmetrical target, while wearing perfectly insulating gloves to prevent thermal expansion. Or regular tools and materials and conditions to make a practical tool.

\** NOTE: unlike a saw, which essentially removes a vertical column of material, a laser removes a truncated conical section, as if the sawblade were tilted at an angle and then wrapped around a single point. For most cases, this is negligible and the kerf will basically act as a vertical cut -- if you're building a jewelry box, nobody sane will care about 0.1 mm of kerf at all, never mind a fraction more of that in a slightly-slanted cut from the conical kerf. However, if you are cutting very fine details, say < 1 mm teeth on a gear, here kerf is critical for whether those gears mesh or jam or slip **and** the orientation of the cuts now matter. See my masterful diagram of a gear:

\\|||||||/

Those gears will mesh **very differently** if they are both right-side-up with the points meshing

\gear1/\gear2/

vs flipping one upside down so the slanted cuts complement each other:

\gear1//gear2\

