---
tags:
  - computer_graphics
date: 2025-01-09
---
# RGB Colour Model

Monitors today can't produce all the colours.

Actually can't produce all the wavelength of visible light
- They fake it

Monitors produce RGB => Sending signals to the cones, to emulate a real wavelength.

# Frame Buffer

A frame buffer is a block of memory in a computer or device used to store image data that is displayed on a screen. It acts as a digital canvas where pixel information (colour, depth, and other attributes) is stored for rendering an image frame.

**Make a diagram here from the note** 

Constantly push the data in the Frame Buffer to the display in some standard frequency. 

# Visual Pipeline of Frame Buffer

**CPU**: Sends rendering commands to the GPU.

**GPU**: Processes the scene and outputs pixel data.

**Frame Buffer**: Stores the pixel data for the entire frame.

**Display Hardware**: Reads the frame buffer and sends the data to the monitor.

Input (scene Data) -> GPU (rendering) -> Frame Buffer -> Display Hardware -> Screen
- This process repeats for each frame to create smooth, real-time images on the screen.

# Scan Line

It is a horizontal line on display
- Old cathode RayTube (CRT) monitors, hardware was designed to draw line by line a horizontal first. 

To compensate for vertical colour bleed, lines were spaced out.

Modern Systems copy from VRAM to memory inside a monitor.
- Then monitor decides how to draw. 
- Nowadays, monitors have their own hardware to manage graphics on screen.

```ad-danger
Problem: What if you are in the process of updating your Frame Buffer(VRAM), the monitor gets a new image? This problem is called Tearing.
```

# How to fix Tearing?

The standard approach to fix tearing is called Double buffering.
- You work on your image into another buffer. (Main memory / VRAM)
- When image is ready, you copy the whole image over at once as fast as you can before monitor grabbing it in the middle.
- This is called a BLIT (Block Image Transfer)
	- By using a BLITing, we can reduce the possibility of tearing.
	- In hardware can guarantee no tearing.
	- Can slow down the systems performance.

Double Buffering also requires double memory.

Double memory copy time. (From your buffer to the frame buffer and from frame buffer to the monitor).
**^ Make a diagram of that**

By increasing copy time will lead to loosen it's efficiency.

Game consoles have dedicated hardware to control tearing, while games on PC sometime struggle with tearing. 

Modern Solutions are,

Higher Refresh Rate
- Suppose, instead of 60fps, if prefer 120 fps, the tearing you see will be minimised.

Brand specific emulations of "wait for vertical retrace"
- Vsync
- Free-symc
- G-sync

# Rasterization

The process of going from data in some format to specific pixel values. 

# Vector Graphics vs Raster Graphics

Vector graphics are computer-generated images made up of geometric shapes, such as lines, points, curves, and polygons, that are defined on a Cartesian plane. Vector graphics are different from raster images, which are made up of colourised pixels, in that vector graphics can be scaled to any size without losing quality or resolution.

In vector graphics --- define shapes as series of draw commands.
- Mathematically defined.
- Can scale up "Indefinitely", "Infinite" precision.
- File formats: svg, eps, pdf, ai, emf
- Much of vector graphics stuff do in software -> keep vector as long as possible.

Not all displays are raster. 
- CRT vector display
- Plotters

Many components stay in vector form as long as possible to maximise flexibility. 

```ad-tip
Flexibility in this circumstance refers to retaining the information for as long as possible.
```

# Advantages of Vector Graphics

Vector graphics can be resized to any size without losing quality or resolution. This makes them ideal for logos, icons, diagrams, charts, and illustrations that need smooth, crisp edges.

Vector graphics are smaller than bitmap images because they don't store data about each pixel.

Vector graphics have "infinite" resolution.

Vector graphics are easy to manipulate and reuse.
Vector graphics are more versatile than raster files because they can be adjusted in size without losing resolution.

# Disadvantages of Vector Graphics

They can't handle complex images, such as photographs.

They require specific software to view, so they can't be opened on a simple browser or mobile device.

# Raster Data

Each pixel on a raster is represented by bits.
- 1 bit(s) per pixel -> on/off
- 4bpp -> $2^{4}$ => 16 values
- 8bpp -> $2^{8}$ => 256 values
- These systems used techniques called a colour palette.

Palette - A look up table that indexes raster pixel values => RGB intensities

CGA - 4
EGA - 16 
These above are hardware for monitors that contain preloaded colours.

VGA - 256 - programmable palette

The good thing about palette was low pixel bit depth -> less memory -> faster, because of moving less memory.
- Less flexible
	- 1bpp
	- 4bpp
	- 8bpp
	- 12 bits per pixel -> R(4 bits) G(4 bits) B(4 bits)
	- 24bpp
# Palette

A palette is a group of colours that are used to describe an image. In a oaletted image, each pixel is assigned an index that points to a color in the palette, instead of storing the actual RGB values for each pixel. This makes the resulting image smaller than it would be if each pixel stored its own RGB values. 

RGB and CMYK are the two main color models used for designs. RGB colors are used for on-screen viewing. RGV is an additive colour model, meaning it adds red, green, and blue light together to create different colours.

# Different Bits per pixels

12, 24 are not good numbers for computer scientists, because these are no multiples of 9. 
- 24 bit colour on 32 bit machine (not following byte/word boundary, we are losing bytes)

16, 32 doesn't bother because nothing is left over. In 32 bit colour model we use RGBA (8 bits each), A refers to alpha (which refers to transparency).