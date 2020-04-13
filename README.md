# AAE_Notebook_033_ControlDesign

## Controller Design

We covered the roll-pitch controller first because it's the most mathematically complex of the controllers and we wanted to stay focused on the math of 3d rotations. However, this isn't the first controller we would implement if we were implementing this architecture from scratch. 

The inner-loop controls operate on a faster time scale than the outer loop, so we'd implement and tune them first. 

If we were just looking at the altitude controller, roll-pitch controller, and body-rate controller, in what sequence would we implement the controllers?
 
  1. Body-Rate Controller. Once you could rely on the controller to hit its roll, pitch, yaw-rate commands, then we'd implement step two, roll-pitch command.
  2. Roll-Pitch Controller. To do this in practice, we manually control the thrust to roughly counteract gravity.
  3. Altitude Controller, as it's critical in avoiding crashes.

A good sequence in which to implement each of the controllers would be as follows:

  1. Body-Rate Controller
  2. Roll-Pitch Controller
  3. Altitude Controller
  4. Lateral Controller
  5. Yaw Controller

***   ***   ***   ***   ***   ***   ***   ***   ***

See [solution.py](https://github.com/FadedIllusions/AAE_Notebook_033_ControlDesign/blob/master/solution.py) for complete solution implementation.
