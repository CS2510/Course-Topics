## New Idea: `fixedUpdate`
- `fixedUpdate` is called before the physics engine resolves collisions
- `update` is called after the physics engine resolves collisions
- Always use `fixedUpdate` when you manually change the position of a game object