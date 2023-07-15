---
title: PICO-8 Llama Game - Day 1
description: Where I started.
date: 2023-07-07
categories:
  - gamedev
  - pico8
  - llamagame
published: true
author: '/pfp.jpg'
headerimage: '/day1.png'
---

<!-- ![Text](image.webp) -->

When I first launched up PICO-8 I had wanted to make a bunny game. I have a pet rabbit called Zeus who is a 'ruby eye white' - white coat and ruby eyes.

![Zeus](/Zeus.jpg)

It turns out though that I can't draw rabbits, so I figured my sprite decided it was a llama and I'm now making a llama game.

![Llama](/day0.png)

After I drew my sprite I drew a basic background, and added in some daisies to the background, maybe eventually the llama will eat them or something similar to increase health?

At the end of day one, I had a map showing, with my llama sprite on screen and able to move around. Below is the code to get this initial functionality.

```llama = {x=100, y=100}
    function _update()
        if (btn(➡️)) llama.x = llama.x+=1
        if (btn(⬅️)) llama.x = llama.x-=1
        if (btn(⬇️)) llama.y = llama.y+=1
        if (btn(⬆️)) llama.y = llama.y-=1
	end
    function make_llama(x,y)
        return {
            x=x, y=y, n=2
        }
        end
    function _draw()
        cls()
        map(0,0,0,0,128,32)
        spr(llama.s, llama.x, llama.y)
    end
```

It took me a little trial and error. I only have about an hour or two daily max to work on this, so would have liked to get more done today, but at the same time I loved having something I could 'use' within just a couple of hours. Tomorrow I'm hoping to make a second llama sprite facing right, and have it face that way when moving right.
