## New Idea: Overview: Collision Resolution and Minimum Transform Vector
- We need to resolve collisions by moving objects that overlap away from each other
- We want to move objects the minimum amount possible to resolve collisions
- The minimum amount and direction is called the *Minimum Transform Vector*
- The separate axis theorem, the process we use to find *if* objects are in collsion, can also give us the Minimum Transform Vector

## New Idea: Finding the Minimum Transform Vector
- Until now, our collision code only determine if polygons were in collision, not how much they were in collision
- While we loop over the "shadows" (projections onto the wall), we can keep track of the minimum amount of overlap we see and in what direction
- If we never find a gap in the projections, then we can calculate the minimum transform vector
  - The length of the vector is the minimum amount of overlap we saw
  - The direction of the vector is the direction of the axis used when projecting
- By returning this minimum transform vector instead of just `true`, we can do collision resolution

## New Idea: Collision Resolution
- When the Scene class is doing collision detection, it tracks which game objects have a rigid body component
- We store the two game objects in these kinds of collisions and their minimum transform vectors
- After send collision events, we loop over these collision and move the rigid bodies by the amount of teh minimum transform vectors
  - ...remembering to invert the minimum transform vector if the game object with the rigid body is listed second.
- Note that this satisfies Netwon's third law of motion