# Task 05 – Relative Velocity

## Problem Statement

A river flows east at $2 \text{ m/s}$. A boat that can travel at $5 \text{ m/s}$ in still water wants to go directly north across the river. In what direction (angle) should it head? How long will it take to cross the river if it's 200 meters wide?

## Theory

This is an application of relative velocity in two dimensions. The velocity of the boat relative to the shore ($\vec{v}_{bs}$) is the vector sum of the velocity of the boat relative to the water ($\vec{v}_{bw}$) and the velocity of the water relative to the shore ($\vec{v}_{ws}$).

$$
\vec{v}_{bs} = \vec{v}_{bw} + \vec{v}_{ws}
$$

To travel directly north, the east-west component of the boat's net velocity must be zero.

## Step-by-Step Solution

### Defining the Vectors

Let north be the $+y$ direction and east be the $+x$ direction.

$$
\vec{v}_{ws} = (2, 0) \text{ m/s}
$$

The boat must head at an angle $\theta$ west of north to counteract the river's current. 

$$
\vec{v}_{bw} = (-5 \sin(\theta), 5 \cos(\theta)) \text{ m/s}
$$

### Finding the Angle

The resultant velocity vector $\vec{v}_{bs}$ must only have a $y$ component:

$$
\vec{v}_{bs} = (-5 \sin(\theta) + 2, 5 \cos(\theta))
$$

Set the $x$ component to zero:

$$
-5 \sin(\theta) + 2 = 0
$$

$$
\sin(\theta) = \frac{2}{5} = 0.4
$$

$$
\theta = \arcsin(0.4) \approx 23.58^\circ
$$

The boat must head $23.58^\circ$ west of north.

### Crossing Time

The net speed of the boat in the northward direction is the $y$ component of $\vec{v}_{bs}$:

$$
v_{north} = 5 \cos(23.58^\circ) = 5 \sqrt{1 - \sin^2(\theta)} = 5 \sqrt{1 - 0.4^2} = 5 \sqrt{0.84} \approx 4.58 \text{ m/s}
$$

The time to cross the 200 m wide river is the distance divided by the northward velocity:

$$
t = \frac{d}{v_{north}} = \frac{200}{4.58} \approx 43.6 \text{ s}
$$

## Final Result

* Heading angle: $23.58^\circ$ west of north.
* Crossing time: $43.6 \text{ s}$.

## Interpretation

The boat sacrifices some of its forward speed relative to the water to overcome the lateral push of the river. As a result, its effective speed across the river ($4.58 \text{ m/s}$) is less than its speed in still water ($5 \text{ m/s}$).
