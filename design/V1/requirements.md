# Robot Version 1 Requirements

## Required Subsystems
1. Shoulder - Robot arm movement
2. Hand - End of arm note manipulator and scorer
3. Undertaker - Under bumper ground intake
4. Drive - Make the robot go forward (with swerve)
5. Vision - Handle limelight computation

## Subsystem Responsibilities

### Shoulder Requirements

Hardware: 1 or 2 linked motors, external encoder
Sensing: Arm angle 
Public states: Arm is on target

### Hand Requirements

Hardware: Feeding motor, shooting motor, rangefinder
Sensing: Note location, Shooter speed
Public states: Note ready, Shooter ready, Ready to shoot (composite of the previous two) 

### Undertake Requirements

Hardware: Intake motor
Sensing: Note location sensor
Public states: Note collected