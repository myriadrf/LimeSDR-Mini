Board temperature control
#########################

LimeSDR-Mini has integrated temperature sensor which controls FAN to keep board in operating temperature range. FAN must be connected to J10 (0.1” pitch) connector. FAN control voltage is 5V, but it can be changed to 3.3V by resistors. Fan will be turned on if board will heat up to 55°C and FAN will be turned off if board will cool down to 45°C. By default temperature sensor is unpopulated and FAN is always on.

.. figure:: /images/LimeSDR-USB_1v4_fan_control_hyst.png
  :width: 600
  
  Figure 9: FAN control temperature hysteresis 




