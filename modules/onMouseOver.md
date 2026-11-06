# New Idea: Mouse Over Events
- The engine will report when the mouse is over a game object
- We need to move the mouse from screen space (pixels) into world space
- We invert the camera matrix and the matrix that moves the origin to the center of the screen
- We then report overlap
- Components can listen for these events to fire