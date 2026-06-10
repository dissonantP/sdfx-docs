[back to docs root](/README.md)
[back to SDF tab docs](/pages/6-sdf.md)

# SDF Tab - Growth modes and simple adjustments

I mentioned earlier that SDF expansion treats white shapes as the "inside" and grows outward from there.

Actually, there are three growth modes - "Grow Outward", "Shrink Inward", and "Shade Inward".

By default, only "Grow Outward" is enabled, and you can control the spread distance using the "SDF spread radius" parameter:

<img src="/images/sdf-1.png" alt="img">

If we enable "Shrink Inward", we can now see the border of the shape preserved as a black line.

<img src="/images/sdf-2.png" alt="img">

With "Grow Outward", the border of the shape is bright white, and pixels farther away get darker (preserving the interior of the shape as pure white).

With "Shrink Inward", a second effect takes place simultaneously to transform the interior of the shape. The borders are now treated as black, and that blackness spreads internally. As a result, increasing the spread radius causes the interior to become more dark:

<img src="/images/sdf-3.png" alt="img">

If this is not desirable, we can apply separate "SDF Spread Radius" values to "Grow Outward" and "Shrink Inward". We just need to uncheck "Lock Spreads". Then we can tweak the Spread Radius independently:

<img src="/images/sdf-4.png" alt="img">

"Shade Inward" is basically the same as "Shrink Inward" except it spreads white from the border inward, instead of black.

Note that "Shade Inward" and "Shrink Inward" are mutually exclusive; both cannot be turned on at the same time.

<img src="/images/sdf-5.png" alt="img">

We can use the "Pow" slider to control the falloff curve. Increasing it past 1 makes the bright pixels brighter and the dark pixels darker. Decreasing it below 1 makes all non-black pixels brighter:

<img src="/images/sdf-9.png" alt="img">
<img src="/images/sdf-6.png" alt="img">

This can cause some interesting variation when "Concentric Lines" is enabled (which I know we haven't covered yet). At pow = 1, the lines are equal thickness. But when pow under 1, they start large and grow smaller (and vice versa when pow is above 1):

<img src="/images/sdf-7.png" alt="img">

Lastly, we have "Quantize Step" which essentially just posterizes the SDF brightness:

<img src="/images/sdf-8.png" alt="img">


[Next: Noise](/pages/6-2-noise.md)