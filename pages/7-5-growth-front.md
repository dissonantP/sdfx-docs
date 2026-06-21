[back to docs root](/README.md)

[back to Post-SDF tab docs](/pages/7-post-sdf.md)

# Post SDF Tab - Growth Front

For some context. Growth Ridges kinda worked as a space-filling effect but was pretty hacky, so I decided to take a stab at creating some more "actual" space filling effects. This is the first of those.

By default, it shows medial lines and grows outward from the input shape's boundary:

<img src="/images/growth-1.png" alt="img">

Using "Hide above / below SDF boundary" we can get rid the inner and outer parts:

<img src="/images/growth-2.png" alt="img">

Note that if we set "Hide below SDF boundary" to 0 then it will grow outside the SDF bounds.

The main three knobs are "Iterations", "Growth Distance", and "Source Separation".

Increasing "Source Separation" will add more space between the lines.

<img src="/images/growth-3.png" alt="img">

Increasing "Growth Distance" by itself (with low iterations) will cause the effect to grow further outward, but in a cruder, more rigid way (which can nonetheless by stylistic):

<img src="/images/growth-4.png" alt="img">

For smoother growth lines, keep "Growth Distance" relatively low and increase "Iterations":

<img src="/images/growth-5.png" alt="img">

You may notice with certain inputs that the growth is lopsided, and stubbornly refuses to grow from certain areas. Try increasing "Open Side Allowance" if this happens, which will attempt to make the distribution more even - but at high values it does produce artifacts:

<img src="/images/growth-6.png" alt="img">

Whereas "Hide above / below" is merely a Post Process, "SDF seed cutoff" actually changes the spawn point for the effect. Incrase / Decrease it to cause the lines to spawn from more central or further locations on the SDF

<img src="/images/growth-7.png" alt="img">

You can get a more sparse effect by turning off "Preserve Previous Marks". That way, only the last iteration is kept:

<img src="/images/growth-8.png" alt="img">

You can play around with "Feedback" to change the growth pattern. At low values it starts looking like spiderwebs:

<img src="/images/growth-9.png" alt="img">

[Next: Territory Map](/pages/7-6-territory-map.md)
