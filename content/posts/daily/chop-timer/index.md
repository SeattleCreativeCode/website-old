+++
date = "2019-03-07T00:00:00+0800"
title = "CHOPS: Timer"
author = "Russell Hay"
authorLink = "https://graysonarts.com"
topics = ["TouchDesigner"]
tags = ["chops", "chop", "timer", "touchdesigner", "basics", "learning"]
image = "timer.png"
imagetext = "A screenshot of touchdesigner with a timer that feeds into a circle."
+++
The `Timer` chop is the first one where we get a bit of real complexity in what it takes to make it work.  Out of the box, it has three channels. Two are "binary" channels, for `ready` and `done`. The other is an increasing `timer_fraction` which represents the progress of the timer.

Out of the box, `Timer` isn't going to do anything because there are two signals that need to happen for timer to start working. Inside of the attributes, there is a `init` and `start` pulse buttons.  `init` will cause `ready` to go to `1`. Once we hit `start`, `ready` will go to `0`, and `timer_fraction` will start to increase.  Once the timer is completed, `done` will go to `1`.

If you want to have `Timer` repeat, you need to change `on done` to `re-start`.  This will cause the timer to repeat. I think you still need to send the initialize signal once for things to start.

Additionally, `Timer` can be configured to have multiple segments so the timing doesn't have to be static. In order to use the segment feature, you'll need to attach a `Table DAT` to the `Segment DAT` in `Timer`. You'll need to create columns for the things listed in [`Timer`'s documentation](https://docs.derivative.ca/index.php?title=Timer_CHOP#Parameters_-_Segments_Page).

In the example, I'm using two of the columns in the `Segment DAT`: `begin` and `length`. This allows me to create multiple segments of timing for the growing.

Download the touchdesigner file: {{< toe "timer example" >}}

{{< youtube xgIac0Nwzf4 >}}