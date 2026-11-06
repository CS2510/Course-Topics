## New Idea: Rigid Body Dynamics
- In our rigid body component, we can add a velocity property
- In the rigid body's update function, we change the position by the velocity times `Time.deltaTime`
- We can also add acceleration, which we will call gravity.
- In the rigid body's update function, we change the velocity by gravity times `Time.delatTime`
- Note that this satisfies Netwon's first and second law of motion