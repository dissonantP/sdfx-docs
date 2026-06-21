[back to docs root](/README.md)

[back to Post-SDF tab docs](/pages/7-post-sdf.md)

# Post SDF Tab - Growth Ridges

This is a kind of weird effect which can do a couple things.

For some context, this is actually an earlier iteration of the "Preserve Growth Intersections" effect which didn't really work well for that purpose, but was kinda cool in its own way so I kept it.

By default, it draws two rings, one at the SDF's outer boundary and one at the midpoint.

<img src="/images/ridges-1.png" alt="img">

The shape can be simplified by increasing the "Source Separation":

<img src="/images/ridges-2.png" alt="img">

The outer ring can be offset further away by increasing "Grow Outward":

<img src="/images/ridges-3.png" alt="img">

Similarly, you can move the inner ring around using "Grow Inward". In the following image I've hidden the original SDF using "Color Non Growth Ridges" and also applied "Preserve Growth Intersections" so we can continue to see the outlines of the letters:

<img src="/images/ridges-4.png" alt="img">

A couple other settings:
- Uncheck "Include Outside Boundary" to include only the inner ring.
- Increase "Growth Ridge Centering" to move offset both rings toward to the center.

With some tweaking (specifically, changing "Grow outward" to very low e.g. 0.01) you can get just the centerlines of the shape, which is cool:

<img src="/images/ridges-5.png" alt="img">

Increasing "Growth Ridge Centering" even more and enabling "Color non growth ridges", we get a cleaner result, if clean is what you're after:

<img src="/images/ridges-6.png" alt="img">

This effect can work well as a space-filling algorithm when you run it a couple times in sequence, although some of the other Post-SDF effects do a better job (basically, all the remaining ones which we haven't discussed yet).

Here's an example of an art piece I did using multiple Growth Ridge Iterations. It's some old game box art, modded.

<img src="/images/ridges-7.png" alt="img">

[Next: Growth Front](/pages/7-5-growth-front.md)
