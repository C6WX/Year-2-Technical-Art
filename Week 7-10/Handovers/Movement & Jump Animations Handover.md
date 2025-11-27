# Movement & Jump Animations Handover

**Movement Animations**

**Callum Wade** **2404781@students.ucreative.ac.uk** 

**Client: Cameron Gildea** **Project: "Name still to be decided"**

**Delivery Date:**

**Version: 1.0**


## Asset Overview
Movement and jump animations that play based on the players direction and speed and also wether the player is touching the ground and their current velocity.


### Integration Guide



### Technical Documentation

#### Movement
For the character to have omni-movement, an animgraph, a blend space, and an event graph that gets the player's direction and speed to determine which animation should be played. When the player is standing still, an idle animation is played but when the player starts moving forward or backwards, it transitions into a walking animation and then a running animation. When the player moves left and right, a left/right walk animation plays before changing to a left/right run animation. When the player.
<br>

![Animgraph](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%207-10/Images/Handovers/Movement/Anim%20Graph.png)
<br>

![ABS Omni-direction](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%207-10/Images/Handovers/Movement/Blend%20Space.png)
<br>

![Event Graph](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%207-10/Images/Handovers/Movement/Animation%20Event%20Graph.png)
<br>

![Idle To Run](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%207-10/Images/Handovers/Movement/Idle%20To%20Run.png)


#### Jumping
Jumping is implemented by adding it onto the locomotion state machine that works the blend space for the movement. The jumping is broken down into three parts: jump start, jump loop and jump land. Jump start activates when the player's Z velocity is greater than 100 and is falling equals true. Jump loop activates when the jump start animation is about to finish or if the players Z velocity is less than 100 and the player is falling. Jump end activates when the player is no longer falling.
<br>

![Locomotion Graph](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%207-10/Images/Handovers/Movement/Locomotion%20Graph.png)
<br>

![Idle To Run to Jump Start](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%207-10/Images/Handovers/Movement/Idle%20To%20Run%20to%20Jump%20Start.png)
<br>

![Jump Start](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%207-10/Images/Handovers/Movement/Jump%20Start.png)
<br>

![Jump Start to Jump Loop](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%207-10/Images/Handovers/Movement/Jump%20Start%20to%20Jump%20Loop.png)
<br>

![Idle To Run to Jump Loop](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%207-10/Images/Handovers/Movement/Idle%20To%20Run%20to%20Jump%20Loop.png)
<br>

![Jump Loop](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%207-10/Images/Handovers/Movement/Jump%20Loop.png)
<br>

![Jump Loop to Jump Land](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%207-10/Images/Handovers/Movement/Jump%20Loop%20to%20Jump%20Land.png)
<br>

![Jump Land](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%207-10/Images/Handovers/Movement/Jump%20Land.png)
<br>

![Jump Land to Idle TO Run](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%207-10/Images/Handovers/Movement/Jump%20Land%20to%20Idle%20To%20Run.png)


