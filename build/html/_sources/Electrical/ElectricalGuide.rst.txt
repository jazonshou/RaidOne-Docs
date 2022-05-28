################
Electrical Guide
################

Alright, so you've decided to do electrical shenanigans for Raid One. First, some Raid One 
wiring history. In 2022, Raid One ranked 33 out of 35 teams in the Taiwan regional. Why? Because
our wiring kept dying. So this time around, try to make the wiring more resistant to bumps and 
vibrations. 

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
power jack in case one power source is ever disconnected (P.S. Raid One was frozen for ~2 
matches because of a radio issue… although it wasn’t related to a power issue, this still 
shows how important it is to keep the radio safe).


CAN Protection
==============

In some ways, CAN is your best friend because it opens a realm of near-limitless freedom 
to programmers. On the other hand, since all CAN devices are daisy chained, one poor connection 
can cause the disconnection of all other CAN devices down the line. Thus, here are some ways 
to protect your CAN devices:

* Keep the drive train motor controllers at the front of the CAN bus 
* Use CANivore's to create seperate CAN buses that can connect directly to the USB protect on
  the Roborio
* Make sure there are no dangling cables 
* When stripping CAN wires, make sure you don't also remove the little metal wires on the inside. 
  If you do, it might cause a bad connection. 

In general, as long as you treat your electrical components & wiring with respect, they CAN 
also treat you with respect. 