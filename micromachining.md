# Micro-machining

## 1mm 2-flute end mill in aluminium

On [2023-09-14](20230914.md) I machined a 2mm thick aluminium escape wheel using a 1mm end mill.

https://img.incoherency.co.uk/4625

This is what I learnt.

The feed rate computed by the calculator is too high, try the following:

Width of cut: **1 mm** (full slotting)

Depth of cut: **0.3 mm**

Horizontal feed: **100 mm/min**

Vertical feed: **50 mm/min**

Spindle speed: **24000 rpm**

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

## 2mm 1-flute end mill in aluminium

On [2023-09-15](20230915.md) I made a 3mm thick balance wheel using the 2mm end mill.

https://img.incoherency.co.uk/4626

Watch out for the lead-out gouging the work next time...

Width of cut: **2 mm** (full slotting)

Depth of cut: **0.32 mm**

Horizontal feed: **330 mm/min**

Vertical feed: **330 mm/min**

Spindle speed: **24000 rpm**

I did not bother measuring the run-out before starting and it was fine. I drilled the holes with drills instead of the end mill.
It went *much* faster than the 1mm end mill did, and seemed less likely to break. I ran out of engine degreaser so at the
end the chip evacuation was very poor, and there is a very slightly worse surface finish on the bottom of the outside profile.
So spraying the degreaser is definitely helpful.
