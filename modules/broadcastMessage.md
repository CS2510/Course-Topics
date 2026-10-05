## 💡New Idea: `broadcastMessage`
- We can simplify calls to all components in a game object with `broadcastMessage`
- `broadcastMessage` calls a given functions on all components with that function


## Four methods of communication
| Method | Code Example| Kind |
|---|---|---|
| Components on the same game objects| `this.gameObject.getComponent(<Type>).key = value` | Tightly Coupled|
| Components on different game objects | `GameObject.find(<Name>).getComponent(<Type>).key = value`| Tightly Coupled |
| Components in different scenes | `Globals.key = value`| Loosely Coupled |
| Event driven | `GameObject.findGameObjectsByType(Transform).broadcastMessage("<Function Name", [<params>])`| Loosely Coupled |