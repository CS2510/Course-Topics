## 💡New Idea: Communication - Find a component on a game object
- We often need to communicate within a game object
- If two components share a game object, they can communicate with `this.gameObject.getComponent()`
- `getComponent` returns a component of a given type using `instanceof`