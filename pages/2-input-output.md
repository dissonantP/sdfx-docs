[back to docs root](/README.md)

# Input, Output, and Effect Execution

Here we'll explain this part of the UI:

![img](/images/input-output-ui.png)

## Input

You select input by simply clicking on a layer in Photoshop's layers panel.

![img](/images/click-layer.png)

You can also click on groups, in case you want to use a stack of layers as the input.

![img](/images/click-group.png)

The plugin will rasterize the given group behind the scenes (don't worry, it won't overwrite your group).

It's important to understand that ONLY the selected layer or group will be used for input. So if you want multiple things to be included in the input, put them all together in a group.

You can press the "Lock" icon at the top of the plugin panel to lock your layer / group selection. This means, even if you click on something else, the plugin's input source will remain the same.

## Output

By default, the output is set to "Create New Layer". After the plugin executes for the first time, it will automatically change the output to point to this newly created layer. So it will re-use the same layer for subsequent executions instead of creating more layers.

This behavior (that the output layer is reused) has benefits. You can add procedural effects on the output, and they will apply whenever the SDF effect is re-executed:

![img](/images/output-fx.png)

If you want, you can manually select an output layer to write to. You can press "Refresh Layers" to get an updated list of layers in your scene. Or you can switch it back to "Create New Layer" if you want a fresh output layer.

## Triggering Execution

The lightning bolt icon toggles "Apply Results Immediately" mode. When checked off, the plugin will only run when you manually click the "Execute" button. When checked on, it will automatically update the output every time you change a setting or move a slider.

[Next: Settings Tab (high level overview)](/pages/3-settings-tabs.md)