# Week 2 Task – Material Systems and Techniques  
**Unit:** Technical Art (Level 5 Games Development)  

## Brief  
This week focuses on developing practical skills in advanced material creation and runtime material control in Unreal Engine 5. You are required to create a **material showcase project** that demonstrates your understanding of key material systems and techniques covered in this week's content.

Your project should demonstrate technical proficiency, creative problem-solving, and an understanding of how these systems are used in professional game development workflows.

---

## Deliverables

You must create **all five** of the following materials/systems in a single UE5 project:

---

### 1. Stylized Water Material with World Position Offset  
**Technical Requirements:**  
- Implement **World Position Offset (WPO)** to create animated wave motion
- Use time-based animation for continuous wave movement
- Include parameters for wave height, speed, and frequency
- Add visual elements: foam, depth fade, refraction, or transparency
- Demonstrate vertex animation without skeletal meshes

**Guiding Questions:**
- How does WPO affect performance compared to animated meshes?
- How can you control wave direction and intensity?
- What vertex density is required for smooth wave deformation?
- How does your water material respond to different lighting conditions?

---

### 2. Material Parameter Collection (MPC) System  
**Technical Requirements:**  
- Create an MPC with at least **4 parameters** that control a global scene effect
- Implement the MPC in **at least 2 different materials**
- Create a Blueprint that modifies MPC values at runtime
- Demonstrate a cohesive environmental effect (e.g., time of day, weather system, global color grading)

**Example Systems:**
- Time of day (sun angle, ambient color, light intensity)
- Weather system (rain intensity, wetness, wind strength)
- Damage/corruption spreading across multiple surfaces
- Global magical effect or environmental hazard

**Guiding Questions:**
- Why use MPC instead of individual material parameters?
- How does your system maintain visual consistency across materials?
- What performance benefits does MPC provide?

---

### 3. Dynamic Material Instance with Runtime Control  
**Technical Requirements:**  
- Create a material with **at least 3 exposed parameters** (scalar and/or vector)
- Implement a **Dynamic Material Instance (DMI)** in Blueprint
- Create interactive controls to modify parameters during gameplay
- Demonstrate a practical use case (e.g., damage effect, dissolve, customization, hit feedback)

**Implementation Details:**
- Create DMI in BeginPlay (not every frame!)
- Use appropriate parameter types (scalar, vector, texture)
- Show smooth transitions or interpolation between values
- Include visual feedback that responds to player input or game events

**Guiding Questions:**
- When should you use DMI versus Material Instance Constant?
- How do you optimize DMI creation and updates?
- What gameplay scenarios benefit from runtime material modification?

---

### 4. Parallax Occlusion Mapping (POM) Material  
**Technical Requirements:**  
- Implement **Parallax Occlusion Mapping** using UE5's POM node
- Use appropriate height map with visible depth effect
- Configure min/max steps for quality vs. performance balance
- Apply POM offset to all relevant texture samples (base color, normal, roughness)
- Demonstrate self-occlusion and depth parallax


**Guiding Questions:**
- How does step count affect visual quality and performance?
- What types of surfaces benefit most from POM?
- How does POM compare to simple bump offset?
- What are the limitations at silhouette edges?

---

### 5. Additional Advanced Material Technique  
**Choose ONE of the following:**

#### Option A: Post Process Material
- Create a post-process material with a visible screen effect
- Choose blendable location (before/after tonemapping) appropriately
- Implement effect using Scene Texture nodes
- Examples: outline shader, screen distortion, custom color grading, stylized effect

#### Option B: Comprehensive Master Material and Triplanar Mapping Material
- Develop a comprehensive Master Material
- Implement world-aligned texture projection blending with the master material
- Use UE5's WorldAlignedTexture node or custom setup
- Demonstate the customization and organization of your material instance and material graph.


#### Option C: Material Function Library
- Create at least 3 reusable Material Functions
- Use functions in multiple materials to demonstrate reusability
- Examples: custom tiling, Fresnel effects, UV manipulation, noise generators
- Document inputs/outputs clearly

#### Option D: Runtime Virtual Texture (RVT) Implementation
- Set up RVT volume in your scene
- Configure materials to write to RVT
- Sample RVT data in another material
- Demonstrate practical use (e.g., footprints, decals, dynamic blending)

---

## Assessment Criteria

Your work will be evaluated against the following criteria:

### Exploring
- Engaging in critical and creative inquiry through questioning, research, and material/process-based investigations
- Demonstrating understanding of technical concepts through implementation
- Experimenting with parameters and techniques to understand their effects

### Making
- Developing and refining creative work through iteration, risk-taking, and material engagement
- Technical proficiency in material creation and Blueprint implementation
- Quality of visual output and attention to detail
- Problem-solving when encountering technical challenges

### Connecting
- Communicating technical decisions and implementation choices
- Engaging with professional workflows and industry-standard practices
- Demonstrating understanding of when and why to use specific techniques
- Clear documentation of your materials and systems

### Situating
- Critically positioning work within professional game development contexts
- Understanding performance implications and optimization considerations
- Awareness of platform limitations and scalability
- Ethical consideration of accessibility (e.g., motion, visual effects)

### Synthesizing
- Bringing together disparate elements into meaningful, cohesive outcomes
- Creating a unified showcase that demonstrates multiple techniques working together
- Integrating materials into a coherent scene or demonstration
- Showing how different systems complement each other

---


**Technical Documentation** 
   - Brief description of each deliverable
   - Technical challenges encountered and solutions
   - Performance considerations and optimization choices
   - Reflection on learning outcomes and professional applications
   - Include screenshots, gifs and any other applicable media
   - Show before / after where relevant
   - Detail your understanding of your implementation


---


### Documentation:
- Take screenshots of your material graphs as you work
- Record video clips of interesting developments
- Note down problems and solutions as they occur
- Explain *why* you made specific technical choices

---


**Remember:** This task is about demonstrating technical understanding through practical application. Focus on clean implementation, good documentation, and showing that you understand *why* these techniques are used in professional workflows.

Good luck!

