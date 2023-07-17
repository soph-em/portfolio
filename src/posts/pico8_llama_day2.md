---
title: PICO-8 Llama Game - Day 2
description: Getting started with animating sprites.
date: 2023-07-08
categories:
  - gamedev
  - pico8
  - llamagame
published: true
author: '/pfp.jpg'
headerimage: '/day2.png'
---

Today I decided that next I'd make the sprite face right when moving right, then back to facing left when moving left. This was quite a simple change with a conditional added when pressing either ⬅️ or ➡️ keys.

```if btn(➡️) then
		llama.x = llama.x+1
		llama.s=32
	end
	if btn(⬅️) then
		llama.x = llama.x-1
		llama.s=16
    end
```

I've not added any changes for up or down yet, and I'm not sure if I will.

Next, I decided to make the llama spit when pressing the ❎ key. By the time I got to the end of the evening, I managed to get it to animate when I pressed ❎, but not for it to spit. The animation was buggy with it going through the wrong set of sprites and often ending on the wrong one, or no sprite at all. Sadly, I ran out of time to fix it before it got too late. Pictured in the header is one of the animated sprites it often got stuck on.
