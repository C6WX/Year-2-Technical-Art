# Week 3 Task – Auto Landscape Materials

**Callum Wade** **2404781** **17/10/25** 


### 1. Height-Based Blending System 

#### What is it?

A height-based blending system is a technique used to apply different material layers to an object (usually a landscape), using each vertex's height value to control the blending alpha between multiple textures.
<br>
To prevent harsh transitions, falloff controls can be applied on the height mask by using power curve functions to create softer blending edges between material layers. Having smoother edges between zones adds more of a natural look to the changes in biomes while also preserving distinct biome characteristics.
<br>
The height range that works best for a landscape varies based on the vertical scale of each landscape. For example, smaller landscape's height range for hills can be anywhere between 80-160 whereas a more mountainous landscape can bet anywhere between 400-1000. 
<br>
Height blending works with other blending systems by mixing their masks together. For example, a slope mask can adjust the height based mask so that rock textures appear on steep slopes, while grass and snow appear based on height. Noise or detail textures break up repeating patterns, making transitions look more natural and realistic.


#### Blueprints

##### Base Layer Blueprint

![Base Layer](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%203/Images/Task%201/Base%20Layer%20Blueprint.png)

##### Snow Layer

![Snow Layer](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%203/Images/Task%201/Snow%20Layer.png)

##### UVs and depth fading 

![UVs](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%203/Images/Task%201/UVs%20and%20depth%20fade%20mask.png)

##### Tiling Variation

![Tiling Variation](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%203/Images/Task%201/Tiling%20Variation.png)

##### Tiling Variation Function

![Tiling Variation F](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%203/Images/Task%201/Tiling%20Variation%20Function.png)

##### Near/Far Tiling

![Near/Far Tiling](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%203/Images/Task%201/Near%20Far%20Tiling.png)

##### Material Blending

![Material Blending](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%203/Images/Task%201/Material%20Blending.png)

##### Snow Mask

![Snow Mask](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%203/Images/Task%201/Snow%20Mask.png)

##### Height Based Snow Blending 

![Snow Blending](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%203/Images/Task%201/Height%20Based%20Snow%20blending%20system.png)


#### Final result

[Snow Height Blending Video](https://youtu.be/Pi4WpL4WLGk)

### 2. Slope-Based Blending System 

#### What is it?

A slope-based blending system automatically blends textures based on the steepness of a terrain surface instead of just using height alone. It examines how sloped each part of the landscape is and applies materials like rock on steep cliffs and grass on flatter ground.
<br>
Overhangs and complex geometry can confuse normal-based slope calculations because surfaces can face unexpected direction. One way to handle this is by using layered material functions specific to complex geometry or manually painting materials on problematic areas. The other way of handling this is by using additional techniques like custom mesh attributes, vertex colours or baked masks to accurately paint materials on vertical or underside surfaces.
<br>
The most natural-looking transitions are usually created on gentle slopes of about 15 to 45 degrees. Smooth falloff between this range creates realistic blending without harsh lines.
<br>
Slope blending enhances the sense of geological realism by copying how natural erosion and weathering distributes materials differently on steep versus flat surfaces. It ensures the flat surfaces will be covered in grass whereas steeper surfaces will be covered in rock.

#### Blueprints

##### Material Slope Masks

![Slope Masks](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%203/Images/Task%201/Snow%20Layer.png)

##### MidLow Layer

![MidLow Material](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%203/Images/Task%202/MidLow%20Layer.png)

##### MidHigh Layer

![MidHigh Material](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%203/Images/Task%202/MidHigh%20Layer.png)

##### Cliff Layer

![Cliff Layer](https://raw.githubusercontent.com/C6WX/Year-2-Technical-Art/refs/heads/main/Week%203/Images/Task%202/Cliff%20Layer.png)

#### Final result

[Slope Mask Video](https://youtu.be/CJs2Rk82Or0)

### 3. Foliage Type Integration and Generation  

#### What is it?

Foliage type integration and generation refers to bringing different foliage models in a game and then automatically placing them in the environment.
<br>
To create believable ecosystem distributions, many key factors need to be taken into account. These key factors include: environmental gradients, species interactions, environment disturbance, micro-habitats and variation. To account for all these factors, research on the environment will be required for specie variation, gradient masking and layered blending for realistic environment transitions and map scale and design to determine how big the environment should be and if there is any disturbances from nearby environments.
<br>
In real environments, foliage density is determined by resource availability, competition, climate and disturbances.
<br>
To balance visual richness with performance, optimising foliage placement using culling, level of detail systems and instancing. Level of detail can be used by using higher-detailed models for plants closer to the player and less detailed models for plants further away. Using frustum, occlusion and distance culling can avoid rendering foliage that is outside the camera view or blocked by other objects. Reusing instanced static meshes can also help as it will reduce the amount of draw call required for rendering the foliage.


#### Blueprints



#### Final result



### 4. Extras


#### Blueprints


##### Colour Variation


##### Tiling Variation 


##### Puddles


##### Rocks Using Grass Types
