################
Electrical Guide
################

So you've decided to be a part of the Raid One electrical team. First, some Raid One history. 
In 2022, Raid One ranked 33 out of 35 teams in the Taiwan regional. Why? Because
our wiring kept dying. So try to make the wiring more resistant to bumps and vibrations. 

Electrical Layout
=================

.. figure:: ../images/frc-control-system-layout-rev.svg
    :alt: Electrical Layout
    :width: 750

Redundancy
==========

Try to make things redundant. For instance, the radio can be powered in 2 different ways. 
One way is through the barrel power jack. Another way is through POE (power over ethernet). 
In scenarios like this, it is better practice powering the radio through POE AND the barrel 
power jack in case one power source is ever disconnected.

CAN Protection
==============

In some ways, CAN is your best friend because it opens a realm of near-limitless freedom 
to programmers. On the other hand, since all CAN devices are daisy chained, one poor connection 
can cause the disconnection of all other CAN devices down the line. Thus, here are some ways 
to protect your CAN devices:

* Keep the drive train motor controllers at the front of the CAN bus 
* Use CANivore's to create seperate CAN buses that connect directly to the USB port on the Roborio
* Zip-tie dangling cables 
* When stripping CAN wires, try not to remove the little metal wires on the inside. 
  If you do, it might cause a bad connection. 

In general, as long as you treat your electrical components and wiring with respect, they CAN 
also treat you with respect. 

Additional information regarding FRC electronics can be found 
`here <https://docs.wpilib.org/en/stable/docs/zero-to-robot/step-1/how-to-wire-a-robot.html>`_.