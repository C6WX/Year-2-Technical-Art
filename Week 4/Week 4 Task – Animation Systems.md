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



#### Final result



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



#### Final result



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



#### Final result




