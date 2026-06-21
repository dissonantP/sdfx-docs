[back to docs root](/README.md)

[back to Post-SDF tab docs](/pages/7-post-sdf.md)

# Post SDF Tab - Concentric Lines

This is one of my favorite effects, as you've probably guessed from my frequent references to it so far.

The effect is really simple. At its core, this effect is just a modulo which we apply to the SDF brightness.

If you're unfamiliar with modulo, I'll try to explain it succinctly. X modulo Y means: divide X by Y and then discard everything except the remainder. So 3 modulo 3 would equal 0 (no remainder), 3 modulo 1 would also equal 0, and 3 modulo 2 would equal 1.

When we initially enable the effect, we see this:

<img src="/images/concentric-1.png" alt="img">

By default, the concentric lines are overlaid on top of the SDF. We can remove the raw SDF from the output entirely by checking "Color non concentric lines" (by default, it will color them black, which will hide them):

<img src="/images/concentric-2.png" alt="img">

By default, "Threshold concentric lines" is enabled, which is why our output is monotone. We can tweak "Concentric thickness" to change the line thickness:

<img src="/images/concentric-3.png" alt="img">

If we uncheck "Threshold concentric lines" we can see the modulo output directly:

<img src="/images/concentric-4.png" alt="img">

Whereas before the SDF flowed continuously from brightness 1 down to 0, now it cycles between 1 and 0 repeatedly over smaller intervals. Since modulo is 0.1, and 1 divided by 0.1 is 10, this cycle happens 10 times over the span of the SDF, and we see 10 rings. This also explains why, when you change the SDF spread radius, the spacing of the concentric lines changes as well (because it will fit the same number of rings into a smaller area).

Anyway, we can also tint the color of the concentric lines:

<img src="/images/concentric-5.png" alt="img">

Note that the white-to-black SDF is still there underneath. To see more of it, we can use "Concentric cutoff min / max" settings which will limit the area that concentric lines get drawn over. Lower "max" to hide the lines at the SDF center, and raise "min" to hide them at the outside. Here's both of them used together:

<img src="/images/concentric-6.png" alt="img">

Believe it or not, that's actually it. A pretty simple effect but can be very versatile and aesthetically pleasing.

[Next: Growth Ridges](/pages/7-4-growth-ridges.md)
