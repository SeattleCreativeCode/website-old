+++
title = "CHOPS: Noise"
date = "2019-03-07T14:53:20-07:00"
author = "Russell Hay"
authorLink = "https://graysonarts.com"
topics = ["TouchDesigner"]
tags = ["chops", "chop", "noise", "touchdesigner", "basics", "learning"]

[[resources]]
  src = "noise.png"
  title = "Noise Chop"
  [resource.params]
    description = "A screenshot of touchdesigner with noise driving a collection of lines that move and flash"
+++
`Noise` oh how I love the `noise` chop. It's a great way to add movement and interest into a system without having to be specific about what you want to create. By using noise, you can add variety into the system and generate an infinite combination of things.

`noise` is a bit different than a pure random number generator because it tries to give a better transition between consecutive values.

The below sketch is `noise` that is converted to a `top` and then animated using a `timer`.

Download the touchdesigner file: {{< toe "noise example" >}}

{{< youtube lqTKbTEwHpU >}}