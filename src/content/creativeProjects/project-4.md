---
title: 'TBD'
description: 'A collection of post-processing effects and shaders'
image:
    url: '/minecraft.png'
    alt: 'A cube made out obsidian in a well lit room.'
worksImage1:
    url: '/multi.png'
    alt: 'A reflective metal sphere.'
stack: GLSL, C++, Qt
website: https://astro-milky-way.netlify.app/
---

The first shader employs a dynamic blurring effect by averaging sampled colors from a primary texture. It achieves this by iterating over a set number of points (25 in this case), and for each point, it calculates an angle that depends on both the iteration index and a uniform time variable, u_Time. This results in a swirling motion as time progresses. The offsets for sampling are determined by the sine and cosine of the calculated angle, effectively creating a circular sampling pattern around the current texture coordinate, fs_UV. The color values from these samples are then accumulated and averaged to produce a smooth, motion-blur-like effect in the rendered texture. The final color output is a normalized sum of these colors, giving the texture a dynamic, fluid appearance as if it is constantly in gentle motion.

The second shader I have created involves a displacement effect based on the color information from a secondary texture. This shader begins by fetching a color from the secondary texture, which it then uses to perturb the texture coordinates of the main rendering texture. The displacement scale is controlled by a constant, allowing for subtle to pronounced effects based on the red and green channels of the secondary texture's current pixel. Additionally, I extract the red channel from the secondary texture to simulate a lighting effect, which is then added to the main texture's sampled color. This results in an image where both texture and perceived lighting dynamically change based on the secondary texture's content, introducing a complex interaction between two different textures that affects both color and apparent illumination.