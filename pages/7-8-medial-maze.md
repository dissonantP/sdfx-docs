[back to docs root](/README.md)

[back to Post-SDF tab docs](/pages/7-post-sdf.md)

# Post SDF Tab - Medial Maze

The last Post-SDF effect to discuss is Medial Maze. Here's what it looks like with default settings:

<img src="/images/maze-1.png" alt="img">

I'll increase spacing to make the lines a bit less dense, and increase thickness to make the lines themselves bigger:

<img src="/images/maze-2.png" alt="img">

"Follow SDF ridges" makes the maze reflect the directionality of the SDF expansion (notice how the lines are more horizontal / vertical at the borders):

<img src="/images/maze-3.png" alt="img">

"Branch length" can be reduced:

<img src="/images/maze-4.png" alt="img">

Reduce "Maze density" to limit the outward expansion of the maze:

<img src="/images/maze-5.png" alt="img">

"Branch angle jitter" introduces some randomness into the line directions:

<img src="/images/maze-6.png" alt="img">

We also have "Avoid SDF above brightness" and "Remove below SDF brightness". They are named differently because the first affects the seed, and the second is just a post-process:

<img src="/images/maze-7.png" alt="img">

[Next: Output and Multi-Pass](/pages/8-output.md)
