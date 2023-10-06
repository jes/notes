# Micro-machining

## 1mm 2-flute end mill in aluminium

* Width of cut: **1 mm** (full slotting)
* Depth of cut: **0.3 mm**
* Horizontal feed: **100 mm/min**
* Vertical feed: **50 mm/min**
* Spindle speed: **24000 rpm**

On [2023-09-14](20230914.md) I machined a 2mm thick aluminium escape wheel.

https://img.incoherency.co.uk/4625

This is what I learnt.

The feed rate computed by the calculator is too high, try the following:

**Make sure you measure the runout before starting, and attempt to minimise it.**

**Consider using the 5mm collet even though the shank is 4mm.**

**Consider using copious amounts of a spray solvent for coolant/lubrication/chip evacuation.**

**The tips of the teeth on the escape wheel are very sharp, fragile, consider adding a radius.**

**Consider measuring the runout and then telling FreeCAD that the tool is oversize (0.1mm TIR => 1.05mm diameter).**

The first endmill snapped immediately. For the second one I measured the runout at over 0.2mm! (Over 20%
of diameter!)

I couldn't improve it much using the 4mm collet. I tried to shim the tool with some paper but couldn't
get it in there.
I tried clamping down with the 5mm collet and measured about 0.1mm runout.
Tapping the endmill with a drift didn't seem to help, so I just ran it with the 0.1mm runout and it worked!

I used quite a lot of the "engine cleaner & degreaser" to make sure the path was clear of chips before the start
of each "lap".

The dimensions came out to within about 0.1mm, which is as good as we can expect with 0.1mm runout.
The bore is a bit under 2.1 mm (nominally 2.0). The slot width is about 1.1mm (nominally 1.0).

The outer diameter across tooth tips is 26.1mm (nominally 26.4mm, but they are very thin and fragile).

It took about half an hour.

On [2023-10-06](20231006.md) I made this escape wheel:

https://img.incoherency.co.uk/4784

I broke the first tool, possibly because I forgot to check the runout. I was using the 4mm collet because
I forgot that I should maybe not. I reduced the feed rate to **40 mm/min** for the second attempt, and it worked
without drama. I wish I had measured the runout though.

## 2mm 1-flute end mill in aluminium/brass

* Width of cut: **2 mm** (full slotting)
* Depth of cut: try **0.5 mm** (was 0.32mm before)
* Horizontal feed: **400 mm/min**
* Vertical feed: **200 mm/min**
* Spindle speed: **24000 rpm**

On [2023-09-15](20230915.md) I made a 3mm thick balance wheel.

https://img.incoherency.co.uk/4626

I did not bother measuring the run-out before starting and it was fine. I drilled the holes with drills instead of the end mill.
It went *much* faster than the 1mm end mill did, and seemed less likely to break. I ran out of engine degreaser so at the
end the chip evacuation was very poor, and there is a very slightly worse surface finish on the bottom of the outside profile.
So spraying the degreaser is definitely helpful.

Watch out for the lead-out gouging the work next time...

On [2023-09-17](20230917.md) I made 2x 2mm thick frame plates.

https://img.incoherency.co.uk/4634

On [2023-09-30](20230930.md) I made a 1mm thick brass scale for the Douzieme gauge.

https://img.incoherency.co.uk/4727

I used WD-40 as a lubricant, but the brass chips seemed to fly away from the work much more readily than the aluminium ones,
so it wasn't nearly as necessary.

On [2023-10-01](20231001.md) I made a tiny brass clamp for the Douzieme gauge:

https://img.incoherency.co.uk/4729

I first drilled the holes with the 1.2mm PCB drill (later opened up to 1.7mm with the little 14v cordless drill).
Then I carefully made the countersinks by plunging the 90-degree 6mm V-bit tool. This tool was chattering quite a lot,
so I went very slowly.

Then I did the profile cut, at 60% feed rate, it took less than a minute.

On [2023-10-05](20231005.md) I made these frame plates for the metal escapement model:

https://img.incoherency.co.uk/4772

First drilled the 4 holes in the middle with the 0.5mm PCB drill (later opened up by hand with the pin vice).
I fed in **0.1 mm** increments, at **30 mm/min** to drill the 0.5mm holes and it worked without any drama.
I sprayed WD-40 on the surface before starting. Even though I used a 0.5mm PCB drill, the holes needed to be opened
up to 0.5mm with a piece of sharpened 0.5mm blue pivot steel.

On [2023-10-06](20231006.md) I made this escape wheel:

https://img.incoherency.co.uk/4784

Roughed with the 2mm end mill, at **14000 rpm** and **40 mm/min**.

## 0.6mm fibreglass-cutting tool

* Width of cut: **0.1 mm**
* Depth of cut: **0.1 mm**
* Horizontal feed: **40 mm/min**
* Vertical feed: **20 mm/min**
* Spindle speed: **24000 rpm**

On [2023-10-06](20231006.md) I made this escape wheel:

https://img.incoherency.co.uk/4784

Most of the cutting was down with the 1mm and 2mm tools, as detailed above, but finishing the roots of the
teeth was done with the 0.6mm tool. It worked without drama, but I had my coordinate system misaligned so
only some of the teeth were cut correctly.
