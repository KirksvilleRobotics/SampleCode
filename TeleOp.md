# TeleOp Specific

### Basic Structure
A TeleOp program should have two basic functions, `init()` and `loop()`.

`init()` is for settings up motors, sensors, and servos.

`loop()` is the code the robot runs through millions of times a second. In the loop you are checking for conditions and acting upon them.

  i.e. "if buttonA is pressed, run this motor"
  
Because TeleOp is recursive, it is easy to repeatedly assign motor and servo values, changing values faster than is practical. What helps is keeping the assigning to the end of the loop, in one place. Save the current speed or position you want in a variable to use later, that way every time you find a new value you want to set the motors or servos to, they don't spaz out.

### Gampad Controls
`gamepad1` or `gamepad2` refers to the first and second gamepads respectively. You cannot use those names all by itself, you must append a button, stick, or switch to it you want to check.

  i.e. `gamepad1.a` refers to the A button on the first controller.
  
Buttons, bumpers, or the top hat (d-pad) represent a boolean value. They are `true` if the corisponding control is activated and `false` if it isn't.

The left and right sticks and triggers return an floating point from `-1.0` to `1.0`. In code the library's treat the stick's y-postion and x-postion as two seperate inputs. `1.0` if the stick is all the way down or all the way to the left, and `-1.0` if the stick is all the way up or all the way right. You **shouldn't** check the sticks against a hard value like `-1.0` or `1.0` because the stick feedback can be imprecise. You **should** instead use a range of values so the code actually activates.
