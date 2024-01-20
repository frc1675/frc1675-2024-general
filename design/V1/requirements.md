# Robot Version 1 Requirements

## Required Subsystems
1. Arm - Robot arm movement
2. Shooter - End of arm note manipulator and scorer
3. Undertaker - Under bumper ground intake
4. Drive - Make the robot go forward (with swerve)
5. Vision - Handle limelight computation
6. LED - Handle LED state

## Subsystem Responsibilities

### Arm Requirements

- Hardware: 1 or 2 linked motors, external encoder
- Sensing: Arm angle, hardstop sensor 
- Public states: Arm is on target

### Shooter Requirements

- Hardware: Feeding motor, shooting motor, rangefinder 
- Sensing: Note location, Shooter speed 
- Public states: Note ready, Shooter ready, Ready to shoot (composite of the previous two) 

### Undertaker Requirements

- Hardware: Intake motor
- Sensing: None
- Public states: None

### LED Requirements

- Hardware: REV Blinkin
- Sensing: None
- Public states: None