---
title: 'ASCII Filter'
description: 'Use your camera to make ASCII Art'
image:
    url: '/ascii1.png'
    alt: 'A depiction of a pink-ish red sunset'
worksImage1:
    url: '/ascii2.png'
    alt: 'Hilly voxel environment'
stack: HTML, CSS, JavaScript
website: https://editor.p5js.org/kunstpleb/sketches/qfGKWfeDw
---


In my version of Daniel Shiffman's ASCII art project from The Coding Train, I've introduced several modifications to give it a unique spin, transforming the ASCII art into a Matrix-style "rain" effect. 

Firstly, I adjusted the ASCII character set and the way characters are mapped from the video input. While the original project used a fixed set of characters to represent varying shades of brightness, I've maintained this concept but added a twist by allowing the characters to change over time. This simulates the iconic digital rain from the Matrix films, where text continuously flows down the screen.

To achieve this, I introduced a time-based variable that modifies which character is selected from the density string. Using millis() to get the running time since the program started, I created a time offset that adjusts the character index cyclically. This means as time progresses, the characters displayed for the same pixel brightness level change, creating an effect of falling rain.