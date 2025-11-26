# Rock Throw Handover

**Rock Throw Niagara System and Rock Throw Animations**

**Callum Wade** **2404781@students.ucreative.ac.uk** 

**Client: Cameron Gildea** **Project: "Name still to be decided"**

**Delivery Date:**

**Version: 1.0**


## Asset Overview
When the right mouse button is held, a charge up animation will play and then change to a charging animation which continues to loop till the button is released. While the attack is being charged, a crack decal spawns behind the player and debris will start being thrown in the air from the crack while the camera also starts shaking. When the player releases the right mouse button, the debris stops spawning, the camera stops shaking, and the throw animation plays while a niagara system is spawned and shot forward in front of the player.

## Integration Guide



## Customization Guide

### Rock Throw Niagara System
The exposed parameters on the rock throw niagara system allows easy control over the size of the mesh rendered, the lifetime, amount of rocks spawned, the rock spread and the velocity of the rocks fired.

### Crack Debris 
Within the crack debris, the exposed parameters allows easy adjustments to the lifetime, size and spawn rate of both the ground debris and the air debris as well as the spawn radius of both types.

### Camera Shake
The camera shake can be adjusted in the camera shake blueprint. The blend in time can be changed to increase/decrease how fast the shaking intensifies.

## Technical Documentation

### Rock Throw Niagara System
The rock throw niagara system uses a mesh renderer to spawn rock models that spawn and fire in a cone shape using add velocity (In Cone). Spawn burst instantaneous is used to spawn all the particles in one go so that it acts like pellets being shot and initialize particle is used to control the lifetime and size of the rocks fired. 

