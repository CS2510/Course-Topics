## 💡New Idea: Repeated rendering
- We can manually call draw over and over to create an animation...
- ... and using a `for` loop causes the browser to crash.
- We need to find a way for the browser to call our code on a regular interval, which we can do with the `requestAnimationFrame` function
- requestAnimationFrame
  - 🔗Additional information:
    - [MDN website about requestAnimationFrame](https://developer.mozilla.org/en-US/docs/Web/API/Window/requestAnimationFrame)
    - [W3 Schools requestAnimationFrame](https://www.w3schools.com/jsref/met_win_requestanimationframe.asp)

## 💡New Idea: Updating our game
- When we create a game, we want to strictly separate our game representation (model) from our draw code.
- Technically, people call this the separation of our model and view
- To do this correctly, we will have two functions, one called `update` that is in charge of update our game model and another called `draw` that updates the view
- Since we will call `update` and `draw` repeatedly, one after another, we put these in a function called `gameLoop`
- The game loop is the loop that will update and draw our game over and over again until the player is done.
  - Note that even though it is called a game *loop*, in this class, we call the game loop with `requestAnimationFrame`, not a formal loop structure. 
  - The reason for this is that in low-level languages where you have to build the threading for the game loop yourself, you traditionally do use a a loop strucuter
- gameLoop formalization 
  - 🔗Additional information: [A blog post about what a game loop is](https://m-abdullah-ramees0916.medium.com/the-game-loop-f6f5cb68c00)
