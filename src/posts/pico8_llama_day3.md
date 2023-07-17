---
title: PICO-8 Llama Game - Day 3
description: Getting llama spitting working
date: 2023-07-09
categories:
  - gamedev
  - pico8
  - llamagame
published: true
author: '/pfp.jpg'
headerimage: '/day3.png'
---

I forgot to Ctrl + S when closing my code last night which meant that I had to re-write everything I wrote yesterday, though fortunately it didn't take too long. If there was one thing I could change about Pico8, it would be a save reminder and/or a warning on shut-down.

Worked on the animation again today. I fixed the animation bug and now use an index/counter and when the index reaches the length of the array of sprites that animating through, it stops. I find it interesting how Lua starts indexing arrays at 1, not 0, it's tripped me up a couple of times so far. My code looked something like this:

```
llama = {x=100, y=100, s=16}
spitleft = {16, 17, 18, 16}
index = 1
animation_speed = 0.1
animation_timer = 0

function _update()
  if btn(➡️) then
    llama.x = llama.x + 1
    llama.s = 32
  end
  if btn(⬅️) then
    llama.x = llama.x - 1
    llama.s = 16
  end
  if btn(⬇️) then
    llama.y = llama.y + 1
  end
  if btn(⬆️) then
    llama.y = llama.y - 1
  end
  if btnp(❎) then
    spit()
  end
end

function spit()
  llama.s = spitleft[index]

  index = index + 1
  if index > #spitleft then
    index = 1
  end
end

function _draw()
  cls()
  map(0, 0, 0, 0, 128, 32)
  spr(llama.s, llama.x, llama.y)
end
```

After this I still had a little time, so I added for the llama to also spit when facing right, and the spit travels in the right direction. I learned about 'dx' or 'change in position' today to be able to alter the direction and speed of the spit. At first I had a funny issue that if my llama changed direction, that every spit changed direction with it, but fixed that one quite quickly. By the end of the day my code looked something like this:

```llama = {x=100, y=100, s=16, animating=false, left=true}
spitleft = {16, 17, 18, 16}
spitright = {32, 33, 34, 32}
index = 0
animation_speed = 0.5
animation_timer = 0
spits = {}

function _update()
    if btn(➡️) then
        llama.x = llama.x + 1
        llama.left = false
        llama.s = 32
    end
    if btn(⬅️) then
        llama.x = llama.x - 1
        llama.left = true
        llama.s = 16
    end
    if btn(⬇️) then
        llama.y = llama.y + 1
    end
    if btn(⬆️) then
        llama.y = llama.y - 1
    end
    if btnp(❎) then
        spit()
    end

    for i = #spits, 1, -1 do
        local llamaspit = spits[i]
        llamaspit.x = llamaspit.x + llamaspit.dx

        if llamaspit.x > 128 then
            del(spits, i)
        end
    end

    if llama.animating then
        if llama.left then
            llama.s = spitleft[index]
        else
            llama.s = spitright[index]
        end

        index = index + 1
        if index > #spitleft then
            index = 1
            if llama.left then
                llama.s = 16
            else
                llama.s = 32
            end
            llama.animating = false
        end
    end
end

function spit()
    llama.animating = true
    shootspit()
end

function shootspit()
    add(spits, {x=llama.x, y=llama.y, dx=llama.left and -1 or 1})
end

function _init()
end

function _draw()
    cls()
    map(0, 0, 0, 0, 128, 32)
    spr(llama.s, llama.x, llama.y)
    for llamaspit in all(spits) do
        spr(3, llamaspit.x, llamaspit.y)
    end
end
```

There's an issue that the spit isn't moving while the llama is, but it's late enough that it's now a tomorrow problem.
