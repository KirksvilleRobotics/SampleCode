# Autonomous Specific

## Basic Structure
Because field starting positions and team allignment can vary, more than one Autonomous program should be created, but inheritance should be used so you keep each program updated and code shorter.

*If you don't know what inheritance is or how to implement it in code, research it. A basic understanding of it is useful outside of robotics.*

In short, one main, abstract, and autonomous program should be made to house all the methods you will use no matter the robot's oreientation. Smaller, child programs should be made for every starting position.

Unlike TeleOp, Autonomous only has one main method, `runOpMode`. The method is linear so once it ends the program does. Think of the method in steps/sections...

**1 Initilization**

