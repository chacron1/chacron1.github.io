+++
title = 'Solo developing a game for Bigmode Game Jam 2026 - Devlog #1'
date = '2026-02-01'
draft = false
tags = ['blog', 'development', 'post', 'godot', 'gamejam', 'gamedev']
type = 'blog'
listIcon = "/writing.png"
teaser = "Taking it slow"
+++

---

## Introduction

When I decided to participate in this Game Jam, I set myself a list of goals that I'd like to meet during the development. I am not here to win anything. My list of goals is kinda different.  
I want to get out of my *comfort zone*. I want to show raw, unfinished material which would normally be deemed "unworthy" by my 'standards' (standards my ass—they've been holding me back since forever).  
I want to connect with people more. I want to blog, I want to talk with folks on Discord — I want to join in on all the fun stuff that I feel I've been missing out on as an 'introvert'.  
So without further ado: I present to you my first blog post.

## The theme: 'Slick'

Thursday, January 29, 2026—where I live, the Game Jam started at 4:00 PM, and with it, a theme was unveiled:

**SLICK**

As the Game Jam spans over a week, I've decided to take it easy and start by writing out some ideas.  
But first - what does **SLICK** actually mean?  
Initially, I thought that slickness is what game developers like to call "juice" (I believe the term was originally popularized with an amazing talk by Martin Jonasson & Petri Purho: [Juice it or lose it](https://www.youtube.com/watch?v=Fy0aCDmgnxg)). So basically making your game fill less stiff and more polished.
I also think that "slick" is a term which Dunkey uses a lot when developers are adding some unexpected flair.

E.g. Koopas dancing to the music in **New Super Mario Bros. Wii**.
![KoopaDance](/koopa-dance.gif)

* GIF pulled from: <https://makeagif.com/gif/koopa-bah-bah-dance-a7lWt0>*

Slick also could refer to a not-so-trustworthy dude.  
Another theme interpretation, and the one I went with is **Slick Moves**. This is also the one I see the most on Bigmode Discord. (skateboarding, snowboarding, cars doing crazy moves etc.)

## Slick moves and boomboxes -> Idea is born

So after a lengthy brainstorming session, I've come up with a game idea:

**A turn-based rhythm game in which you battle evil boomboxes by executing slick dance combos**

![Initial Sketch](/bigmode_initial_sketch.jpg)

* Initial sketch made in Procreate.

I know it sounds absurd, but in my mind, it fits the theme perfectly.
First of all, rhythm games have a lot of natural slickness to them.
The gameplay is tightly connected to the sound, which adds a layer of polish to the game by default. Dancing is just doing slick moves to the rhythm.  
Ok, ok - but what about the turn-based part?
Ideally the battles would happen by executing combos to the rhythm Patapon style.
For example by pressing **left**, **left**, **up**, **right**, you'd activate an attack combo.
By pressing **up**, **up**, **up**, **right**, you'd activate a healing move.
And so on.
In response to your attacks, the boombox will do its move and give you your turn back.

## How do you even start making a rhythm game?

To be honest, I've never made a rhythm game before, so I did lots of research and found some really good insights on the internet. I've decided to put it all together here-maybe it'll inspire someone else to dive into this rabbit hole of a subject.

YouTube videos:

* [A $16 One-Button Rhythm Game - Premium Game Design With Extreme Constraints - Hafiz Azman](https://www.youtube.com/watch?v=MJEH3vRGi7U)
* [I want to make a rhythm game but I don't know how - lislis](https://www.youtube.com/watch?v=MJEH3vRGi7U)
* [Complete Godot Rhythm Game Tutorial - LegionGames](https://www.youtube.com/watch?v=_FRiPPbJsFQ)

Blog posts / Docs:

* [Sync the gameplay with audio and music - Godot Docs](https://docs.godotengine.org/en/stable/tutorials/audio/sync_with_audio.html)
* [How To Make a Rhythm Game - a quick and dirty guide to setting up your project - Hafiz Azman](https://fizzd.me/posts/how-to-make-a-rhythm-game-a-quick-and-dirty-guide-to-setting-up-your-project)
* [AudioStreamSynchronized - Godot Docs](https://docs.godotengine.org/en/stable/classes/class_audiostreamsynchronized.html)

Open Source Github Repositories:

* [Example Rhythm Game - Godot official demo projects](https://github.com/godotengine/godot-demo-projects/tree/master/audio/rhythm_game)
* [Godot Midi Plugin - nlaha](https://github.com/nlaha/godot-midi)

I especially recommend content made by Hafiz Azman. He's one of Rhythm Doctor creators, and his input here is top-notch.
Also, a ready-made *[Conductor](https://github.com/godotengine/godot-demo-projects/blob/master/audio/rhythm_game/game_state/conductor.gd)* class that follows his teachings is available in the Godot demo projects repository.

## What I've got so far

I started by creating a short looping theme so I could test the rhythm part.
I feel that 110 BPM is a good starting point so I've set the tempo and created a POC in FL Studio using Massive 2 as a lead bass synth.

{{< audio src="/boombox-ost.wav" >}}
.

Next I made an ugly-looking boombox model in Blender.

![Boombox in Blender](/blender-boombox.png)

Then I watched some scenes from Step Up 3 to find some interesting freezes as an inspiration for the in-game slick moves:

![StepUp3](/stepup3-moose.jpg)

* Screenshot from: <https://www.youtube.com/watch?v=8BvnTjENv4g>*

![StepUp3](/stepup3-drawing.jpg)

* Drawing over the poses in Pixaxi on iPad

![StepUp3](/stepup3-poses.jpg)

* Selected poses

Having everything ready for testing I've made a simple playground scene in Godot in which I've set everything up without pressuring myself to structure the code.
Using curves I've animated the boombox inspired by the bouncing Toyota Yaris videos I've been seeing on YouTube.

Here's how it's looking right now:

{{< video src="/boombox-video-01.webm" >}}

You can check out the project on its GitHub repository here: <https://github.com/chacron1/boombox>

---
