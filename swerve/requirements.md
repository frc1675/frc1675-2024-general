# Swerve Drive Standards
This document outlines what a correctly functioning swerve drive behaves like.

## Basic Functionality
- Modules drive at the same speed and in the same direction.
- Modules rotate to a zero position. 
- Modules zero positions line up with each other.
- Modules rotate in sychronization with each other. (Module angles are the same relative to the zero positon).

## Driving 
- Drive chassis can translate in all directions from a stopped position.
- Drive chassis can rotate without translating.
- Drive chassis can translate while rotating.
- Drive chassis can accelerate and declerate without tipping.
- Drive chassis has minimal noitceable input lag / acceleration time. 
- Drive chassis does not drift while translating. 

## Autonomous Movement
- Drive chassis can autonomously translate in a straight line.
- Drive chassis can autonomously translate through a Bezier curve (use PathPlanner).
- Drive chassis can autonomously translate in a rectangle shape to its starting position. 