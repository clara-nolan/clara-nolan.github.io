---
title: 'Realtime Renderer'
description: 'An Unreal inspired realtime renderer system able to handle subsurface scattering, roughness, and metallic sliders'
image:
    url: '/obsidian.png'
    alt: 'A cube made out obsidian in a well lit room.'
worksImage1:
    url: '/metal.png'
    alt: 'A reflective metal sphere.'
worksImage2:
    url: '/gun.png'
    alt: 'A pistol in a forest environment'
stack: GLSL, C++, Qt
website: https://astro-milky-way.netlify.app/
---

In this project, I have implemented a physically-based shader with environment mapping, focusing on the integration of pre-computed irradiance into the plastic-metallic BRDF. I have developed shaders in GLSL, handling varying degrees of roughness and metallicness, and integrating different environmental conditions into the rendering process. For the direct lighting component, I have crafted functions that utilize multiple importance sampling to enhance the realism in material representation, particularly for diffuse and microfacet surfaces. I've also enabled environment map sampling, which adds depth and realism to scenes that lack direct light sources. For the global illumination aspect, I've employed new BSDF-based rays to simulate realistic light interaction and update color accumulation effectively. 