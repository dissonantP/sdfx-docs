[back to docs root](/README.md)

[back to Post-SDF tab docs](/pages/7-post-sdf.md)

# Post SDF Tab - Territory Map

This effect splits the SDF into regions and draws lines dividing them. Here's what I see with default settings:

<img src="/images/territory-1.png" alt="img">

"Cell Spacing" controls the number of lines that are draw. "Territory distance" control how far outward the lines go. If we want to draw a ring connecting the outward points of the lines, we can enable "Draw Outer Border":

<img src="/images/territory-2.png" alt="img">

By lowering "Start Brightness", we can make the lines originate from farther out on the SDF.

Here, I've also checked "Color non boundaries" so the effect is more clear:

<img src="/images/territory-3.png" alt="img">

Using "Draw Inner Border" we can connect the inner points of the lines.

Here, I've also enabled "Preserve Growth Intersections" to presere the shapes of the letters:

<img src="/images/territory-4.png" alt="img">

By increasing "Cell Irregularity", we can add more subdivisions: 

<img src="/images/territory-5.png" alt="img">

We can affect the placement of these subdivisions using the "Outer Bias" slider. Moving below 0 makes them more concentrated at the center, and moving above 0 makes them more concentrated at the outside:

<img src="/images/territory-6.png" alt="img">

<img src="/images/territory-7.png" alt="img">

Nifty.

<img src="/images/territory-8.png" alt="img">

[Next: Reaction Fill](/pages/7-7-reaction-fill.md)
