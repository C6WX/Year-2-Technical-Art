# Week 2 Task – Material Systems and Techniques  

**Callum Wade** **2404781** **07/10/25** 

### 1. Stylized Water Material with World Position Offset  

#### Problems during creation

#### Solutions

#### Technical choices

#### Final result

![Water Material](WaterMaterialTest.gif)

#### Blueprints

<br>
<iframe width="600" height="600" src="https://blueprintue.com/render/nk_eyujq/" scrolling="no" allowfullscreen></iframe>
<br>

#### About topic (guiding questions)


### 2. Material Parameter Collection (MPC) System    

#### Problems during creation

1. When lurping between the wet and dry textures, they would change too quick and too much.
2. When going to multiply the base colour of the landscape with the base colour, it gave an error as a float 3 and float 4 couldn't be multiplied together.
3. The global controller blueprint wasn't properly changing the light intensity of the sky light in the scene.
4. I tried using a button to control changing the time of day but it wasn't doing anything.

#### Solutions

1. I added a divide node to the RainAmount parameter before it went into the lurp node so that the parameter can be changed easier while the material would change slower.
2. To solve this problem, I used a component mask to turn the float 4 into a float 3.
3. Instead of adjusting the intensity of the sky light, I changed the directional light. 
4. Instead of using a button to change the time of day, I used a delay node to change it after 5 seconds.

#### Technical choices

#### Final result

![Material Parameter Collection System](MPC.gif)

#### Blueprints

##### Landscape Material
<iframe width="600" height="600" src="https://blueprintue.com/render/9t4olk6n/" scrolling="no" allowfullscreen></iframe>
<br>

##### Bush Material
<iframe width="600" height="600" src="https://blueprintue.com/render/iccj0cnb/"   scrolling="no" allowfullscreen></iframe>
<br>

##### Global Controller
<iframe width="600" height="600" src="https://blueprintue.com/render/p3g1jaar/"   scrolling="no" allowfullscreen></iframe>
<br>


#### About topic (guiding questions)



### 3. Dynamic Material Instance with Runtime Control    

#### Problems during creation

#### Solutions

#### Technical choices

#### Final result

![Dynamic Material Instance](DynamicMaterialInstance.gif)

#### Blueprints

##### Wood Material
<iframe width="600" height="600" src="https://blueprintue.com/render/5zp4cm7t/" scrolling="no" allowfullscreen></iframe>
<br>

##### Dynamic Panel
<iframe width="600" height="600" src="https://blueprintue.com/render/xp2fivgm/" scrolling="no" allowfullscreen></iframe>
<br>

#### About topic (guiding questions)



### 4. Parallax Occlusion Mapping (POM) Material      

#### Problems during creation

1. A glitch occured with the material where the shadows took over the whole material so that it could'nt be seen.

#### Solutions

2. To solve this problem, I disabled cast shadows. 

#### Technical choices

#### Final result

![Brick POM Material](https://raw.githubusercontent.com/C6WX/Images/refs/heads/main/Images/POM%20Brick%20material.png)

#### Blueprints

##### Brick Texture
<iframe width="600" height="600" src="https://blueprintue.com/render/chrrzmir/"   scrolling="no" allowfullscreen></iframe>
<br>

#### About topic (guiding questions)


### 5. Post Process Material   

#### Problems during creation

#### Solutions

#### Technical choices

#### Final result

![Post Process Material](CellShading.gif)

#### Blueprints

##### Cell Shader
<iframe width="600" height="600" src="https://blueprintue.com/render/2costsu5/" scrolling="no" allowfullscreen></iframe>
<br>

##### Character Material
<iframe width="600" height="600" src="https://blueprintue.com/render/4upsvvjy/" scrolling="no" allowfullscreen></iframe>
<br>

##### Character Outline
<iframe width="600" height="600" src="https://blueprintue.com/render/4zd15p_q/" scrolling="no" allowfullscreen></iframe>
<br>

##### Emissive Material
<iframe width="600" height="600" src="https://blueprintue.com/render/a5raxtpb/" scrolling="no" allowfullscreen></iframe>
<br>

#### About topic (guiding questions)