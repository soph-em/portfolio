---
title: PICO-8 Llama Game - Day 4
description: Fixing the spit, adding enemies.
date: 2023-07-10
categories:
  - gamedev
  - pico8
  - llamagame
published: true
author: '/pfp.jpg'
headerimage: '/day4.png'
---

I decided that firstly today I'd resolve why the spit doesn't move while the llama is moving. I realised it was because it was the same speed as the llama, so matching it, and just so long as I increase my 'dx' from 1 it functions as intended:

```
function shootspit()
    add(spits, {x=llama.x, y=llama.y, dx=llama.left and -2 or 2})
end
```

I brainstormed a bit more of my game features after this, I didn't really go into this game with a plan. I've started to get a good idea of the direction to go in now. I'll have enemies that get killed during collision with the spits, but can also attack the llama back. Maybe I'll have power-ups for the llama to increase it's speed/spits/power. I'll probably include levels or a points based system.
Since I have the most clear view on the enemies, I decided that they'll be my next focus. I googled 'llama enemies' at first and according to Denver Zoo "_The most common predators of llamas are coyotes, mountain lions, and ocelots._"

I settled on a starting place of foxes, lions, tigers, zombies, and ghosts. I'll want them to have different behaviours and mechanics with varying difficulty for the levels. I spent the rest of my evening drawing the enemy sprites, facing both directions. I also drew some heart sprites and displayed them at the top of the screen, but didn't have any functionality tied to it. The next task will be to add some enemies to the map, make them move randomly, and make them take damage, in addition to making the llama health functional.
