# Week 2 Task – Material Systems and Techniques  

**Callum Wade** **2404781** **07/10/25** 

### 1. Stylized Water Material with World Position Offset  

#### Problems during creation

#### Solutions

#### Technical choices

#### Final result

![Water Material](WaterMaterialTest.gif)

#### Blueprint

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

![Material Parameter Collection System](WaterMaterialTest.gif)

#### Blueprint

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

#### Blueprint

#### About topic (guiding questions)



### 4. Parallax Occlusion Mapping (POM) Material      

#### Problems during creation

#### Solutions

#### Technical choices

#### Final result

#### Blueprint

#### About topic (guiding questions)


### 5. Post Process Material   

#### Problems during creation

#### Solutions

#### Technical choices

#### Final result

#### Blueprint

#### About topic (guiding questions)