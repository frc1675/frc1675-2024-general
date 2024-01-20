```mermaid

classDiagram

    class Arm {
        -MotorController leadMotor
        -MotorController followerMotor
        -Encoder encoder
        -LimitSwitch switch
        -PIDController pid
        -double targetAngle

        +getAngle() double
        +getTarget() double
        +getIsOnTarget() boolean
        +setTarget(double angle) void
        +isAtHomePosition() boolean
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

    class LED {
        -MotorController blinkin

        +setPattern(Pattern p)
    }

```