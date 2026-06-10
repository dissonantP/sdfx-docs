[back to docs root](/README.md)

[back to Pre-SDF docs](/pages/5-pre-sdf.md)

# Pre SDF: Stipple

Stipple fills the input shape with dots.

Many of the parameters will be familiar (to set color, spacing, size, and SDF rendering / interaction).

<img src="/images/stipple-1.png" alt="img">

As with hatching, we can randomize the size within a range:

<img src="/images/stipple-2.png" alt="img">

When density is below 1, dots start getting randomly removed:

<img src="/images/stipple-3.png" alt="img">

Jitter applies noise to the dot positions, changing the layout from a grid to purely random:

<img src="/images/stipple-4.png" alt="img">

<img src="/images/stipple-5.png" alt="img">

[Next: Directional Extrude](/pages/5-6-extrude.md)