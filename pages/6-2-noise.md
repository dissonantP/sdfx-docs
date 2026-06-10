[back to docs root](/README.md)
[back to SDF tab docs](/pages/6-sdf.md)

# SDF Tab - Noise

Noise can be enabled via the "Global Noise" checkbox. We see the standard noise controls "amplitude", "frequency", and "seed", which I'll assume you're familiar with:

<img src="/images/noise-1.png" alt="img">

If we toggle on "Incremental Noise", the noise will start out small and then get larger near the outer edge of the SDF:

<img src="/images/noise-2.png" alt="img">

We can use the "Noise Interpolation" slider to control where noise begins. Lower values start the noise closer to the source shape's surface, and higher values start the noise only at the outer boundary of the SDF.

<img src="/images/noise-3.png" alt="img">

This can be further fine-tuned with "Noise ramp width", which I'll try and explain in a single sentence: whereas "Noise Interpolation" sets the location at which noise begins, "Noise ramp width" controls how long it takes before the noise is fully applied.

<img src="/images/noise-4.png" alt="img">
<img src="/images/noise-5.png" alt="img">

If you want to invert the interpolation so noise starts big and then gets smaller, you can do that with the "Invert Interpolation" button:

<img src="/images/noise-6.png" alt="img">
<img src="/images/noise-7.png" alt="img">

This all probably seems very esoteric until you realize that SDF noise can cause interesting variations when fed into the Post-SDF effects.

For example, here's what it looks like when fed into Concentric Lines. Note that "Incremental Noise" is enabled so that noise gets stronger as the SDF grows. In the second image, I've enabled "Invert Interpolation" so the noise gets weaker over time instead.

<img src="/images/noise-8.png" alt="img">

There are a few types of noise available using the "Noise Mode" dropdown:

<img src="/images/noise-9.png" alt="img">

The last thing to mention is that if you're using Outward / Inward growth simultaneously, you can apply independent noise settings to each.

For example, here I've unchecked "Global Noise" and have instead applied noise only to the inward growth:

<img src="/images/noise-10.png" alt="img">

Phew, that was a mouthful. Moving on.

[Next: Preserve Growth Intersections](/pages/6-3-preserve-growth-intersections.md)