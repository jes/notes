# Anniversary Clocks

## Resources

 * http://www.thehorolovarcompany.com/
 * https://www.clockworks.com/clock-repair/clock-repair-help-1.html
 * https://www.youtube.com/watch?v=-EsKQANaKY0

## Principles

At first glance the anniversary clock seems pretty much directly isomorphic to a pendulum clock,
but it is quite a bit more subtle because of the fact that the "pendulum" and the escapement are joined by a *spring*.
I'm working with a deadbeat escapement, so the following applies in addition to everything that would normally apply to a deadbeat escapement.

While the impulse is being delivered, the part of the spring that the fork is attached to is being driven
"ahead" of the position that the balance wheel's rotation would naturally place it. This puts energy in the
spring, which accelerates the balance wheel.

If the impulse is completed too quickly, then the fork will "snap back", which will pull the anchor back
towards the centre. This effect is unavoidable. The only way the fork will not "snap back" once the impulse
is complete is if the impulse is not adding any energy.

If the fork snaps back far enough, then it will pull the anchor back to a position such that the next tooth,
due to land on the locking face of its adjacent pallet, will instead land directly on the impulse face.
It will then immediately push the anchor back the other way, and the clock will rapidly run down. This is
called *flutter*.

At its core, *flutter* is caused by the suspension spring "snapping back" too far once the impulse is removed.

Causes of flutter include:

 * too much torque provided: the drive torque is too great, so the impulse is delivered too quickly
 * too little torque required: the spring is too weak (or similarly, too long), so it takes too little torque to rotate it by the applicable angle
 * not enough rotation: the relationship between the fork and the lever is wrong, such that the spring is not being rotated by enough angle before the tooth can escape
 * not enough locking safety margin: if the anchor snaps back by 1 degree, then you need more than 1 degree of locking safety margin on the escapement
 * too much moment of inertia: this effect is only minor, because during the impulse the spring is being "wound up" relative to the balance wheel, but it is still true that if the balance wheel moves further during the impulse phase, then the "snap back" is reduced

The next problem unique to the anniversary clock is that when the lever and fork are interacting, the effect
on the suspension spring is not a pure torque, but is also pushing it to one side or the other. My intuition is that
this is a waste of energy, but I haven't proved that.

The effect can be reduced by:

 * move the fork closer to the mounting point so that moving it sideways would put a sharper angle in the spring, which would mean any given sideways movement implies a larger vertical movement, i.e. takes more energy
 * make the balance wheel heavier so that any given vertical movement takes more energy, or equivalently so that the tension in the spring is larger
 * reduce drive torque so that the torque on the spring is lower
 * reduce leverage so that the torque on the spring is lower

And then the next thing is that there is some minimum amplitude that the clock needs to achieve in order
for escapement to occur. You can imagine that clamping the fork near to the suspension
spring means that, absent any force from the anchor, it moves in proportion to the balance wheel (if the fork is 1/10 of the way down,
then it rotates 1/10 as far as the balance wheel does), and obviously if it doesn't move far enough then it doesn't
push the anchor far enough and therefore the escape wheel never escapes.

Increasing the weight on the balance wheel is desirable
because of the associated increase in moment of inertia, but the downside is that a balance wheel with a given
amount of energy will have a lower amplitude if it has a higher moment of inertia. So if you make the balance
wheel too heavy then you won't have enough amplitude for the escapement to work.
