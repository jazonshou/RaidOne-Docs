############################
Oh no! The bot doesn't move!
############################

Oh no, so sad, truly some unfortunate news... luckily for you, the bot was not supposed to move!

Setting up the code:
====================

1. Set the path as a long (~half the field) straight line.
2. Go to ``Constants.java`` and change ``Constants.AutoConstants.MAX_VEL`` and 
   ``Constants.AutoConstants.MAX_ACCEL`` to something reasonable (it really depends on how 
   fast the chassis is. But try to keep it at a safe speed)
3. Set ``Constants.ChassisConstants.kV`` to a small number like ``0.5``

Now you're basically ready to go! But in order to tune effectively, we need to see how 
the bot reacts to different inputs. Thus, we can use Glass to view velocity graphs. 

Setting up Glass: 
=================

1. Open up WPIlib Glass
2. Configure these settings and click apply

.. image:: ../images/glass_setup.PNG

.. note:: 
    Make sure to change "Team/IP" to your correct team number

3. Go to "Plot" in the toolbar and select "New Plot Window"
4. Click "Add Plot"
5. Do steps 3 & 4 twice to add 2 plots
6. From the "NetworkTables" tab, drag and drop "actual left vel" and "desired left vel" to 
   one of the plots and "actual right vel" and "desired right vel" to the other plot
7. Now, all the velocities will be graphed when you run the path. 

Running the Code and Tuning:
============================

Now your ready to run the code!


Keep running the code until the max actual velocity is around the same place as the max 
desired velocity. 

.. image:: ../images/tuning/untuned.PNG

And then... 

.. image:: ../images/tuning/kv.PNG

Next we will tune the kA. Keep tuning the KA until the accerlation and deceleration parts of 
the profile matches between the actual and desired velocities. It should end up like this: 

.. image:: ../images/tuning/ka.PNG

Next we will tune the kP. Keep tuning the kP until the actual graph matches the desired graph 
even better. 

.. image:: ../images/tuning/kp.PNG

.. note:: 
    It is okay if the robot does not drive straight. We will correct this later on. 

Wow, now that you are done tuning, life is good because now you can basically make the chassis 
follow any path!


Wait, but the robot doesn't drive straight...? 

Adding the Secret Sauce (aka. Ramsete)
======================================

What Ramsete does is that it looks at the robot's current position and corrects its velocities
based on the readed position. Though, there's a reason why this is called the "Secret Sauce." 
Although Ramsete makes your paths extremely accurate, the math does not add up. 

.. image:: ../images/ramsete.jpg

"If it works it works"