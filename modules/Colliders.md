# New Idea: Colliders
- We want the engine to keep track of collisions for game objects that have been "labeled" with a Collider component
  - We can use colliders to simplify hit boxes
- The engine will track anything that has a Collider component
- The engine will send events when there is a collision with the game objects in question
- Components can listen for these events to fire