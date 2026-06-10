[back to docs root](/README.md)

[back to Pre-SDF docs](/pages/5-pre-sdf.md)

# Pre SDF: Radial Spokes

This effect is similar to "Tangent Lines" but rather than drawing lines which follow surface edge directions, it draws lines which are _perpendicular_ to them.

<img src="/images/radial-1.png" alt="img">

Most of the controls are the same as with Tangent Lines:

<img src="/images/radial-2.png" alt="img">

Note that by default, Radial Spokes are only drawn _outward_ from the shape, so "Hide Spokes Outside Source" might not show too much. You can enable "Bidirectional Spokes" to fix this:

<img src="/images/radial-3.png" alt="img">

"Corner Filter" (adjusted with "Corner Sensitivity") can be used to only show lines at areas with high curvature. Applying a bit of blur beforehand can smooth out surface noise and produce a cleaner result here:

<img src="/images/radial-5.png" alt="img">

Note that by default, lines are produced at both convex and concave curves. This can be adjusted using the "Corner Side Filter" settings:

<img src="/images/radial-6.png" alt="img">

Neat 👍

<img src="/images/radial-7.png" alt="img">

[Next: Hatching](/pages/5-4-hatching.md)