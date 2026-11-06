## New Idea: Different kinds of collisions
- Powerups like coins have the following properties
  - They can't push objects
  - They aren't pushed
  - They don't initiate collision events
- Ground/Elevators/Platforms have the following properties
  - They push objects
  - They aren't pushed
  - They don't initiate collision events
- Sensors (invisible colliders) have the following properties
  - They don't push objects
  - They aren't pushed
  - They initiate collision events
- Characters have the following properties
  - They push objects
  - They get pushed
  - They initiate collision events
- Here is a table with the same information:

| Type                | Is Pushed? | Pushes Back? | Initiates Events? | isTrigger? | RigidBody? |
| ------------------- | ---------- | ------------ | ----------------- | ---------- | ---------- |
| 🪙 Coin (powerup)    | No         | No           | No                | Yes        | No         |
| 🛗 Floor (immovable) | No         | Yes          | No                | No         | No         |
| ❓Sensor             | No         | No           | Yes               | Yes        | Yes        |
| 🏃 Character         | Yes        | Yes          | Yes               | No         | Yes        |


## New Idea: Detailed Collision Rules
- If two colliders on different game objects do not overlap, there is no interaction
  - No Physics, no events
  - Break
- If we get here, we know two colliders on different game objects overlap
- If neither of the game objects have a Rigid Body, then there will be no interaction between the colliders
  - https://discussions.unity.com/t/what-are-the-oncollisionenter-requirements/104083
  - No physics, no events
  - Break
- If we reach this point, then the physics engine will respond to the overlap of the colliders. We know that the colliders haven't been disabled with Physics.IgnoreCollisions, we know the layers the colliders are in are allowed to collide in the Layer Collision Matrix, and we know at least one of the game objects has a rigidBody attached
- If either of the colliders is marked as a trigger, then:
  - No physics, onTriggerXXX events
- If we get here, neither of the colliders is marked as a trigger and we have at least on rigid body between the pair
  - If they are both have rigid bodies
    - Physics response on both, onCollisionXXX events
  - If one has a rigid body
    - Physics response only on the one with a rigid body, onCollisionXXX events