# Ripple Effect Handover

**Ripple Niagara System**

**Callum Wade** **2404781@students.ucreative.ac.uk** 

**Client: Cameron Gildea** **Project: "Name still to be decided"**

**Delivery Date: 28/11/25**

**Version: 1.0**


## Asset Overview
A ripple effect that is created by a niagara system, intended to be spawned once an enemy dies. 

### Integration Guide
To add this effect to your project, use the implementation blueprint that I show below in your enemy death blueprint so that the effect will play whenever the enemy dies.


### Customisation Guide
The niagara system has four open parameters that can be easily changed. These parameters can be changed to alter the colour, lifetime, size, and spawn count of the effect.
<br>

![Ripple Parameters](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%207-10/Images/Handovers/Ripple/Ripple%20Parameters.png)

### Technical Documentation

#### Niagara System
The effect is created by using a sprite renderer to render the ripple material and a spawn emitter burst to spawn a single effect and then a scale sprite size to make the ripple expand outwards. Initialize particle allows the lifetime, colour, and size of the ripple to be adjusted using parameters. 

#### Implementation Blueprint
The effect can be added to an enemy blueprint. In the enemies' death blueprint, use a spawn system at location with a get actor location node plugged into the location input to spawn the ripple where the enemy dies, when they die.

![Implementation BP](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%207-10/Images/Handovers/Ripple/Ripple%20Implementation.png)
