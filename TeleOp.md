# TeleOp Specific

### Basic Structure
A TeleOp program should have two basic functions, `init()` and `loop()`.
`init()` is for settings up motors, sensors, and servos.

`loop()` is the code the robot runs through millions of times a second.
In the loop you are checking for conditions and acting upon them.
  i.e. `if buttonA is pressed, run this motor`


### Motors
DcMotor is the class that holds information and functions for the basic motors.

Initialize: `DcMotor motorName;`
You should do this outside a method so that it is global (can be used from anywhere).

Assign: `motorName = hardwareMap.get(DcMotor.class, "motorName");`
It's best to do this in `init()` when you setting up the robot's configuration.
`hardwareMap` is used to assign a specific motor to the program's motor.
Make sure `motorName` should be the same in both the phone and the code.

Run: `motorName.setPower(1.0);`
`setPower()` is the function to set a motors power. Once you set power it will stay runnign till you set it to 0.0.
`setPower()` takes a float from 0.0-1.0, 0.0 being 0% power and 1.0 being 100%.
