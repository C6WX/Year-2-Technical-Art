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
What does it do? Gets the velocity, speed and direction as well as checking if the player is falling so that these variables can be used in the locomotion animation state machine.
![Event Graph](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%204/Pictures/Task%201/Event%20Graph.png)

##### Animation Graph
What does it do? Allows the output pose to control the whole body of the character.
![Anim Graph 1](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%204/Pictures/Task%201/Anim%20Graph%201.png)

##### Locomotion Animation State Machine
What does it do? This shows the transition between different movement animations and stores the requirements to change animations.
![LASM](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%204/Pictures/Task%201/Locomotion%20Animation%20State%20Machine.png)

##### Idle To Run
What does it do? This changes the character from an idle pose to a walking pose to a running pose based on the speed and direction they are moving.
![Idle To Run](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%204/Pictures/Task%201/Idle%20To%20Run.png)

##### ABS Omni Direction
What is it? This is the graph that controls the transitioning between different movement animations.
![ABS Omni Direction](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%204/Pictures/Task%201/ABS%20Omni%20Direction.png)

##### Idle To Run to Jump Start
What does it do? This checks if the players Z velocity is greater then 100 and that they are falling to make sure that the player has jumped so that the animation can transition to the jump start animation.
![Idle To Run to Jump Start](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%204/Pictures/Task%201/Idle%20To%20Run%20To%20Jump%20Start.png)

##### Jump Start

![Jump Start](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%204/Pictures/Task%201/Jump%20Start.png)

##### Jump Start to Jump Loop
What does it do? This blueprint checks how long is left of the jump start animation and then at the last second of it, transitions to the jump loop animation.
![Jump Start to Jump Loop](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%204/Pictures/Task%201/Jump%20Start%20To%20Jump%20Loop.png)

##### Idle To Run to Jump Loop 
What does it do? This checks if the player's Z velocity is less then 100 and that they are falling to prove that they have fallen so that they can then transition to the jump loop animation.
![Idle To Run to Jump Loop](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%204/Pictures/Task%201/Idle%20To%20Run%20To%20Jump%20Loop.png)

##### Jump Loop

![Jump Loop](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%204/Pictures/Task%201/Jump%20Loop.png)

##### Jump Loop to Jump Land
What does it do? This checks if the player has stopped falling so that it can transition the player to the jump land animation.
![Jump Loop to Jump Land](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%204/Pictures/Task%201/Jump%20Loop%20To%20Jump%20Land.png)

##### Jump Land to Idle To Run
What does it do? When the jump land animation is nearly finished, the animation is blended into the idle or moving animation based on the player's speed.
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
What does it do? When the left mouse button is pressed, the upper body variable is enabled meaning that the upper body animations will be blended with the lower body animations, then the perform combo function is activated. After that the next animation in the montage is played and then after it has played, upper body is deactivated to as the upper body is no longer being used by an animation. Based on the output of the perform combo function, the attack combo will be set back to 0, or the attack combo will increase and the next combo will play if the left mouse button is pressed in time, otherwise the attack combo will be set back to 0.
![Attack Combo](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%204/Pictures/Task%202/Attack%20Combo.png)

##### Perform Combo Function
What does it do? This function checks if the combo has been finished. If it has finished, then attack combo will be reset, otherwise the next attack will be able to be activated.
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
What does it do? Activates the reset combo event on the player through BPI Notifiers
![Reset Combo Notify](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%204/Pictures/Task%202/Reset%20Combo%20Notify.png)

##### Hit Trace Notifies
What does it do? Activates the Hit Trace event on the player through BPI Notifiers
![Hit Trace Start](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%204/Pictures/Task%202/Hit%20Trace%20Start%20Notify.png)
<br>
<br>

![Hit Trace End](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%204/Pictures/Task%202/Hit%20Trace%20End%20Notify.png)

##### Hit Trace
What does it do? Activates a visible trace of where the player is hitting, by getting a specific bone in the skeleton, before removing the traces after a certain amount of time.
![Hit Trace](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%204/Pictures/Task%202/Hit%20Trace.png)

##### Particle Spawner Notify
What does it do? Activates the Particle spawner event on the player through BPI Notifiers
![Particle Spawner Notify](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%204/Pictures/Task%202/Particle%20Spawner%20Notify.png)

##### Particle Spawning
What does it do? Spawns particles at the player's right hand whenever they damage something.
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
What does it do? Blends the base pose with upper body animations to allow the character to move while also attacking.
![Anim Graph 2](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%204/Pictures/Task%203/Anim%20Graph%202.png)

#### Final result

[Layer Blend Showcase](https://youtu.be/kNPXKp7luqA)


