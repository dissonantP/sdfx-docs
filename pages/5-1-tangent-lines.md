[back to docs root](/README.md)

[back to Pre-SDF docs](/pages/5-pre-sdf.md)

# Pre SDF Effect: Tangent Lines

As soon as we enable Tangent Lines, we can see a dramatic effect:

![img](/images/tangent-1.png)

What this is doing, is looking at the edges of the input shape, and drawing lines that match the directions of those edges at some locations.

We can increase the Line Length and increase Spacing (so that we create fewer lines):

![img](/images/tangent-2.png)

By default, it prefers to draw lines in locations that have high curvature. We can force the lines to be equally spaced by checking the "Equal Tangent Spacing" box:

![img](/images/tangent-3.png)

Increasing "Tangent Angle Noise" can make things look more chaotic:

![img](/images/tangent-4.png)

And changing "Tangent Line Offset" will move the lines away from the shape border. Values above 0 will make it go outside the shape, and values below 0 make it go inside.

![img](/images/tangent-4-5.png)

If we increase the SDF expansion distance, we can see that the tangent lines aren't really affecting it:

![img](/images/tangent-5.png)

The "Apply Before SDF" option fixes that:

![img](/images/tangent-6.png)

If we uncheck "Show Tangent Lines", they continue to affect the SDF but are no longer directly visible.

![img](/images/tangent-7.png)

By checking "Replace Source with Tangent Lines", we're essentially saying "I ONLY want to see tangent lines, and none of the original input shape". Here I've turned off SDF expansion so it's more clear:

![img](/images/tangent-8.png)

All this is intended to be a procedural way to feed interesting input to the SDF and Post SDF settings. For example, here's a result with the Concentric Lines effect enabled again:

![img](/images/tangent-9.png)

[Next: Edge Roughen](/pages/5-2-edge-roughen.md)