## 💡New Idea: Games are Drawn with a Camera
- Early games didn't have a camera
- Some puzzle games don't have a camera
- But most everything else does

## 👩‍💻Code Together: Cameras
- Add a Camera component to the engine
  - Add a Camera.main getter that returns a game object named Camera
- In the Scene constructor, add a Camera game object with a Camera component as the first item
- Before you render, apply the **inverse** of the camera transform
- Make the camera follow a game object in a game

## 💡New Idea: UI Layers are drawn above the camera
- UI element move with our current setup

## 👩‍💻Code Together: Stationary UI Layer
- When rendering, filter out the UI layer from the main render loop
- After restoring from the main render loop, separately render the game objects on the UI Layer


## 🖼️Activity: Look at the Camera in Super Smash Bros for Cameras
- Start about :45 - [Super Smash Bros Ultimate, 4 Players](https://www.youtube.com/watch?v=QrZn4trMK_U)

## 💡New Idea: Cameras need several properties to look good
- Cameras should not go out of boundaries
- The camera should give the player some leeway

## 👩‍💻Code Together: Camera properties
- Clamp the position of the camera to be within certain bounds
- Only move the camera if it is offset from the goal by a certain amount
- Add a Mathf class with a clamp function
  - Similar to the Mathf functions in Unity.