this repo contains the code for both the path planning algorithms used for the rover
as well the motor control.


Uptill now the motor control is able to communicate commands generated through the sockets.
the commands are basically generated by modelling a differential drive robot.

Exisiting server code use the velocity forwardBackwardSpeed and leftRightSpeed to rotate the motors.
i have calculated the commands so that existing server code can be used to drive the robot as a differential drive robot.


tested the communication on custom_server.py coded as to run on the pi.
also the file motor_control.py consisits the code in which we give a random linear and angular velocity and the dimensions of the rover
to generate the required velocity commands to be send to the rover which interprets the commands to be vl and vr of the differential drive robot

so now if we want to convert the given velocity commands into pwm signals for the motor then we can simply multiply a constant k in the server code while giving the commands to the motor so
value of k = PWM/velocity
