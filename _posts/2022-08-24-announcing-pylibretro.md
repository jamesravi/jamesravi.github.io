---
layout: post
title: Announcing pylibretro
tags:
  - post
---

![]({{ site.baseurl }}/images/pylibretro-i-made-something.gif)

To be honest, the image above is a bit misleading. I have **not** created a Python clone of the game [2048](https://en.wikipedia.org/wiki/2048_(video_game)) (which you might be aware of). **However**, I have created [a Python library](https://github.com/jamesravi/pylibretro) that is able to run Libretro cores such as the [2048 core](https://github.com/libretro/libretro-2048)!

I should probably explain that [Libretro is an API ](https://www.libretro.com/index.php/api/)designed by the [RetroArch](https://en.wikipedia.org/wiki/RetroArch) team that allows loading emulators (and even certain games using the API, [you can see a list here](https://en.wikipedia.org/wiki/RetroArch#Supported_systems)) using a standardized API. It’s wonderful because if I had wanted to build a Python interface to an emulator without it I would have had to hack in several hundreds lines of C (or C++) code and would have only been able to control that particular emulator.[^1] 

Instead, via Libretro this library can be used to load many emulators easily, potentially opening the door for web-based emulation (like this defunct [Twitch Plays style JavaScript project](https://github.com/rauchg/weplay)) or reinforcement learning applications.[^2]

AND LOOK IT WORKS:

![](https://raw.githubusercontent.com/jamesravi/pylibretro/master/2048example.gif)

Of course, it should say it works _to a degree_. There’s much to be done, it sometimes randomly freezes, other cores result in segfaults (probably need to test a few more other than 2048), lots of functionality and callbacks are missing etc. Nevertheless, the [source code is available on GitHub](https://github.com/jamesravi/pylibretro) and you can [install it from PyPI](https://pypi.org/project/pylibretro/). It’s also my first time creating a Python package and I thoroughly enjoyed learning and using [poetry](https://python-poetry.org/) (which was recommended by several people online) to do so.

[^1]:
     Also, that’s assuming if I had managed to do so - given I’m less experienced with C, it probably would have been near impossible.

[^2]:
     I should mention, OpenAI has beaten me to the punch and obviously done so better with [Gym Retro](https://github.com/openai/retro), but it seems to [only support a limited number of consoles](https://github.com/openai/retro#emulated-systems), and as [adding support for new emulators seems to be a struggle](https://github.com/openai/retro/issues/169), I felt prompted to attempt to make this library.

