
## 💡New Idea: Vector Operations
- In order to do collisions, we need to be able to do lot of different operations on vectors
- `add` adds two vectors together
- `minus` subtracts two vectors
- `magnitude` is a property (getter) that returns the length of the vector
  - The length of a vector is the square root of the sum of the squares of its components
- `normalize` returns a vector that has a length of one
  - We do this by dividing `x` and `y` by the magnitude of the vector
- `orthogonal` returns a vector that is orthogonal (perpendicular) to the given vector

## 💡New Idea: Vector Multiplication
- There are three basic ways to multiply vectors in game programming: `times`, `scale`, and `dot`
  - We can also do a cross product, but we don't need that for collision detection

$$ v\ times\ s = (v_{x}*s, v_{y}*s)$$
$$ v_1\ scale\ v_2=(v_{1x}*v_{2x}, v_{1y}*v_{2y})$$
$$ v_1\ dot\ v_2=v_{1x}*v_{2x}+v_{1y}*v_{2y}$$

- We use `times` when we want to scale a vector by a single number (a scalar). For example, if I want to make a polygon twice as large in all directions, I would multiply each point in the polygon by one number using `times`
- We use `scale` when we want to scale a vector by another, non-uniform vector. For example,  if I want to make a square a rectangle, I would multiple each point in the square by a non-uniform vector using `scale`. The `scale` function is similar to the mathematical idea of component-wise multiplication.
- We use `dot` when we need to find the similarity between two vectors or project one vector onto another vector. For example, if I want to know if the heading of an enemy is nearly the same direction as the heading toward the player, I would multiple those two vectors using `dot`. As another example, if I want to project vector 1 on vector 2, I would multiple those two vectors using `dot`.
  - When two vectors have an identical heading, their dot product is 1. If there are orthogonal, their dot product is 0. If they are pointing in opposite directions, then the dot product will be -1.
  - Additional information can be found here: https://en.wikipedia.org/wiki/Dot_product