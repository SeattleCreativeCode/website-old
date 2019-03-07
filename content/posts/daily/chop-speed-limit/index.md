+++
date = "2019-03-05T00:00:00+0800"
title = "CHOPS: Speed + Limit"
summary = "TouchDdesigner Deep Dive Day One, CHOPS, Speed + Limit"
authors = ["stainless"]
topics = ["TouchDesigner"]
tags = ["chops", "chop", "speed", "limit", "touchdesigner", "basics", "learning"]

[[resources]]
  src = "speedlimit.png"
  title = "Speed & Limit Chops"
  [resource.params]
    description = "A screenshot of touchdesigner with a network that is LFO into speed into math into limit into circle"
+++
Due to traveling, I'm a bit behind on my daily posts and explorations, so I decided to combine `Speed` and `Limit` together because I felt like both are easy enough to grasp that it wouldn't do a disservice to do them together.

`Speed` takes a rate, and transforms it into the cumulative value by apply the rate to the value. Think of it as a sum over time. It's an application of Newton's equations. If you chain two `Speed` chops, then you have acceleration as an input, and position as the output. This is useful for modeling real world movement like gravity, not that I did that.

`Limit` allows you to force a channel to be between two values with a number of different options handle values that are outside of the limit. I used the `clamp` option which replaces any value above the upper limit to the upper limit, and same for the lower limit.

{{< youtube tKmFLQI8t6k >}}