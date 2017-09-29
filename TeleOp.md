# TeleOp Specific

### Basic Structure
A TeleOp program should have two basic functions, `init()` and `loop()`.

`init()` is for settings up motors, sensors, and servos.

`loop()` is the code the robot runs through millions of times a second. In the loop you are checking for conditions and acting upon them.

  i.e. "if buttonA is pressed, run this motor"

### Gampad Controls
`gamepad1` or `gamepad2` refers to the first and second gamepads respectively. You cannot use those names all by itself, you must append a button, stick, or switch to it you want to check.

  i.e. `gamepad1.a` refers to the A button on the first controller.
  
Buttons, bumpers, or the top hat (d-pad) represent a boolean value. They are `true` if the corisponding control is activated and `false` if it isn't.

The left and right sticks and triggers return an integer value. `-128` if the stick is all the way down or all the way to the left, and `128` if the stick is all the way up or all the way right. You shouldn't check the sticks against a hard value like...
 
