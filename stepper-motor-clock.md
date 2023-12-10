# Stepper motor clock

Instructions for using the stepper motor clock.

## Power

The clock is synchronous with the supplied AC frequency. If you run the clock off the National Grid, it should keep
good time. If you run it off AC created by an inverter or a generator it might not.

You can check the recent grid frequency at https://gridwatch.co.uk/frequency

The plug has a 3-amp fuse.

## Setting the hands

Use your index finger to **gently turn the minute hand**. The hour hand is geared to the minute hand and will turn
with it, in the proportion of hours to minutes.
Do not attempt to turn the hour hand directly as this will require a lot of torque and may break the hour hand.

A magnetic clutch allows the hands to move independently of the motor.

## Timekeeping

The clock will lose about 0.4 seconds per day. This is because the gear ratio of the stepper motor's internal
gearbox is, contrary to the representations made in the markings on the motor (16:1) and the smallprint of the datasheet (16.128:1),
about 16.03231:1. I have selected the closest geartrain I could calculate to turn this into minutes and hours, but
this still leaves an error of about 0.4 seconds per day.

Over a period of 6 months the clock will lose slightly more than 1 minute.
This is not considered a problem as the time will need setting every 6 months anyway when the clocks change.

## Components

The capacitor is a 47uF ceramic capacitor, and it lives inside a 3d-printed plug that connects to the motor cable.
https://www.digikey.co.uk/en/products/detail/tdk-corporation/FK20X5R0J476MN000/2815373

The transformer gives 6.3v AC output from 230v AC input. https://www.digikey.co.uk/en/products/detail/triad-magnetics/F-313X/5032119

The motor is a "28BYJ-48" stepper motor, but there are lots of different specifications. You want it to take 12v input
and have a 16:1 nominal gear reduction. Past that, you may have to experiment to find out that is close enough to 16.03231:1
that it will work, or change some of the gears to compensate. https://www.digikey.co.uk/en/products/detail/adafruit-industries-llc/918/5629415
