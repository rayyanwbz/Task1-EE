Introduction:

This Arduino sketch defines the behavior of a hexapod robot's legs through servo motors. It sets initial positions for each joint and provides functions to execute movements like walking forward, backward, turning left, and turning right.


Explanation:

1-Servo Initialization:

-Six servo objects (hipLeft, kneeLeft, ankleLeft, hipRight, kneeRight, ankleRight) are defined using the Servo library. Each represents a joint of a leg.

2-Servo Pins:

-Pins for each servo are defined (hipLeftPin, kneeLeftPin, etc.) to which the servo motors are connected.

3-Initial Positions:

-Initial angles (hipCenter, kneeCenter, ankleCenter) are set to 90 degrees for each joint, positioning the legs initially at a neutral stance.

4-Movement Functions:

-moveJoint(int legNumber, int jointNumber, int angle): Moves a specific joint (hip, knee, or ankle) of a given leg (1 for left, 2 for right) to a specified angle.

-moveLeg(int legNumber, int angles[3]): Moves all joints of a leg (hip, knee, ankle) simultaneously using an array of angles.

5-Walking Functions:

-walkForward(): Performs a sequence to simulate walking forward:
Lifts one leg, moves it forward, adjusts the other leg for balance, and repeats for the other leg.

-walkBackward(): Similar sequence but moves backward.

6-Turning Functions:

-turnLeft() and turnRight(): Rotate the hips of the legs to simulate turning left or right.

7-Setup Function (setup()):

-Attaches each servo object to its corresponding pin and initializes all servos to their initial positions (hipCenter, kneeCenter, ankleCenter).

8-Loop Function (loop()):

-Executes the walkForward() function repeatedly to demonstrate forward walking motion. Adjustments can be made to include user input or sensor data to control different movements.
