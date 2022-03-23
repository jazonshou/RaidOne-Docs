###############################
Making the Robot Move in Teleop
###############################

Open up shuffleboard and driver station and enable the robot. 

.. warning::
    **BUT WAIT!!! MAKE SURE THERE IS NO ONE NEAR THE ROBOT WHEN YOU ENABLE. WHEN YOU DO ENABLE, 
    SHOUT "ENABLED" LOUD AND CLEAR TO MAKE SURE EVERYONE AROUND KNOWS THAT THE ROBOT IS ENABLED. 
    THIS IS A VERY IMPORTANT SAFETY PRECAUTION. IF YOU FAIL TO FOLLOW THESE SIMPLE RULES, 
    SEVERE CONSEQUENCES WILL FOLLOW. YOU HAVE BEEN WARNED.**

Make sure that when you push the left joystick forward, the robot moves forward, and when you 
push the left joystick backwards, the robot moves backward. As for turning, when the right 
joystick is pushed left, the robot turns left, and when the right joystick is pushed right, the
robot turns right. 


While testing these features, make sure that the encoder values also correspond to the way the 
robot is moving. If that is not the case, reverse the encoders/motors in ``Chassis.java``. You 
can read encoder readings in shuffleboard. 

.. figure:: ../images/shuffleboard.PNG
    :width: 75%