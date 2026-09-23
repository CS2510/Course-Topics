## 💡New Idea: Controlled Scene Changes
- We don't want to change the scene in the middle of an update loop.
- Instead, we want to update the next time we start a frame in the game loop
- By tracking the next scene in SceneManager, we can wait to make the change at the appropriate time.
- We can also do additive scene creation, i.e., adding the game objects of a scene on top of the current scene
  - This allows us to compose scenes out of multiple scenes.
  - When we do this, our scenes look consistent, and it is easy to update a large game.

