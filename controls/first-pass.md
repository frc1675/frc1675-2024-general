# First Pass Controls
These are the robot controls for driver tryouts.

## Driver

### Responsibility
The driver is responsible for moving the robot around the field and shooting.

### Controls
- Left stick: Robot translation - Field relative
- Right stick: Robot rotation
- Right trigger: Spin up and shoot - Speeds are adjusted based on arm angle


## Operator

### Responsibility
The operator is responsible for placing the arm in the correct positions, and manually stopping the intake if necessary. 

### Controls
- Right trigger: Move arm to home position
- Left trigger: Move arm to amp score position
- Y Button: Disable intake
- A Button: Enable intake if disabled

## Automatic Control
These are events which happen automatically based on sensory input

| Event | Robot Action | Rationale |
| ----- | ------------ | --------- |
| Arm is not in home position | Intake is disabled | We want to avoid intaking note when indexer is not present |
| Note is detected within indexer | Intake is disabled | We want to avoid intaking when we already have a note since this is illegal |
| Arm is extended to amp position | Drivetrain is slowed down | We want to avoid tipping, so we slow down when the center of gravity changes |

Finally, the intake should always be running if no stop condition of the intake is meet. 

