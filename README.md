# Hex display circuit files

I can't guarantee these are correct!
This is from memory + old drawings of a perf-board design.

The general idea is this:

* 555 timer as an oscillator
* 74HC74 flip-flop to provide two phases of equal duration
* ATF16V8 with logic to control the 7-segment display
* On one half, drive the left segment; on the other half, drive the right segment

Some problems:

* I'm using a single 330 ohm resistor, where as I should have used one per segment
* 74HC74's driver might not be enough for all segments, so a buffer (74HC541) might be useful

Code was compiled using galasm.
