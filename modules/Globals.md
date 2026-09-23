## 💡New Idea: Communication - Communicate across scenes
- We can't directly communicate between components on different scenes
- Instead we communicate indirectly
- One way to communicate indirectly is with `Globals`
- By setting a static variable on `Globals`, components in other scenes can query than variable.
- For example, we can add points to a game by adding a points variable to Globals