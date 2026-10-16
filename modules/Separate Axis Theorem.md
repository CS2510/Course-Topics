## 💡New Idea: Separate Axis Theorem
- Consider a point and a polygon. How do I know if the point is inside the polygon?
- What if I had a light that I shown on the point and line. If I can find a position for the light where the shadow of the point and polygon are not overlapping, then they can't be in collision.
- There are infinite positions for the "light". Smart mathematicials that shown that if we shine the light in the direction orthogonal to all the lines in the polygon, we have checked enough "lights"
- This does not work with concave polygons.
  - We can use Separate Axis Theorem if we break the polygon into sub-polygons, but that is out of scope for this project.


## 💡New Idea: Implementing the Separate Axis Theorem
- Working backward, write a function that takes points projected onto a line. Think of them as points that represent shadows. Can I determine if one point is between all the other points (the collision point and the projection of the polygon)
  - See if the point is between the min and max of the other points
- Given a direction of a "flashlight", can I determine if a point is in collision with a polygon
  - Project the point and polygon vertices onto a line perpendicular to the direction of the flashlight. See if there is an overlap
- Given a point and polygon, can I determine if there is any overlap?
  - Project the point and vertices onto the lines that are perpendicular to the edges of the polygon. Look for overlap.
- Given a point and a game object, can I determine if there is any overlap?
  - Move the vertices in the Polygon component based on the Transform component. Then see if there is any overlap.