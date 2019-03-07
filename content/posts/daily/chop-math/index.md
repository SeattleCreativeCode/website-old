+++
date = "2019-03-03T00:00:00+0800"
title = "CHOPS: Math"
summary = "TouchDdesigner Deep Dive Day One, CHOPS, Math"
authors = ["stainless"]
topics = ["TouchDesigner"]
tags = ["chops", "chop", "math", "touchdesigner", "basics", "learning"]

[[resources]]
  src = "math.png"
  title = "Math Chop"
  [resource.params]
    description = "A screenshot of touchdesigner with two LFO chops feeding into a math chop which is driving a circle top."
+++
The `math` chop allows you to combine channels into a single value or scale them up/down using pre-add, post-add, and multiply. This allows you to combine simple chops to create complex movement. In the case of the sketch that I created, it allowed me to create a bit of [anticipation](https://www.youtube.com/watch?v=F8OtE60T8yU) in the movement.

It took some experimenting to get the motion smoothed out to the point where it is. There are plenty of places for tweaking parameters inside of the `math` chop. In my case, the `channel pre op` is set to `Square`. The `Combine` for both channels and chops are set to `Add`, and the `pre-add` is `0.25` and the multiply is `0.5`.  This gave a nice movement when set to the `radius` of my `Circle` top. The rest of the motion is driven by the `LFOs` that are feeding into the `math` chop.

{{< youtube kzUm5T5RzwE >}}