Reference Clock
###############

The LimeSDR Mini clock system is based on a high stability 40 MHz VCTCXO (Voltage Controlled Temperature Compensated Crystal Oscillator), which can be tuned by the onboard 8-bit DAC (IC9, DAC5311).

The board provides U.FL connectors for reference clock input (J8) and output (J9). The clock input is not connected by default. To use an external reference clock, fit R62 and remove R59, which disconnects the onboard VCTCXO. Clock functions are listed in Table 2.

.. list-table:: Table 2. Clock functions
   :header-rows: 1
   :stub-columns: 1

   * - Function
     - Specification
     - Notes
   * - Onboard oscillator
     - 40 MHz VCTCXO
     - Rakon RTX5032A, ±0.5 ppm stability
   * - External clock input
     - U.FL (J8)
     - 10–52 MHz, 1.8 V–3.3 V, not connected by default
   * - Clock output
     - U.FL (J9)
     - 2.5 V CMOS (VDIO_LMS_FPGA)

.. warning::
   When using external clock references, ensure signal levels and frequencies match specifications.

   Improper clock signals may cause unstable operation and potential damage to the device.
