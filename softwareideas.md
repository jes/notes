# Software ideas

## OpenStreetMap viewer

[2023-08-31](20230831.md) has some plans for a tool like the waypoint editor for Waypointer Moto,
but more generally useful. Like a mini-GIS.

## Timegrapher

[2023-09-22](20230922.md) I tried to use tg-timer but couldn't get it to work, and I'm not sure if
it's too specifically targeted at standard lever escapements with defined periods.

I really just want something that will listen to the microphone or an audio/video recording and tell me what frequency it is
ticking at, and maybe a way to plot some visualisation of the beat/regularity.

## Video hosting

[2023-09-23](20230923.md) has an idea for a tool like imagebin but for hosting videos, that gets
the videos out of the YouTube silo, and gives me convenient tools for counting frames etc. and
embedding in the notes system.

## Image measurer

I do a lot of image measuring, where I load up one or two images in GIMP and measure distances and/or
angles. Examples:

https://img.incoherency.co.uk/4661

https://img.incoherency.co.uk/4659

Maybe a little web tool that lets me load in an image (and optionally a 2nd image to alpha-blend on top),
and then lets me measure lengths and angles, and, *importantly*, draws the measurements on top of the
image in a way that makes it convenient for me to show the measurements. For example with red lines
and red numbers like in the examples above.

## Moodboard

Something that lets me stick in images that I want to keep in my mind, crop them, scale them, and lay them
out in a sensible way. I don't want to have to manually do the layout, but I want to be able to manually
tweak the layout. I think Pinterest sort of does this, but I'm not interested in proprietary software or
data silos.

## G-code sender

The G-code sender should have normal overrides like feed rate and spindle speed, but it should also
preprocess your G-code and offer a "depth of cut" override. Also preprocess your G-code to detect
different "sections" and allow just running 1 section at a time, or repeating a section with different
depth (repeating with different cutter compensation?). And finally, maybe detect helix moves, or pocket
moves, and allow a "width of cut" override? That one is much harder.

If I made a G-code sender to my taste I'd probably want to use it everywhere, which means the milling
machine would probably have to switch to Grbl, and Grbl doesn't have cutter compensation, so might have to skip that.

Maybe it's best to add my features to UGS instead of starting from scratch, not sure which would be more trouble.

Features I like from UGS, or would like that aren't in UGS:

* MDI but with pipelining of commands
* 3d view
* g-code view
* click in 3d view to "jog to here", "set current coordinates" or "follow outline"
* DRO with arithmetic
* jogging - maybe want an easy way to make a physical jog controller with knobs for feed rate etc.
* display of active G codes (G91 etc.)
* standard overrides
* "run from line" in g-code display
* current Z coordinate override
* depth of cut override
* "section" runner
* start section from a given depth (i.e. skip the first few laps)
* stop section at a given depth (i.e. skip the last few laps)

Probably the first things to look at are how easy it is to preprocess the G-code to detect sections and laps,
and how easy it is to interrupt Grbl to flush the planner buffer so that we can change the Z coordinate.

On [2023-11-19](20231119.md) I broke a tool because I did some mental arithmetic wrong in adjusting the Z
offset. My custom G-code sender should have a way to say "move Z down by 0.1mm" without the user having to
do any mental arithmetic to work out "OK, it's at Z=5, so I need to touch off at Z=5.1 to get it to be 0.1mm
lower".

## Debughackers

It's like Protohackers except every problem is a program and a bug report, and you have to fix the bug
and submit your patch, shortest patch wins.

Maybe the entire buggy application is released upfront and the UI is like a bug tracker, and then the
leaderboard is based on a score for how many you've solved, and how short your patches were, tie-broken
by the time submitted. The leaderboard could show a SHA256 of the patch so you can see which people
had different fixes.

Twists:

* no bug report
* incorrect bug report
* multiple bug reports
* multiple bugs
* you don't have to submit a patch, you have to submit an *exploit*

## Gear train calculator

You give it the ratio (with tolerance?), the minimum/maximum number of gears, the minimum/maximum number of teeth per gear,
and any numbers of teeth that are already fixed, and it searches to find solutions.
