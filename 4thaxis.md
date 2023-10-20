# 4th axis

Positive angles turn the axis **anti-clockwise** as you view towards the chuck. (Is that how it should be?).

## Alignment

[2023-09-08](20230908.md): I cut gear teeth using the 4th axis, it was 0.25mm out of concentric. I wrote a Perl script
to correct for the concentricity error, it works pretty well.

[2023-09-03](20230903.md): I re-cut the register for the chuck to try to improve concentricity.

[2023-10-17](20231017.md): Concentricity error in cutting pivots was about
0.27mm. So this is no better than before! OK some of the error is from
the collet, but I did notice that the high spot was always in the same
place relative to the chuck register, so the chuck register is definitely
the major source of error.

[2023-10-20](20231020.md): I discovered that the source of the concentricity error is that
the chuck is registering on the *bolts* rather than on the register. I widened the bolt holes
and now it is possible to centre it, but there is a bit of play in the register. Better than
before though.

## Potential improvements to the 4th axis

* re-cut the chuck register again?
* some method to more accurately square it to the table
* a (manual?) "brake" to lock it in place to take the load off the servo, when just using for positioning

## Concentric gear cutting

See https://github.com/jes/concentric-gear-cutting for the script to counteract the eccentricity.

## Concentric pivot cutting

There's a script in https://github.com/jes/concentric-gear-cutting
for cutting pivots on shafts.

Also instructions in [20231017.md](20231017.md) for an efficient workflow.
