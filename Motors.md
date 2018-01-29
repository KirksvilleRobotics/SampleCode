# Motors
`DcMotor` is the class that holds variables and methods for the basic motors.

**Initialize:** `DcMotor motorName;`
You should do this outside a method so that it is global (can be used from any method).

**Assign:** `motorName = hardwareMap.get(DcMotor.class, "motorName");`
It's best to do this in `init()` when you setting up the robot's configuration.
`hardwareMap` is used to assign a specific motor from the phone's config to the program's motor.
Make sure `motorName` is the same in both the phone's config and the code.

**Run:** `motorName.setPower(1.0);`
`setPower()` is the function to set a motors power. Once you set power it will stay running till you set it to `0.0`.
`setPower()` takes a double from `0.0`-`1.0`. `0.0` is 0% power and `1.0` is 100%.
