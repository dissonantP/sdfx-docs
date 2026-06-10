[back to docs root](/README.md)

# Prep Tab

<img src="/images/prep-tab-ui.png" alt="prep-tabs">

This tab is simple, but can strongly affect the output image by helping define the "shapes" which are fed into the SDF.

All of the effects in this tab can already be done natively by Photoshop, they are just here for convenience.

NOTE: I know I haven't covered the other tabs yet, but I will show a bit of them here just because it's necessary to understand the implications of the Prep settings.

Let's consider this input image:

<img src="/images/silverfish.png" alt="silverfish">

First thing we need to consider is this: what's the "inside" of the shape, and what's the "outside"?

The answer is simple. The SDF algorithm considers pixels above 50% brightness "inside" and the rest "outside".

Since the insect is dark and the background is white, the background will be considered the "inside" of the shape and the SDF will attempt to "grow" into the space occupied by the insect.

With everything in "Prep" turned off, this produces an underwhelming SDF result:

<img src="/images/silverfish-2.png" alt="silverfish">

We can fix this by toggling "Invert" on. Now the insect is treated like the "Inside", and the SDF grows outward from it, producing a kind of glow.

<img src="/images/silverfish-3.png" alt="silverfish">

We can visualize the SDF another way by enabling "Draw Concentric Lines" in the Post SDF tab:

<img src="/images/silverfish-4.png" alt="silverfish">

Here you can see the rings emanating outward from the insect. But the insect shape is not well-preserved. This is because the insect varies greatly in brightness, so the SDF has a hard time figuring out what's the "inside" of the shape vs the "outside".

That's where "Pre-Threshold" comes in. Toggling that on and adjusting the cutoff, we see the shape preserved much better:

<img src="/images/silverfish-5.png" alt="silverfish">

For images with a lot of noise, "Blur" can help smooth things out, making thresholding work better. In the case of our insect image, it just removes detail:

<img src="/images/silverfish-7.png" alt="silverfish">

"Sharpen" can be helpful when you have a low-res source image that you've scaled up. It can help firm up edges, which may have become become blurry during upscaling. You can play around with using it for other purposes. In this case, you can see it accentuates some of the detail in the center of the insect shape.

<img src="/images/silverfish-8.png" alt="silverfish">

[Next: Pre-SDF Tab](/pages/5-pre-sdf.md)