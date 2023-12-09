# Stepper motor clock

Instructions for using the stepper motor clock.

## Power

The clock is synchronous with the supplied AC frequency. If you run the clock off the National Grid, it should keep
good time. If you run it off AC created by an inverter or a generator it might not.

You can check the recent grid frequency at https://gridwatch.co.uk/frequency

The plug has a 3-amp fuse.

## Setting the hands

Use your index finger to **gently turn the minute hand**. The hour hand is geared to the minute hand and will turn
with it, in proportion of hours to minutes.
Do not attempt to turn the hour hand directly as this will require a lot of torque and may break the hour hand.

## Timekeeping

The clock will lose about 0.4 seconds per day. This is because the gear ratio of the stepper motor's internal
gearbox is, contrary to the representations made in the markings on the motor (16:1) and the smallprint of the datasheet (16.128:1),
about 16.03231:1. I have selected the closest geartrain I could calculate to turn this into minutes and hours, but
this still leaves an error of about 0.4 seconds per day.

Over a period of 6 months the clock will lose slightly more than 1 minute.
This is not considered a problem as the time will need setting every 6 months anyway when the clocks change.

## Troubleshooting

If the clock makes a loud buzzing noise but is otherwise working, turn it off and on again to cure the buzzing.
The exact cause of the buzzing is not known, but it has been observed immediately after a transient dip in grid voltage.

If the clock makes a quiet buzzing noise and is stopped, this suggests there is not enough torque to turn the geartrain.
Pull the drive pin piece off the motor shaft and how hard it is to turn the geartrain, from the motor end, by hand. It
should be extremely easy. If it is not easy to turn, inspect the geartrain for faults. If it is easy to turn, then the
problem could be any of:

 * the motor is damaged
 * the capacitor is disconnected or damaged
 * the transformer is damaged

It should be easy to replace the motor, but you will need to acquire one with an internal gear ratio of about 16.03231:1
otherwise the clock will run at the wrong speed.

The installed capacitor is a ceramic capacitor of 47uF, and it lives inside the 3d-printed plug that connects to the motor cable.

The installed transformer is either 6.3v or 12v.
