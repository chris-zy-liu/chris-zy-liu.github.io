---
title: "BSPWM Picture in Picture Video Player Setup"
layout: post
categories: Essays
---

Sometimes the limitations of a window manager becomes apparent, lacking many features that a desktop environment would have. One feature that I find useful in other desktop environments is an always on screen video player, so that the content we are watching is always visible.<!-- excerpt-end -->

This video player need to have the following features:
- Follow to other workspaces
- Be a floating window
- Be resizeable
- Always be at full transparency

Luckily for us, most modern video players have a "Picture in Picture" mode, where the content being played is moved to a smaller stand alone window. In most desktop environments, this would solve our needs. However, this only allows BSPWM to spawn in a tiled window that looks rather ugly.

We can achieve the features we need by using BSPWM and picom rules.

The simple line
```bash
bspc rule -a '*:*:Picture-in-Picture' follow=false state=floating sticky=on
```
can take care of most of our needs, the window now spawns as a floating window and always follow us to other workspaces. However, if your picom config creates a transparency effect for windows that are not in focus, this could cause the player to lose its color saturation.

We can remedy this with
```bash
opacity-rule = [
	"100: name = 'Picture-in-Picture'",
	...
];
```
Now our player will remain at full opacity even if it is not in focus!
