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
<br>

![Rock Throw NS Parameters](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%207-10/Images/Handovers/Rock%20Throw/Rock%20Throw%20Paramaters.png)

### Crack Debris 
Within the crack debris, the exposed parameters allows easy adjustments to the lifetime, size and spawn rate of both the ground debris and the air debris as well as the spawn radius of both types.
<br>

![Debris Parameters](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%207-10/Images/Handovers/Rock%20Throw/Debris%20Parameters.png)

### Camera Shake
The camera shake can be adjusted in the camera shake blueprint. The blend in time can be changed to increase/decrease how fast the shaking intensifies.
<br>

![Shake Settings](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%207-10/Images/Handovers/Rock%20Throw/Camera%20Shake%20Settings.png)

## Technical Documentation

### Rock Throw Niagara System
The rock throw niagara system uses a mesh renderer to spawn rock models that spawn and fire in a cone shape using add velocity (In Cone). Spawn burst instantaneous is used to spawn all the particles in one go so that it acts like pellets being shot and initialize particle is used to control the lifetime and size of the rocks fired. 

### Blueprint Logic
An input action is used for when the right mouse button is pressed to get when the button is pressed, whilst it is being held and when it is let go. When the button is pressed, the player movement is deactivated. Then, whilst it is being held, the charge start animation is played. When that is completed, the right click held boolean becomes true, which activates the charge loop animation in the animation blueprint, and the camera shake activates. Next, the rock throw spawn decal and system function is called which uses a line trace to get a location on the ground and behind the player, which is where the crack decal and debris is then spawned. Once the right click button is released, reset is called which allows the rock throw to be activated again. The right click held boolean is then deactivated so that the player stops playing the charge animation. The camera shake then stops and the shoot animation plays with the rock throw niagara system spawning afterwards. When the system has spawned, the debris is destroyed so that debris stops spawning and then the player's movement is reactivated.

![BP Rock Throw](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%207-10/Images/Handovers/Rock%20Throw/Rock%20Throw%20BP.png)
<br>

![BP Rock Throw Function](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%207-10/Images/Handovers/Rock%20Throw/Spawn%20Crack%20and%20Debris.png)

