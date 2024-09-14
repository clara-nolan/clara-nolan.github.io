---
title: 'TBD'
description: 'A phsyically based path tracer'
image:
    url: '/minecraft.png'
    alt: 'A rendered image of the Cornell Box'
worksImage1:
    url: '/customImage1.png'
    alt: 'first image of your project.'
stack: OpenGL, GLSL, C++, Qt
website: https://astro-milky-way.netlify.app/
---

In this project, my primary goal is to implement the Li_Full Integrator, a new light integrator designed to handle both direct and global illumination at each ray intersection. This development aims to minimize noise and enhance brightness in the rendered images. I have introduced a function to calculate direct lighting using multiple importance sampling, specifically tailored for interactions with diffuse and microfacet surfaces. Additionally, I have generated new BSDF-based rays to explore global illumination effects further and updated the color accumulation based on the materials each ray encounters. To add another layer of realism, especially in scenes devoid of direct light sources, I have enabled sampling from the environment map. 

TLDR; a PBR path tracer that handles global illumination, diffuse, specular, and mirror to translucent material.
