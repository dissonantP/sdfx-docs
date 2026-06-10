[back to docs root](/README.md)

[back to Pre-SDF docs](/pages/5-pre-sdf.md)

# Pre SDF Effect: Tangent Lines

As soon as we enable Tangent Lines, we can see a dramatic effect:

<img src="/images/tangent-1.png" alt="img">

What this is doing, is looking at the edges of the input shape, and drawing lines that match the directions of those edges at some locations.

We can increase the Line Length and increase Spacing (so that we create fewer lines):

<img src="/images/tangent-2.png" alt="img">

By default, it prefers to draw lines in locations that have high curvature. We can force the lines to be equally spaced by checking the "Equal Tangent Spacing" box:

<img src="/images/tangent-3.png" alt="img">

Increasing "Tangent Angle Noise" can make things look more chaotic:

<img src="/images/tangent-4.png" alt="img">

And changing "Tangent Line Offset" will move the lines away from the shape border. Values above 0 will make it go outside the shape, and values below 0 make it go inside.

<img src="/images/tangent-4-5.png" alt="img">

If we increase the SDF expansion distance, we can see that the tangent lines aren't really affecting it:

<img src="/images/tangent-5.png" alt="img">

The "Apply Before SDF" option fixes that:

<img src="/images/tangent-6.png" alt="img">

If we uncheck "Show Tangent Lines", they continue to affect the SDF but are no longer directly visible.

<img src="/images/tangent-7.png" alt="img">

By checking "Replace Source with Tangent Lines", we're essentially saying "I ONLY want to see tangent lines, and none of the original input shape". Here I've turned off SDF expansion so it's more clear:

<img src="/images/tangent-8.png" alt="img">

Enabling "Hide lines inside source" will prevent the lines from crossing into the input shape:

<img src="/images/tangent-10.png" alt="img">

As you'd expect, "Hide lines outside source" does the opposite: 

<img src="/images/tangent-14.png" alt="img">

"Post noise" is by default in "displacement" mode, which can give tendril-like results when frequency is turned low:

<img src="/images/tangent-11.png" alt="img">

The other "Post noise" type is "Erode / Dilate" which produces a more staticky type effect:

<img src="/images/tangent-12.png" alt="img">

Tangent lines can produce cool results by itself, and can give interesting variations when combined with the various SDF and Post SDF settings. For example, when we take that previous Erode / Dilate example and feed it into an SDF with "Preserve Growth Intersections" and "Draw Concentric Lines" enabled, we get something that kinda looks like coral, or a fossil.

<img src="/images/tangent-13.png" alt="img">

[Next: Edge Roughen](/pages/5-2-edge-roughen.md)