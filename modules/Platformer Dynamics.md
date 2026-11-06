

## 💡New Idea: Platformer Dynamics
- Characters can't jump if they aren't grounded
- Characters don't slip through platforms
- Gravity is rarely exactly true gravity
- Characters need a terminal velocity
- Characters often can double jump
- Charcters don't float when they bump their heads

## 👩‍💻Code Together: Platformer Dynamics
- Add an isGrounded variable
  - Set to true when there is a collision below and you are heading down
  - Set velocity to 0
- Add a double jump variable
  - Invert whenever you jump
- Cap downward velocity
- Pick your own gravity
- When you hit something above you and you are going up, set velocity to 0
