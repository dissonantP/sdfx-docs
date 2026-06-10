[back to docs root](/README.md)

# What's an SDF?

SDF stands for Signed Distance Function/Field and here's the Wikipedia article: [link](https://en.wikipedia.org/wiki/Signed_distance_function).

Honestly I don't really understand much of that article but basically an SDF is a mathematical way to represent a shape.

Imagine an image as being grid, with each pixel being a cell.

The value for each cell is a number representing the distance from the surface of the shape.

Cells with value 0 (the black dashed line in the below image) fall exactly along the surface of the shape.

Cells with value besides 0 (e.g. 4.5 or -8) are that many units away from the surface.

Positive values are outside the shape, and negative values are inside it.

Here's an image to illustrate:

<img src="/images/whats_an_sdf.png" alt="sdf">

This method of mathematically representing shapes has a lot of uses, including for collision detection in games, and simulation of volumetric effects like fluid, fog and fire.

They can also be used for image effects, which is the purpose of this plugin.

**That being said**, this plugin does not really represent shapes using mathematical formulas. We draw greyscale pixels with varying brightness representing the SDF values. So it can be considered a rasterized distance field effect, not a fully continuous one.

[Next: Input, Output, and Effect Execution](/pages/2-input-output.md)