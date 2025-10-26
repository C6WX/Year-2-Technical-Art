# Week 4 Task – Animation Systems

**Callum Wade** **2404781** **24/10/25** 


### 1. Animation Blueprint with Locomotion System


#### What is it?
An animation blueprint with a locomotion system is a blueprint that controls how a character's animations transition from one to another based on the direction, speed or type of movement they are performing. This is made using an animation blueprint with an anim graph. For a walking to running animation, the animation blueprint is used to work out the direction and speed that the character is using and the anim graph is used to layer animations as well as control what causes animations to transition into one another.
<br>
Animation popping occurs when transitions happen at inconsistent times, blend times are too short or poses cause jump cuts between animations. One way to fix this is by adjusting the blend time based on the type of animations you are trying to blend. Another way is by ensuring that transitions only occur at points within the animations that work. For a movement animation, this can be done by using a speed variable so that a running or walking animation only transitions to an idle animation when the speed is low enough.
<br>
When the combat state is in use, it takes over the whole body and stops the walking animation from playing. However this can be fixed by using a layered blend per bone node in the anim graph so that as well as throwing a punch, the character can still be walking with the lower half of their body. Another solution is to just stop the player from being able to walk while the combat state is active so that you wouldn't know that the animations aren't blending while hiding it behind a gameplay feature.


#### Blueprints

##### Event Graph

![Event Graph](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%204/Pictures/Task%201/Event%20Graph.png)

##### Animation Graph

![Anim Graph 1](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%204/Pictures/Task%201/Anim%20Graph%201.png)

##### Locomotion Animation State Machine

![LASM](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%204/Pictures/Task%201/Locomotion%20Animation%20State%20Machine.png)

##### Idle To Run

![Idle To Run](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%204/Pictures/Task%201/Idle%20To%20Run.png)

##### ABS Omni Direction

![ABS Omni Direction](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%204/Pictures/Task%201/ABS%20Omni%20Direction.png)

##### Idle To Run to Jump Start

![Idle To Run to Jump Start](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%204/Pictures/Task%201/Idle%20To%20Run%20To%20Jump%20Start.png)

##### Jump Start

![Jump Start](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%204/Pictures/Task%201/Jump%20Start.png)

##### Jump Start to Jump Loop

![Jump Start to Jump Loop](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%204/Pictures/Task%201/Jump%20Start%20To%20Jump%20Loop.png)

##### Idle To Run to Jump Loop 

![Idle To Run to Jump Loop](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%204/Pictures/Task%201/Idle%20To%20Run%20To%20Jump%20Loop.png)

##### Jump Loop

![Jump Loop](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%204/Pictures/Task%201/Jump%20Loop.png)

##### Jump Loop to Jump Land

![Jump Loop to Jump Land](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%204/Pictures/Task%201/Jump%20Loop%20To%20Jump%20Land.png)

##### Jump Land to Idle To Run

![Jump Land to Idle To Run](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%204/Pictures/Task%201/Jump%20Land%20To%20Idle%20To%20Run.png)

#### Final result

[Omni movement Showcase](https://youtu.be/zA2m0oiNtqQ)




### 2. Combat Combo System Using Animation Montages


#### What is it?
A combat combo system using animation montages is something that can be created in unreal engine to make a character perform different attacks in a row based on player input. This uses animation montages and anim notifies to handle timing and combo flow. 
<br>
The way to make a combo system that feels responsive while maintaining animation quality is by using inertialization for seamless blend posing, input buffering to capture early button presses and optimised montage section transitions with short blend-in times triggered by animation notifies.
<br>
To prevent button mashing, combo windows and input gating can be used to control when the next button can be pressed to activate the next attack. Using a combo windows with animation notifies makes sure that any early or late inputs that are outside of the combo window are ignored. 
<br>
Visual affects, UI and audio cues are different ways that a combo window can be communicated to a player to show them when to press the next input to continue the combo.  


#### Blueprints

##### Attack Combo

![Attack Combo](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%204/Pictures/Task%202/Attack%20Combo.png)

##### Perform Combo Function

![Perform Combo Function](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%204/Pictures/Task%202/Perform%20Combo%20Function.png)

##### Boxing Notifies 

![Boxing Notifies](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%204/Pictures/Task%202/Boxing%20Notifies.png)

##### Hook Notifies

![Hook Notifies](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%204/Pictures/Task%202/Hook%20Notifies.png)

##### Punch Notifies

![Punch Notifies](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%204/Pictures/Task%202/Punch%20Notifies.png)

##### Kick Notifies 

![Kick Notifies](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%204/Pictures/Task%202/Kick%20Notifies.png)

##### Combo Window Notifies

![Combo Window Begin](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%204/Pictures/Task%202/Combo%20Window%20Begin%20Notify.png)
<br>
<br>

![Combo Window End](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%204/Pictures/Task%202/Combo%20Window%20End%20Notify.png)

##### Deal Damage Notify

![Deal Damage Notify](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%204/Pictures/Task%202/Deal%20Damage%20Notify.png)

##### Reset Combo Notify

![Reset Combo Notify](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%204/Pictures/Task%202/Reset%20Combo%20Notify.png)

##### Hit Trace Notifies

![Hit Trace Start](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%204/Pictures/Task%202/Hit%20Trace%20Start%20Notify.png)
<br>
<br>

![Hit Trace End](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%204/Pictures/Task%202/Hit%20Trace%20End%20Notify.png)

##### Hit Trace

![Hit Trace](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%204/Pictures/Task%202/Hit%20Trace.png)

##### Particle Spawner Notify

![Particle Spawner Notify](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%204/Pictures/Task%202/Particle%20Spawner%20Notify.png)

##### Particle Spawning

![Particle Spawning](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%204/Pictures/Task%202/Particle%20Spawning.png)


#### Final result

[Combat Showcase](https://youtu.be/qrDXDM9JHss)

### 3. Animation Layering & Slot System


#### What is it?
An animation layering and slot system is a framework that allows multiple animations to affect different part of a character's skeleton at the same time. Slots are defined regions of the body into which animation montages can play, while layered blending specifies which bones or areas each slot's animation will control.
<br>
The bone split that creates the most natural upper and lower body separation is Spine_01 which is the first joint above the pelvis. This joint cleanly divides the torso from legs while maintaining realistic body mechanics.
<br>
The way to handle transitions between full body and layered animations is by using a blend poses by bool node. This node allows a bool to be used that can be turned on and off to change if an animation is using the full body or just the upper/lower body.
<br>
The blend weight that feels most natural for my character is 1. This is due to the fact that having the blend weight any lower makes the character's movements too stiff and stops the combat animations from reaching far.


#### Blueprints

##### Animation Graph With Layer Blend Per Bone Node

![Anim Graph 2](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%204/Pictures/Task%203/Anim%20Graph%202.png)

#### Final result

[Layer Blend Showcase](https://youtu.be/kNPXKp7luqA)


