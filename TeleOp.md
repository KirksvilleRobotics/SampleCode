# TeleOp Specific

### Basic Structure
A TeleOp program should have two basic functions, `init()` and `loop()`.
`init()` is for settings up motors, sensors, and servos.

`loop()` is the code the robot runs through millions of times a second.
In the loop you are checking for conditions and acting upon them.
  i.e. `if buttonA is pressed, run this motor`
