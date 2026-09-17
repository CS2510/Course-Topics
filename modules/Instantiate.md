## 💡New Idea: Add `instantiate`
  - Unity has a global function called `instantiate`. 
  - We can mimic that behavior by creating a gloabl function called instantiate that points to `Scene.instantiate`
  - Instantiate now takes a position argument, so we can position our game objects easily when we create scenes
  - We can also add a rotation argument, so we can rotate our game objects