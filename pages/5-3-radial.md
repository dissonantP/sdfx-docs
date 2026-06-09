[back to docs root](/README.md)

[back to Pre-SDF docs](/pages/5-pre-sdf.md)

# Pre SDF: Radial Spokes

This effect is similar to "Tangent Lines" but rather than drawing lines which follow surface edge directions, it draws lines which are _perpendicular_ to them.

![img](/images/radial-1.png)

Many of the controls will be familiar from the Tangent Lines effect. For example here I've decreased Line Length, increased density by lowering Spacing, and offset from center:

![img](/images/radial-2.png)

"Equal Spoke Spacing" attempts to space the lines equally from one another (alas, it is still imperfect - a potential area of improvement):

![img](/images/radial-3.png)

As with Tangent Lines, there are options to control how the generated lines feed into the output:

![img](/images/radial-4.png)

"Corner Filter" (adjusted with "Corner Sensitivity") can be used to only show lines at areas with high curvature. Applying a bit of blur beforehand can smooth out surface noise and produce a cleaner result here:

![img](/images/radial-5.png)

Note that by default, lines are produced at both convex and concave curves. This can be adjusted using the "Corner Side Filter" settings:

![img](/images/radial-6.png)

[Next: Radial Spokes](/pages/5-4-hatching.md)