[back to docs root](/README.md)

[back to Post-SDF tab docs](/pages/7-post-sdf.md)

# Post SDF Tab - Reaction Fill

This effect is pretty similar to Growth Front Fill but uses a different algorithm. Here's what I see with default settings:

<img src="/images/reaction-1.png" alt="img">

Most of the parameters are the same as Growth Front Fill. For example, "Step Radius" and "Step Iterations" are the main knobs for controlling growth distance. With Radius high and Iterations low, you get more straight lines in the result:

<img src="/images/reaction-2.png" alt="img">

For smoother growth lines, turn down Radius a bit and increase Iterations:

<img src="/images/reaction-3.png" alt="img">

Increasing iterations can make the result a bit cluttered, so you can uncheck "Preserve Previous Marks" to only keep the last iteration:

<img src="/images/reaction-4.png" alt="img">

We can hide lines above / below a certain SDF brightness using "Show above SDF brightness" and "Show below SDF brightness":

<img src="/images/reaction-5.png" alt="img">

"Seed from SDF Boundary" is similar to "Show above SDF brightness", in that it hides lines past a certain point of SDF growth. But it's different because it will use the outer boundary as a seed (so unlike "Show above SDF brightness", it's not just a post-process). The "Reaction min SDF brightness" setting controls the distance that the outer lines are seeded from:

<img src="/images/reaction-6.png" alt="img">

Similarly, "Seed below SDF brightness" will prevent lines from being seeded at the center of the SDF (unlike "Show below SDF brightness", this is not just a post-process):

<img src="/images/reaction-7.png" alt="img">

"Source separation" controls the density of the lines:

<img src="/images/reaction-8.png" alt="img">

But you can see here that it's preferring to seed lines from some locations and not others. We can make it more uniform by increasing "Open side allowance":

<img src="/images/reaction-9.png" alt="img">

The last control is "degradation", which is a post process that removes random pixels within the lines:

<img src="/images/reaction-10.png" alt="img">

[Next: Medial Maze](/pages/7-8-medial-maze.md)
