JTAG
####

To debug FPGA design, flash bitstream to FPGA and/or Flash memory JTAG header J4 or edge connector J3 are used. 

JTAG header located on the PCB top side and attaches to the programmer using 10-pin, 0.05” spaced JTAG connector. By default its is not populated. JTAG header pins, schematic signal names, FPGA interconnections and I/O standards are listed in Table 10.

.. list-table:: Table 10. JTAG header J4 pins
  :header-rows: 1
  :stub-columns: 1

  * - Connector pin
    - Schematic signal name
    - FPGA pin
    - I/O standard
    - Comment
  * - 1
    - FPGA_JTAG_TCK
    - G2
    - 1.8 V
    - Test Clock
  * - 2
    - GND
    - 
    - 
    - Ground
  * - 3
    - FPGA_JTAG_TDO
    - F6
    - 1.8 V
    - Test Data Out
  * - 4
    - VCC1P8
    - 
    - 1.8 V
    - Power (1.8 V)
  * - 5
    - FPGA_JTAG_TMS
    - G1
    - 1.8 V
    - Test Mode Select
  * - 6
    - NC
    -
    - 
    - No connection
  * - 7
    - NC
    -
    - 
    - No connection
  * - 8
    - NC
    -
    - 
    - No connection
  * - 9
    - FPGA_JTAG_TDI
    - F5
    - 1.8 V
    - Test Data In
  * - 10
    - GND
    -
    -
    - Ground

JTAG edge connector J3 located on the PCB top side and attaches to the programmer using 7-pin, 0.1” spaced JTAG connector. By default its is not populated. JTAG edge connector pins, schematic signal names, FPGA interconnections and I/O standards are listed in Table 11.

.. list-table:: Table 11. JTAG edge connector J3 pins
  :header-rows: 1
  :stub-columns: 1

  * - Connector pin
    - Schematic signal name
    - FPGA pin
    - I/O standard
    - Comment
  * - 1
    - GND
    - 
    - 
    - Ground
  * - 2
    - FPGA_JTAG_TCK
    - G2
    - 1.8 V
    - Test Clock
  * - 3
    - FPGA_JTAG_TDO
    - F6
    - 1.8 V
    - Test Data Out

  * - 4
    - FPGA_JTAG_TMS
    - G1
    - 1.8 V
    - Test Mode select
  * - 5
    - FPGA_JTAG_TDI
    - F5
    - 1.8 V
    - Test Data In
  * - 6
    - VCC1P8
    - 
    - 1.8 V
    - Power (1.8 V)
  * - 7
    - VCC5P0_USB
    - 
    - 5.0 V
    - Power (5.0 V)