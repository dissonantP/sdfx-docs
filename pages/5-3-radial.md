[back to docs root](/README.md)

[back to Pre-SDF docs](/pages/5-pre-sdf.md)

# Pre SDF: Radial Spokes

This effect is similar to "Tangent Lines" but rather than drawing lines which follow surface edge directions, it draws lines which are _perpendicular_ to them.

![img](/images/radial-1.png)

Most of the controls are the same as with Tangent Lines:

![img](/images/radial-2.png)

Note that by default, Radial Spokes are only drawn _outward_ from the shape, so "Hide Spokes Outside Source" might not show too much. You can enable "Bidirectional Spokes" to fix this:

![img](/images/radial-3.png)

"Corner Filter" (adjusted with "Corner Sensitivity") can be used to only show lines at areas with high curvature. Applying a bit of blur beforehand can smooth out surface noise and produce a cleaner result here:

![img](/images/radial-5.png)

Note that by default, lines are produced at both convex and concave curves. This can be adjusted using the "Corner Side Filter" settings:

![img](/images/radial-6.png)

Neat 👍

![img](/images/radial-7.png)

[Next: Radial Spokes](/pages/5-4-hatching.md)