# CNC milling machine

Backlash measured on [2023-10-13](20231013.md) as follows:

* X axis: **0.11mm**
* Y axis: **0.11mm**
* Z axis: **0.13mm**

The cause of the backlash is not yet known, I suspect the ballscrews/ballnuts.

I subsequently applied 0.10mm backlash compensation to each axis, but this may come back to bite me.

On [2023-11-17](20231117.md) I noticed that code from `mk-pivot` was acting like it
wasn't moving the Z axis at all. I measured backlash at 0.65mm! I applied backlash compensation
of 0.65mm, ran the code again, and then it acted like it was over-compensating, I measured it
again and got 0.35mm. I think the problem is that the tighter the gibs get, the less ability
gravity has to do backlash compensation for me. You can imagine that if they were totally loose,
you wouldn't need any backlash compensation because gravity would always hold it against the same side
of the ballnut.
