## 💡New Idea: Game Object Lifecycle - Destroy
- Add `destroy`
  - We don't destroy objects immediately
  - We mark them as having been deleted and remove them at the end of the update cycle
- Filter objects with `markForDelete`
  - Remove objects that have their mark for delete flag set
- Call `onDestroy` on game objects that are destroyed
  - `onDestroy` is the event we call on components when their parent game object is removed