## 💡New Idea: deltaTime
- Not all computers run at the same speed, and at times the same computer will run at different speeds during the lifecycle of a game.
- We need to make our game `frame rate independent`
- We do this by tracking a variable called `deltaTime`.
  - We multiply all movements by this variable.
  - This makes movement speed a rate of pixels per second


## 💡New Idea: Variable deltaTime
- Tracking deltaTime by itself will not make our game frame rate independent. 
- We need to ask how much time has passed between each frame
  - We do this by adding a new argument to our game loop, which gets called by requestAnimationFrame