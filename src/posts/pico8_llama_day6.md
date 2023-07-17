---
title: PICO-8 Llama Game - Day 6
description: Enemies taking damage and dying
date: 2023-07-17
categories:
  - gamedev
  - pico8
  - llamagame
published: true
author: '/pfp.jpg'
headerimage: '/day7.png'
---

I had a day off work today, and not too many commitments, so I had a bit more time than usual to work on this today. I'd started working on checking if the foxes were being hit by the spits yesterday, but then my day got a lot busier so I couldn't put any more time into it, it couldn't run because of a syntax error.

Otherwise, I spent some time over the weekend looking at options to make a small console that could run this game, probably a handheld Raspberry Pi. We've ordered a few parts and we're both excited to learn through trial and error.

My first task today was to make the code run, from the error message I had, I was missing an `end` somewhere. My code had turned into a bit of a mess with one of my functions being far too long, and no longer what it was named, and some poorly named variables. I took the chance to do a re-work and split the functions up, rename things, and try to make sure everything was closed.

After I fixed this, I got the interactions working, and animated the foxes flashing when they get hit to show they've taken damage, but the animation for this wasn't working. As soon as one was hit there would be a few second delay then they'd both alternate between flashing. I figured out eventually that my collision logic/mathematics was wrong, and once I'd fixed that the collisions worked as expected.

I then moved on to making a fox 'die' after being hit three times. It took a few debugging print statements, but I also got that working before I wrapped up for the day.

Today I started coding in VS Code then going back to PICO-8 and pressing CTRL + R to run it, I feel like I can write code in the PICO-8 console, but struggle a lot more with debugging or reading code in there.

I've started trying to push more frequently to GitHub to have a better back-up, my code for today is [here](https://github.com/soph-em/llamasurvivors/blob/b42632e33a86c3985ec8125089e1cf3aad8abc83/game.p8)
