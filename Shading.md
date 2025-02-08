---
date: 2025-02-04
tags:
  - "#computer_graphics"
---
# Advanced Shading

Simulate properties of light and material to get more realistic results.

**Materials:** Properties of a surface.
- Colour
- Texture
- Bumpiness
- Reflections
- Material vs Plastic
- Etc.

**Light:** Source that emits
- Size (usually a point) -> directional
- Colour

```ad-tip
Consider things like where the shadow would be casted from the light, how the texture and material reacts with it, how reflections react with it, etc.
```

**Viewer:** (eye) points to the person, camera. Think your perspective in a FPS game.

# Gooch Shading 

Gooch shading is a non-photo-realistic rendering technique for shading objects. It is also know as "cool to warm" shading, and is widely used in technical illustration. 

Gooch shading defines an additional two colours in conjunction with the original model colour:
- Warm colour (such as yellow)
- Cool colour (such as blue)

The warm colour indicates surfaces that are facing toward the light source, while the cool colour indicates surfaces facing away.

This allows shading to occur only in mid-tones so that edge lines and highlights remain visually prominent.

# Specular Light

A specular highlight is the bright spot of light that appears on shiny objects when illuminated.

Specular highlights are important in 3D computer graphics, as they provide a strong visual cue for the shape of an object and its location with respect to light sources in the scene.

# Not Photorealistic Images

A "not photorealistic image" refers to a visual representation that does not attempt to look exactly like a photograph, meaning it deliberately deviates from replicating reality with precise detail and instead embraces artistic styles like cartoonish, illustrative, etc.

# Radiosity

Radiosity is a computer graphics technique that calculates how light reflects and spreads between surfaces in a scene.

It's a global illumination algorithm that considers both direct and indirect light.

```ad-tip

```

## How Radiosity Works?

Radiosity breaks a scene into many small elements, called mesh elements.

It calculates how much light energy is transferred between each element.

It uses the form factor equation to describe the fraction of energy transferred between each pair of elements.

It stores the final grandiosity value for each element.

## Why it's useful?

Radiosity produces realistic images that capture global illumination effects.

It's viewpoint independent, which means it's useful for all viewpoints.

```ad-help
All this means is that no matter how you look at it, it's shaded correctly, from all viewpoints.
```

There are two techniques of radiosity.
- Progressive refinement: A technique that displays immediate visual results that improve in accuracy over time.
- Stochastic relaxation radiosity (SRR): AN algorithm that forms the basis of commercial radiosity systems.

# Soft Shadow vs Hard Shadow

A soft shadow is a diffused shadow with blurred edges, creating a smooth transition between light and dark areas.

While a hard shadow (or cast shadow) has sharp, well-defined edges, resulting in a distinct line between the illuminated and shadowed parts of an object.

Essentially, soft shadows appear more gentle  and less pronounced than hard shadows, which are bold and sharp.

Soft shadows are more like plane changes away from the light source so they're slightly darker, they're still being hit by a lot of light, but it might not be directly from the light source.

The closer the light source, the harder the shadows will be.

# Ray Tracer

Ray tracing is a computer graphics technique that simulates light in a 3D scene to create realistic images.

How it works:
- A virtual camera shoots rays of light into a 3D scene.
- Rays travel through the scene, interacting with objects.
- The ray tracer collects information about the objects, such as their colour, texture, and lighting.
- The ray tracer combines the information to create the final colour and illumination for each pixel.
- The pixels are displayed on the screen.

## What Ray Tracer can do?

**Simulate optical effects:** Ray tracing can simulate reflection, refraction, shadows, and more.

**Create realistic images:** Ray tracing can create images that look *almost* real.

**Create immersive sound designs:** Ray tracing can simulate sound waves to create realistic reverberation and echoes.

**Create real-time graphics:** Ray tracing can be used to create real-time graphics for video games, film, and television.

Ray tracing can be computationally intensive, especially for 4k resolution games.

# Phong Lighting

Phong lighting, also known as the Phong reflection model, is a widely used method in computer graphics to calculate how light interacts with a surface by combining three components:
- Ambient light (constant background illumination)
- Diffuse light (directional light from source)
- Specular light (bright highlights on shiny surfaces)

Creating a more realistic appearance on 3D objects based on the viewing angle and material properties;

It is named after its creator, Bui Tuong Phong in 1975.

# Gouraud Shading

We calculate colour at vertices.

As we fill the triangle we interpolate the colour smoothly across the face.

1. Calculate shading at triangle vertices.
2. Blend results using barycentric coordinates.

Old, simple, limited. banding limits of bit depth.

# Phong Shading
*as opposed to Phong Lighting*

Calculate normals N at vertices.

Interpolate normals across the face.
- Use this N to calculate each pixel.

```ad-question
Do you think Phong Shading would be good for pool balls?
```

