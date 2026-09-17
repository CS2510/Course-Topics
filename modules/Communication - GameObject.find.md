## 💡New Idea: Communication - Find a game object within a scene
- We often need to communicate between components on different game objects
- We start by find the game object in question
  - We use the static function `find` on `GameObject`
  - `find` returns the first game object with a given name
- We then find the component we need to communicate with
  - `GameObject.find(<name>).getComponent(<type>)`