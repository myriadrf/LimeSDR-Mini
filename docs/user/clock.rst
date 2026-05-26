Reference Clock
###############

The LimeSDR Mini clock system is based on a high stability 40 MHz VCTCXO (Voltage Controlled Temperature Compensated Crystal Oscillator) which can be tuned by on-board 10 bit DAC or 16 bit DAC (unpopulated).

The board provides both reference clock input and output U.FL connectors.

.. list-table:: Table 2. Clock Functions
   :header-rows: 1

   * - Function
     - Specification
     - Notes
   * - On-board Oscillator
     - 40 MHz VCTCXO
     - Rakon E7355LF, ±0.5 ppm stability
   * - External Clock Input
     - U.FL (J8)
     - 10-52 MHz, 1.8V - 3.3V
   * - Clock Output
     - U.FL (J9)
     - 3.3V CMOS

.. warning::
   When using external clock references, ensure signal levels and frequencies match specifications. 
   
   Improper clock signals may cause unstable operation and potential damage to the device.

