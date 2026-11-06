
## New Idea: Platformer Games
- We can make a platformer game once we have collision resolution and rigid body dynamics
- Create a player characters with a `Collider` and `RigidBody`
- Give that `RigidBody` gravity. 
  - Remember that games rarely use actually gravity values, especially if you are not using precise world units. 
  - Play around with this value until you get a value that works
- Create some platforms that have `Collider` components
- Your characters should land on these game objects but be able to free fall when not on these platforms.
- ⚠️ This implementation has problems because game objects continuously increase in velocity, even when they have landed on a platform
- In order to prevent a game object from slowly being sucked through a platform, we need to set its vertical velocity to 0 if it lands on a platform.
- In our `onCollisonStay` event, check to see if we are in collision with a platform that is below us and the minimum trantsform vector is pointing up. If so, set our vertical velocity to 0.
- 
## 💡New Idea: Platformer Dynamics
- Characters can't jump if they aren't grounded
- Characters don't slip through platforms
- Gravity is rarely exactly true gravity
- Characters need a terminal velocity
- Characters often can double jump
- Charcters don't float when they bump their heads

## 👩‍💻Code Together: Platformer Dynamics
- Add an isGrounded variable
  - Set to true when there is a collision below and you are heading down
  - Set velocity to 0
- Add a double jump variable
  - Invert whenever you jump
- Cap downward velocity
- Pick your own gravity
- When you hit something above you and you are going up, set velocity to 0
