---
date: 2024-10-03
tags:
  - status/scratch📝
  - status/boat🚤
publish: false
---
# houdini


## Nodes
Nodes are operators. There are a few categories of these.:
- [[OBJ (object, transforms)]]
- [[SOP (surface, geometry)]]
- [[DOP (dynamics, simulation)]]
- [[LOP (lookdev, USD)]]
- [[VOP (vex, shader building)]]
- [[COP (composite, images)]]
- TOP (task, PDG)
- ROP (render, outputs)
- CHOP (channel, motion)


## Nested Network Types

There are two main levels- Object and Stage
At the Object level, every OBJ contains a SOP network. 
At the Stage level, you could put a LOP that references a USD (something on disk), or one that has a SOP network in it, or a LOP with a VOP network inside.

It's a sort of Russian nesting dolls situation. At any level, you always have the ability to put another network inside where you're at. (I guess you can think of this as compound nodes in Resolve color, or as compound clips)

Many tools in Houdini are digital assets with nesting inside. Tools often have multiple layers.



## Other Terms 

Mantra
This is the legacy render engine.

Solaris
Lookdev/USD universal scene description.

Karma
Render USD. This allows the integration of other renderers. 
CPU traditional renderer. XPU is a hybrid that tries to also use GPU.

KineFX
Retargeting and motion editing. Rigging and animation. This is the direction they are going.

MotionFX 
Tied to animation. CHOPS. Layering procedural solutions over existing channels.

FLIP
Fluid solver.

Vellum
Cloth, soft body, fluids, grains, lots of things.
Fast solver.

PyroFX
Fire and smoke.

Bullet
Rigid body dynamics.

POP
Particles. Found in DOPS now.

[[HDA (Houdini Digital Asset)]]



## Viewers

Viewport
- Grid here is in meters
Parameters
Nodes
Geometry Spreadsheet
- Raw data of what you're looking at
	- Positions of geometry
	- Attributes list


