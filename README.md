# PID2
An easy to understand PID library for arduino
***************************************************************
* Arduino PID2 Library - Version 2.0.0
* by Steve Edmonds <steve@edmondsfamily.co.nz
* update of original PID by Brett Beauregard <br3ttb@gmail.com> brettbeauregard.com
*
* This Library is licensed under the MIT License
***************************************************************
This update consists of the following changes.
 - Addition of a proportional band
   PID control is active within a band centred about the setpoint, output is 100%
   below or 0% above this band.
   outside this band, allowing faster initial response.
 - Changes to make kp, ki, kd independant of the sample (compute repeat) time.
 - Normalisation of the input (wrt the proportional band) and output so output
   is in the range 0 to 1.
 - This is a simple PID controller that works well in many situations. There are many
   variations of PID control and initially I found the use of kp, ki and kd strange
   when more familiar with kc, Ti and Td tuning. A good source of information can be found
   at https://www.google.co.nz/books/edition/_/TxKynbyaIAMC?hl=en&gbpv=1 sections 2.2 - 2.4.
 - For an ultra-detailed explanation of why the original code was the way it is, please visit:
   http://brettbeauregard.com/blog/2011/04/improving-the-beginners-pid-introduction/

 - For original function documentation see:  http://playground.arduino.cc/Code/PIDLibrary

 - Updated function list.
     SetMode
     Compute()
     SetOutputLimits
     SetTunings
     SetControllerDirection
     SetSampleTime	         Deprecated.
     GetKp
     GetKi
     GetKd
     GetMode
     GetDirection
