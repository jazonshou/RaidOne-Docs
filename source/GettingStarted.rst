.. _getting_started:

###############
Getting Started
###############

Helpful Resources
=================

The entire purpose of these docs are to make it easy to get started with with code and 
electrical in FRC. Most of these docs are a result of consuming and regurgitating pre-existing 
FRC docs (ex. WPIlib docs) so that a child can understand. A small problem is that some
specific detail may be missed or forgotten through the digestion process, thus, here are some
incredibly helpful resources that can help you when my docs inevitably forget to explain something. 

* `WPIlib <https://docs.wpilib.org/en/stable/index.html>`_: Literally everything programming 
  & electrical related is explained in detail here as long as you're willing to spend the time to read it. 
* `WPIlib API <https://first.wpi.edu/wpilib/allwpilib/docs/release/java/index.html>`_: This API explains 
  in depth about everything that is in the WPIlib.
* `CTRE Phoenix Docs <https://docs.ctre-phoenix.com/en/stable/>`_: The official Phoenix docs 
  are a good place to start. These docs explain concepts quite well but often don't include 
  everything there is in the Phoneix API. 
* `CTRE Phoenix API <https://store.ctr-electronics.com/content/api/java/html/index.html>`_: The Phoenix 
  API provides documentation for literally everything by CTRE (ex. Talon SRX, Victor SPX, and CANifier). 
  This API also offers very direct information when the CTRE docs inevitably fail you. 
* `CTRE Phoenix Example Code <https://github.com/CrossTheRoadElec/Phoenix-Examples-Languages>`_: If you're 
  looking for a quick example of how to use the Phoenix API, this is the place to start.
* `REV Spark Max Docs <https://docs.revrobotics.com/sparkmax/>`_: These docs explain almost everything 
  related to the Spark Max motor controller.
* `REV Spark Max API <https://codedocs.revrobotics.com/java/com/revrobotics/package-summary.html>`_: The Spark 
  Max API provides documentation for everything related to the Spark Max and other REV products (i think). 
  This API also offers very direct information when the REV docs inevitably fail you.
* `REV Spark Max Example Code <https://github.com/REVrobotics/SPARK-MAX-Examples>`_: If you're looking 
  for a quick example of how to use the Spark Max API, this is the place to start.
* `Limelight Docs <https://docs.limelightvision.io/en/latest/>`_: These docs explain almost everything 
  related to the Limelight vision system.

Installation
============

Here is everything you should install for programming (make sure to install the newest version): 

* `WPIlib <https://github.com/wpilibsuite/allwpilib/releases>`_
* `CTRE Phoenix <https://github.com/CrossTheRoadElec/Phoenix-Releases/releases>`_
* `REV Hardware Client <https://docs.revrobotics.com/rev-hardware-client/>`_
* `Pathplanner <https://github.com/mjansen4857/pathplanner/releases>`_
* `Limelight <https://limelightvision.io/pages/downloads>`_
* `Radio Configurator <https://docs.wpilib.org/en/stable/docs/zero-to-robot/step-3/radio-programming.html>`_
* `FRC Game Tools <https://docs.wpilib.org/en/stable/docs/zero-to-robot/step-2/frc-game-tools.html>`_

.. note::
    After installing WPIlib, you will need to install your libraries to the project. 
    `Here <https://docs.wpilib.org/en/stable/docs/software/vscode-overview/3rd-party-libraries.html>`_
    is a short guide on how you can install the vendor libraries. 