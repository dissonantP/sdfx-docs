[back to docs root](/README.md)

# Settings Tabs - a high level overview

Settings are split among 5 tabs. They are run in order, e.g. "Prep" affects "Pre SDF", which affects "SDF", and so on. 

<img src="/images/settings-tabs.png" alt="settings-tabs">

- **Prep** does some basic adjustments on the input image (blurring, sharpening, threshold, and invert).
- **Pre-SDF** offers some experimental / artistic effects on the input image
- **SDF** is where you control the SDF effect itself, as you'd expect.
- **Post SDF** is for various postprocess effects which make use of the SDF. It also contains some growth algorithms which are not strictly speaking dependent on the SDF, but play well with it.
- **Output** offers a few controls for the final output. The main one is for blending in the original input.

[Next: Prep Tab](/pages/4-prep.md)