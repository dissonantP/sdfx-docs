[back to docs root](/README.md)

[back to Post-SDF tab docs](/pages/7-post-sdf.md)

# Post SDF Tab - Concentric Lines

This is one of my favorite effects, as you've probably guessed from my frequent references to it so far.

The effect is really simple. At its core, this effect is just a modulo which we apply to the SDF brightness.

If you're unfamiliar with modulo, I'll try to explain it succinctly. X modulo Y means: divide X by Y and then discard everything except the remainder. So 3 modulo 3 would equal 0 (no remainder), 3 modulo 1 would also equal 0, and 3 modulo 2 would equal 1.

You can see the result on the SDF here. Note that "threshold concentric lines" is on by default, I've turned it off so we can see the modulo result directly:

<img src="/images/concentric-1.png" alt="img">

Whereas before the SDF flowed continuously from brightness 1 down to 0, now it cycles between 1 and 0. Since modulo is 0.2, and 1 divided by 0.2 is 5, this cycle happens 5 times over the span of the SDF. This explains why, when you change the SDF spread radius, the spacing of the concentric lines also changes.

[Next: Border](/pages/7-2-border.md)
