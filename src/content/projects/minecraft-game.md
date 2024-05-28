---
title: 'Voxel-Based Game'
description: 'A recreation of Minecraft using C++'
image:
    url: '/minecraft.png'
    alt: 'A depiction of a pink-ish red sunset'
worksImage1:
    url: '/m1.png'
    alt: 'Hilly voxel environment'
worksImage2:
    url: '/m2.png'
    alt: 'Pink clouds surrounding sun'
stack: C++, GLSL, Qt
website: https://astro-milky-way.netlify.app/
---

I implemented player physics predominantly using gridmarching to check for blocks in order to determine where to destroy or create. In order to implement caves, I used a mix function to layer 3D perlin noise with 3D simplex noise to create tunnels. Additionally,  I implemented the Day and Night cycle by adding my own palletes for sunrise, morning, midday, sunset, and night. I then created a const variable that represented 10,000 ticks, and this variable allowed me to create 5 different phases throughout the day. I based my sun movement off of each interval along with using sin and cos functions. Lastly, I created the post-processing shaders that appear on screen when the user is in lava or water by creating a switch case that would be activated when a boolean was true or false for lava or water respectively. I layered FBM functions along with 2D noise functions to create these effects. 