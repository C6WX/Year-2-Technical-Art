# Combo Attack Handover

**Attack Animations**

**Callum Wade** **2404781@students.ucreative.ac.uk** 

**Client: Cameron Gildea** **Project: "Name still to be decided"**

**Delivery Date: 28/11/25**

**Version: 1.0**


## Asset Overview
Three animations that play one by one for each click of the left mouse button to create an attack combo. Whilst the animations are playing, the player is frozen in place and once an animation stops and another hasn't been activated, the player movement reactivates.

### Integration Guide
To add these to your project, you can either use the character provided or recreate the blueprint displayed below and change the skeleton on the animations provided.

### Customization Guide

The attack animations can be shortened and have their play rate increased within their animation montages. The selected animations can be changed and added to within the attacks anim montage variable in the third person character blueprint. 

### Technical Documentation

When the left mouse button is pressed, the player's movement is frozen and the perform combo function is activated. The function then outputs the current fighting animation which is then played. The perform combo function first checks that there is an attack left to be played. If there is an attack left, the next animation in the sequence is outputted from the function and the perform attack event is called which increases the attack combo variable by one and then creates a delay which detects if the player presses the left mouse button again in time. If the button is not pressed in time or there is no animation left to be played, the attack combo variable is reset back to 0 and the player movement is reactivated.
<br>

![Attack Combo](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%207-10/Images/Handovers/Attack%20Combo/Attack%20Combo.png)
<br>

![Perform Combo Function](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%207-10/Images/Handovers/Attack%20Combo/Perform%20Combo%20Function.png)
