+++
date = "2019-03-02T00:00:00+0800"
title = "CHOPS: LFO"
summary = "TouchDdesigner Deep Dive Day One, CHOPS, LFO"
author = "Russell Hay"
authorLink = "https://graysonarts.com"
topics = ["TouchDesigner"]
tags = ["chops", "chop", "lfo", "touchdesigner", "basics", "learning"]
image = "lfo.png"
imagetext = "A screenshot of touchdesigner with three LFO CHOPs feeding into a circular gradient."
+++
In the previous entry [CHOPS: Constant]({{< ref "chop-constant/index.md" >}}), in order to get any kind of motion, we had to write a python expression. If all we had was `constant` chops, we could still get alot accomplished by using python expressions to drive a visual, but that would get tedious, and I have a feeling cooking performance would suffer, though that's mostly just conjecture on my part.

We used `sin` over the elapsed time to add motion. `LFO` is specifically designed to do just that! It applies a function over time and generates a control signal based on that function.

In this sketch, I replaced the `constant` chops with `LFO` chops. In order to make it more interesting, I fed the output of a `sin LFO` to the offset of the next `sin LFO`, and then for the last `LFO` I set it to a `ramp` function.

All of these were fed into a `DAT` which is controlling a `ramp top` to create a gradient. The network above has some details in order to drive the `ramp top` correctly because it needs two rows.

In the video below, I'm using `Op Viewer`, `layout`, and `movie file out` to create the view so you can see each of the control signals as well as the output.

Download the touchdesigner file: {{< toe "lfo example" >}}

{{< youtube mJ43js2nXaE >}}