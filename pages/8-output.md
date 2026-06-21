[back to docs root](/README.md)

# Output and Multi-Pass

The output tab gives us a few various rendering controls.

## SDF Rendering

All the Post-SDF effects have the ability to hide the input SDF shape via settings like "Color non concentric lines" or "Color non medial maze". However, if none of those are enabled, the SDF will make it through to the output.

In that case, we can use the settings here to tint it, or to remove it above / below a certain brightness.

<img src="/images/output-1.png" alt="img">

Preserved Growth Intersection lines have their own color control in the SDF tab. They are rendered as an output overlay, so they can remain visible even when the SDF brightness field is hidden with the SDF min / max controls.

We also have the option to threshold the output. Obviously you can do this natively in Photoshop, but it's just here as a convenience:

<img src="/images/output-2.png" alt="img">

## Blend source into output

The next section here is "Blend source into output" which by default is set to blend in the original input.

<img src="/images/output-4.png" alt="img">

Let's say for example we have produced this as our output, and we want to show the original insect in the center:

<img src="/images/output-3.png" alt="img">

This works like Photoshop's native "Blend If" control. We can raise "Effect black cutoff" to bring in the original input everywhere that our effect is dark:

<img src="/images/output-5.png" alt="img">

The rest of the settings here "Effect white cutoff", "Source black cutoff", and "Source white cutoff" work the same as Photoshop's "Blend-If", so I'll skip explaining them here.

One thing to note, though. Our plugin doesn't play nicely with Alpha so if your image has a transparent background, put a solid color layer under it, group them, and use the group as input (I mentioned this earlier in the docs, with regards to text effects):

<img src="/images/output-6.png" alt="img">

Note that you can do the exact same thing with Photoshop's native "Blend If" control, so using the plugin UI to blend in the original input is optional:

<img src="/images/output-7.png" alt="img">

The "Previous pass" blend source is not possible with Photoshop's native tooling, however. But to explain that, I first need to briefly explain Multi-pass

## Multi pass

You can enable two-pass or three-pass with these buttons at the top of the plugin:

<img src="/images/output-9.png" alt="img">

Enabling two-pass just adds another row of settings tabs:

<img src="/images/output-10.png" alt="img">

The mechanics are really simple here. The first pass' output gets fed into the second pass as input. Of course, this isn't strictly necessary, since you can manually bake out an output and start over with the plugin using that as the input. But using multi-pass is nice because it keeps everything procedural.

For example, here I do the following:
- First pass: concentric lines, colored green, with the original SDF hidden
- Second pass: grow SDF, apply SDF noise, add concentric lines colored purple, blend in previous pass via Output tab

<img src="/images/output-11.png" alt="img">

Here's what that looks like in the Output tab of the second pass:

<img src="/images/output-12.png" alt="img">

Two-pass (or three-pass, for the adventurous) are powerful controls which can create some chaotic, novel effects. Experiment with them and see what strikes your fancy.

[Next: Presets](/pages/9-presets.md)
