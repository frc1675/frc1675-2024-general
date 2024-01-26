# Shuffleboard PID Tuner
This document outlines how to use the PIDController widget to tune PID controllers.

## What is it?
The PIDController is a widget which is built in to shuffleboard. We can use it to tune the coefficients of a PIDController object via interface.

## How to code
1. Ensure that you have access to your `PIDController` object. Specifically, it should be the wpilib object, not an external PID controller. For example, the `SparkMaxPIDController` object would not work. 
2. Get the shuffleboard tab you would like to use for your subsystem. Typically, the name of the tab is the same as the name of your subsystem. For more information on programming shuffleboard, see the resources section of this document. 
3. Add your `PIDController` to your shuffleboard tab. This should be done with the `.add` method of the tab. After adding, call the `withWidget` method to ensure that the PIDController widget is used with your object.
4. Use your PID controller as normal. Now, the coefficients can be changed at runtime using the shuffleboard to help accelerate tuning. Make sure to update the new constants in code after a tuning session.

### Example Code:
```
public class SomeSubsystem extends SubsystemBase {

    //other subsystem variables
    private PIDController pid;

    public SomeSubsystem() {
        //other setup
        pid = new PIDController(1, 1, 1);
    }

    public void initShuffleboard() {
        Shuffleboard.getTab("Some subsystem").add("PID Tuner", pid).withWidget(BuiltInWidgets.kPIDController);
    }

    //subsystem methods
}
```

## How to use
Once you have written the code, you are ready to tune your PIDController. 
1. Deploy code to the robot as normal.
2. Once you are ready, place the robot in to test mode or the PID controller tuner will not work. You can do this by clicking "Test" in the drivers station before enabling.
3. Open Shuffleboard and click on the tab you created previously. Find the PIDController widget. 
4. Attempt to control your mechanism, change PID constants as needed. To change constants, click on the text boxes on the widget and edit them. Hit enter to apply changes. Note that the robot will automatically disable after changing a constant. This is fine, simply re-enable when ready. 
5. Once you have working constants, make sure to update the in-code constants. 


## Resources
- [PID Control in WPILib](https://docs.wpilib.org/en/stable/docs/software/advanced-controls/controllers/pidcontroller.html)
- [PID Controller JavaDoc](https://first.wpi.edu/wpilib/allwpilib/docs/release/java/edu/wpi/first/math/controller/PIDController.html)
- [BuiltInWidgets JavaDoc](https://first.wpi.edu/wpilib/allwpilib/docs/release/java/edu/wpi/first/wpilibj/shuffleboard/BuiltInWidgets.html#kPIDController)
- [Shuffleboard Programming Basics](https://docs.wpilib.org/en/stable/docs/software/dashboards/shuffleboard/layouts-with-code/index.html)
