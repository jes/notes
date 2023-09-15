# Watchmaking

My techniques for making watch parts.

## Making gear cutters

https://img.incoherency.co.uk/4598

**TODO: try this with silver steel instead of HSS.**

Mount a tool blank in the vice in the milling machine, at a slight angle to provide some clearance (what angle? should I be more thorough about this?).

Model the profile you want to cut in FreeCAD, generate the path, and then edit the path to remove the moves you don't need.

Run the job.

I have done this already with a HSS blank and it worked OK but the machine was not happy cutting HSS. I think next time I should
use silver steel and harden it after cutting.

## Making gears

https://img.incoherency.co.uk/4615

[2023-09-08](20230908.md)

Put the brass rod stock in the collet chuck.

Face off the end.

Part off a disc of a bit more than the required thickness.

Put the superglue arbor in the collet chuck (use the M6 clamping collet in the back of the ER collet to space it out).

Face the end of the superglue arbor, maybe recut air grooves.

Superglue the faced side of the brass disc to the arbor, roughly central.

Turn the disc to final diameter and thickness.

Bore the hole in the disc.

Transfer the collet chuck to the milling machine.

Put the gear cutter in the milling machine.

See [4thaxis](4thaxis.md) for how to use `mk-gear` to cut the gear teeth, correcting for concentricity error.

## Making shafts

[2023-09-15](20230915.md)

**TODO: this process needs a step for hardening the shaft, and a step for polishing it.**

Put the silver steel rod stock in the collet chuck.

Use a right-hand turning tool, with a DCGT (ground) insert, with 0.2mm nose radius if possible.

Turn to the largest diameter.

Use the compound slide to turn a slight taper, if it helps, so that the gear can be hammered on to the required position.

Once the diameter for the gear seat is found, start turning the pivot at the exposed end.

Use the micrometer to measure the diameter, but don't squeeze too hard because it can damage the pivot.

Once the first pivot is in place, use the little ruler to find the required length of the shaft.
Without turning the material around, start turning down the other end pivot. You'll have to leave
a taper where the shoulder should be.

Once the pivot is turned down a bit, "part off" by making a deep-ish groove at the end of the work, and
then break off the shaft by hand.

Take the rod stock out of the chuck, and switch to a collet that suits the most convenient clamping
diameter of the shaft. Use a drill bit or similar if necessary to space out the back of the ER collet.

Now finish turning the other pivot.

If at any point the partially-made shaft bends because the metal is too soft and you took a too-greedy cut,
stop the lathe, manually tap it roughly true using the soft drift, and then start the lathe and push the soft
drift against the spinning part to true it up even more.

## Crossing out

https://img.incoherency.co.uk/4625

[2023-09-14](20230914.md)

## Fitting gears to shafts

https://img.incoherency.co.uk/4631

[2023-09-15](20230915.md)

**TODO: I probably want some improved staking tools.**

Put the gear on a flat surface with a hole in the middle.

Slide the shaft into the hole as far as it can go.

Hammer the shaft home.

If the pivot bent in this process, put the shaft (with gear) back in the lathe, and try to true it up using the
soft drift. This is less likely to happen if using hardened shafts and proper staking tools.
