#################
Code Organization
#################

Before we begin with actual programming, first you need to understand how Raid One (and Raid 
Zero) code is organized. 

Submodules
==========

Every submodule should be organized in its own class which inherits from the Submodule 
class. For your custom features to work, you need to override methods from the Submodule class. 
Here are brief explainations of what each method in submodule does: 

On Init
*******

.. code-block:: java
    :linenos:

    @Override
    public void onInit() {}

This method only runs once at the start of robot code execution. Most things that usually happen
in a java constructor should run here. 

On Start
********

.. code-block:: java
    :linenos:

    @Override
    public void onStart(double timestamp) {}

This method runs once at the start of autonomous and teleop. ``timestamp`` is the time in seconds
since initialization. 

Update
******

.. code-block:: java
    :linenos:

    @Override
    public void update(double timestamp) {}

This method reads cached inputs & calculate outputs (and yes it is basically identical to ``run()``). 
``timestamp`` is the time in seconds since initialization.

Run
***

.. code-block:: java
    :linenos:

    @Override
    public void run() {}

This method runs components in the submodule that have continuously changing inputs (and yes 
it is basically identical to ``update(double timestamp)``). 

Stop
****

.. code-block:: java
    :linenos:

    @Override
    public abstract void stop() {}

This method runs when the robot gets disabled. 

Zero
****

.. code-block:: java
    :linenos:

    @Override
    public void zero() {}

This method zeros all sensors. 

.. note:: 
    When you make a new submodule, you must add it to ``Robot.java``: 

    .. code-block:: java
        :emphasize-lines: 6

        @Override
        public void robotInit() {
            // Register all submodules here
            submoduleManager.setSubmodules(
                superstructure, 
                PUT_YOUR_SUBMODULES_HERE
            );
            submoduleManager.onInit();

            autoRunner = new AutoRunner();
        }