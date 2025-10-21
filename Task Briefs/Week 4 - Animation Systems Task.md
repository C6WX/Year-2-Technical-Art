# Week 4 Task – Animation Systems
**Unit:** Technical Art (Level 5 Games Development)  

## Brief
This week focuses on developing a complete character animation system using Unreal Engine 5's Animation Blueprint and Animation Montages. You are required to create a **functional combat character** with a sophisticated combo attack system that demonstrates animation montage control, state machine logic, and layered animation techniques used in modern action games.

Your project should showcase technical competence and understanding of Animation Blueprints / animation montages and awareness of responsive gameplay animation strategies used in professional game development.

---

## Core Deliverable: Combat Character with Animation Blueprint & Combo System

You must create a **complete playable character** that incorporates **all three** of the following core systems:

---

### 1. Animation Blueprint with Locomotion System
**Technical Requirements:**
- Create a **complete Animation Blueprint** with Event Graph and Anim Graph
- Implement a **locomotion state machine** with at least **5 states**:
  - **Idle** - Standing still
  - **Walk/Run** - Movement (can use blend space or separate states)
  - **Jump Start** - Beginning of jump
  - **Jump Loop** - Airborne state
  - **Jump End** - Landing
- Build a **1D or 2D Blend Space** for movement (Speed, or Speed + Direction) **2D blend space is recommended**
- Implement **variable updates** in Event Graph:
  - **Speed** - Character velocity magnitude
  - **Direction** - Movement direction relative to character rotation (for 2D blend space)
  - **IsInAir** - Jumping/falling state


**Guiding Questions:**
- How do you prevent animation popping during state transitions?
- How does the combat state interact with locomotion states?

---

### 2. Combat Combo System Using Animation Montages
**Technical Requirements:**
- Create **1 attack combo montage** with at least **4 attack sections**:
  Example:
  - **Combo1** - First light attack
  - **Combo2** - Second light attack
  - **Combo3** - Third light attack
  - **ComboFinisher** - Heavy finishing attack
- Implement **montage section jumping** based on player input timing
- Use **Animation Notifies** for:
  - **Combo Window** - Time period when player can input next attack
  - **Damage Dealing** - When attack should deal damage to enemies
  - **Combo Reset** - When combo chain resets to beginning
- Create **Blueprint logic** in Character BP to handle:
  - Attack input detection
  - Combo counter tracking
  - Section jumping based on input timing
  - Combo timeout/reset logic
- Implement **montage slot system** (UpperBody slot) to allow:
  - Attacking while moving (optional)
  - Upper body combat with lower body locomotion

**Advanced Features:** (optional)
- **Heavy attack variant** - Hold button for different attack
- **Combo branching** - Different paths based on input (light vs heavy)
- **Combo canceling** - Ability to dodge/roll out of combo


**Technical Implementation Details:**

#### Montage Setup:
```
Attack_Montage sections:
- Combo1 (0.0s - 0.8s) - First attack animation
- Combo2 (0.8s - 1.6s) - Second attack animation
- Combo3 (1.6s - 2.4s) - Third attack animation
- ComboFinisher (2.4s - 3.5s) - Powerful final attack
```

#### Animation Notifies:
- **AnimNotify_ComboWindow** - Placed during recovery frames when next input is accepted
- **AnimNotify_DealDamage** - Placed at impact frame of attack
- **AnimNotify_ComboReset** - Placed at end of each section if no input received

#### Character Blueprint Logic:
- **Attack Input** → Check if can attack → Play montage or jump to next section
- **Combo Counter** → Tracks current position in combo (0-3)
- **Input Buffer** → Stores input during combo window for responsive feel
- **Montage End** → Reset combo counter and combat state

**Guiding Questions:**
- How do you make the combo feel responsive while maintaining animation quality?
- How do you prevent button mashing while rewarding timing?
- How do you communicate combo windows to the player visually?

---

### 3. Animation Layering & Slot System
**Technical Requirements:**
- Implement **Layered Blend Per Bone** in Animation Blueprint
- Create **bone mask** for upper body (spine, arms, head)
- Set up **DefaultSlot** and **UpperBody** slot in Anim Graph
- Configure **montage to use UpperBody slot** for attacks
- Demonstrate **simultaneous animations**:
  - Lower body: Locomotion (running, walking)
  - Upper body: Combat attacks from montage
- Implement **smooth blending** between layers with appropriate blend weights

**Technical Implementation:**
- In Anim Graph: Locomotion State Machine → DefaultSlot → UpperBody Slot → Layered Blend Per Bone
- Create skeleton bone mask filtering spine_01 and above for upper body
- Set blend depth and blend mode for natural movement
- Test attacking while standing, walking, and running

**Advanced Features:** (optional)
- **Additive aim offset** - Character can look around while in combat
- **Hit reactions** - Upper body reacts to damage while legs continue moving
- **Contextual animations** - Different attack animations based on movement state

**Guiding Questions:**
- What bone split creates the most natural upper/lower body separation?
- How do you handle the transition between full-body and layered animations?
- What blend weights feel most natural for your character?

---

## Assessment Criteria

### Exploring
**Engaging in critical and creative inquiry through questioning, research, and material/process-based investigations**
- Research combat animation systems in action games (Devil May Cry, God of War, Bayonetta, Elden Ring)
- Document your research process and technical discoveries
- Analyze what makes combat feel responsive and satisfying

### Making
**Developing and refining creative work through iteration, risk-taking, and material engagement**
- Technical proficiency in Animation Blueprint construction and montage setup
- Iterative refinement of combo timing and state machine logic
- Creative problem-solving in implementing responsive combat feel
- Risk-taking in attempting advanced layering and branching systems
- Polish in animation transitions and gameplay responsiveness

### Connecting
**Communicating, collaborating, and engaging with audiences, industries, and networks**
- Clear documentation of combo system logic and animation timing decisions
- Understanding of professional combat animation workflows
- Communication of complex technical concepts (montage sections, notifies, input buffering)
- Demonstration of collaborative potential (modular, reusable combat systems)

### Situating
**Critically positioning work within social, cultural, environmental, ethical, and professional contexts**

- Professional context awareness (how AAA studios implement combo systems)
- Understanding of animation's role in gameplay feel and player satisfaction

### Synthesizing
**Bringing together disparate elements into meaningful, cohesive outcomes**
- Integration of locomotion, combat, and layering systems into unified character
- Coherent visual and technical approach across all animation subsystems
- Demonstration of how state machines, montages, and slots work together
- Creation of responsive, satisfying combat gameplay
- Synthesis of technical requirements with gameplay feel and artistic vision

---


## Advanced Challenge Options (Optional)

consider implementing:

### Advanced Combat Features
- **Combo branching** - Light attack vs heavy attack paths with different animations
- **Directional attacks** - Different combos based on movement direction (forward, side, back)
- **Aerial combat** - Jump attacks that can combo into ground attacks
- **Dodge/parry system** - Defensive animations with i-frames and counter-attack opportunities
- **Weapon switching** - Multiple weapon types with different combo chains
- **Charge attacks** - Hold button for powered-up attacks with different timing

### Enhanced Animation Systems
- **Hit reactions** - Enemy and player damage responses using additive animations
- **Stamina integration** - Combat animations affected by stamina state
- **Dynamic camera** - Camera shake and zoom during impactful attacks using animation notifies

### Polish & Feedback Systems
- **VFX integration** - Particle effects triggered by animation notifies (slashes, impacts, dust)
- **Sound design** - Whoosh sounds, impact sounds, and voice grunts synced to animations
- **Screen effects** - Hit stop, slow motion, or screen shake on heavy attacks
- **UI feedback** - Combo counter display, damage numbers, combo rating system
- **Input buffering** - Advanced input queue system for frame-perfect combos

---

## Resources and Research Starting Points

### Technical Resources:
- [UE5 Animation Blueprint Documentation](https://dev.epicgames.com/documentation/en-us/unreal-engine/animation-blueprints-in-unreal-engine)
- [Animation Montages Documentation](https://dev.epicgames.com/documentation/en-us/unreal-engine/animation-montage-in-unreal-engine)
- [Animation Notifies Documentation](https://dev.epicgames.com/documentation/en-us/unreal-engine/animation-notifies-in-unreal-engine)
- [Blend Spaces Documentation](https://dev.epicgames.com/documentation/en-us/unreal-engine/blend-spaces-in-unreal-engine)
- GDC talks on combat animation (God of War, Devil May Cry, Bayonetta)

### Research Areas:
- **Combat Animation Principles**: Weight, impact, anticipation, recovery frames
- **Game Feel**: How animation timing affects perceived responsiveness
- **Fighting Game Design**: Frame data, combo systems, input buffering
- **Action Game Analysis**: Study combo flow in character action games
- **Player Psychology**: What makes combat feel satisfying and fair


### Animation Packs (Marketplace/Mixamo):
- Mixamo has free combat animation sets you can use
- UE Marketplace has various combat animation packs
- Ensure animations have clear attack and recovery phases for combo timing

### Combo System Design Resources:
- Study fighting game frame data to understand attack timing
- Research "animation canceling" vs "animation commitment" design philosophies
- Analyze how different games communicate combo windows to players
- Look into input buffering systems for responsive controls

---

**Key Implementation Points:**
- Each section has an **AnimNotify_ComboWindow** that enables input detection
- Character Blueprint tracks **ComboCounter** (0, 1, 2, 3)
- On attack input during combo window: `Montage Jump to Section` based on counter
- On combo window end without input: Reset counter and return to idle
- **Input buffering**: Store input slightly before window opens for responsive feel

