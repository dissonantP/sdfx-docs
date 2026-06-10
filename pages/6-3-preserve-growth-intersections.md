[back to docs root](/README.md)
[back to SDF tab docs](/pages/6-sdf.md)

# SDF Tab - Preserve Growth Intersections

As the SDF grows, it usually causes self-intersections. This setting highlights those intersection edges.

It's one of my favorite features of the plugin and specifically it's really indispendable for making word art.

Let's finally put the insect aside and use some text as a starting point.

By the way, when working with un-rasterized text layers, you should put a solid color background behind it, then group both of them and use that group as the input. The plugin isn't set up to work with transparent backgrounds.

<img src="/images/intersect-1.png" alt="img">

Now let's add some SDF growth and then apply Thresholding via the Output tab. 

<img src="/images/intersect-2.png" alt="img">
<img src="/images/intersect-3.png" alt="img">

Kinda sucks right? Certainly doesn't look like text anymore.

Now let's enable "Preserve Growth Intersections":

<img src="/images/intersect-4.png" alt="img">

Instantly, we can see our letters again. But it needs some tweaking.

Increasing "Intersection Source Separation" cleans it up right away. This is basically a sensitivity slider. Increase it further, and you'll see even more of the lines disappear.

<img src="/images/intersect-5.png" alt="img">

The other settings are mainly for fine-tuning and niche cases.

"Intersection Source Separation" hides the lines above a certain SDF brightness, should you find a need for that:

<img src="/images/intersect-6.png" alt="img">

I don't really have an example on hand to show the benefits of "Intersection Continuity" but if you find that your intersection lines are stubborn and won't become continuous, you can see if it helps.

[Next: Post SDF](/pages/7-post-sdf.md)