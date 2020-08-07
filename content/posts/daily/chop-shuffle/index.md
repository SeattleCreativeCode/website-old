+++
title = "CHOPS: Shuffle"
date = "2019-03-08T09:31:43-07:00"
author = "Russell Hay"
authorLink = "https://graysonarts.com"
topics = ["TouchDesigner"]
tags = ["chops", "shuffle", "chop", "touchdesigner", "basics", "learning"]

[[resources]]
  src = "shuffle.png"
  title = "Shuffle Chop"
  [resource.params]
    description = "A screenshot of touchdesigner with a four channel noise chop feeding into the shuffle chop "
+++
The `shuffle` chop allows you to reshape the signals coming into the chop. There are a number of different ways to reshape it. You can convert samples into channels, or combine sequentially multiple channels into a single one, or slice the samples into a controllable number of channels.

In the example, which is a particularly contrived example, I have a four channel `noise` chop which is feeding into the `shuffle` chop. I use the `Sequence N Channels` option to combine the four channels into two channels. These are then mapped into the red and green channels via `chop to top` so that I can use them as input to `displace`. This adds a bit of predictable glitchy movement to the `displace`.

Download the touchdesigner file: {{< toe "shuffle example" >}}

{{< youtube sGZtpOM8AFQ >}}