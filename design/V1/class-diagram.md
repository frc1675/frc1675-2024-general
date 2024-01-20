```mermaid

classDiagram

    class Arm {
        -MotorController leadMotor
        -MotorController followerMotor
        -Encoder encoder
        -PIDController pid
        -double targetAngle

        +getAngle() double
        +getTarget() double
        +getIsOnTarget() boolean
        +setTarget(double angle) void
    }

    class Shooter {
        -MotorController feedMotor
        -MotorController shootMotor
        -LaserCAN noteSensor
        -double targetSpeed

        +isNoteInFeeder() boolean
        +isShooterAtTargetSpeed() boolean
        +isShooterReady() boolean

        +setTargetShooterSpeed(double speed) void
        +setFeederSpeed(double speed) void
    }

    class Undertaker {
        -MotorController motor

        +setSpeed(double speed) void
    }

```