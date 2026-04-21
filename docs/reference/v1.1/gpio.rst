GPIO Connector
##############

Eight GPIOs from FPGA are connected to 10 pin 0.05” header. Additional 2 pins are dedicated for power.

FPGA_GPIO[7:4] are shared with TX and RX LEDs. Remove solder from solder bridges to disconnect LEDs from GPIOs lines.

FPGA GPIO header (J3) information is listed in Table 12.

.. list-table:: Table 12. FPGA GPIO connector (J3) pins
   :header-rows: 1
   :stub-columns: 1

   * - Connector pin
     - Schematic signal name
     - FPGA pin
     - I/O standard
     - Comment
   * - 1
     - FPGA_GPIO0
     - N15
     - 3.3V
     -
   * - 2
     - FPGA_GPIO1
     - N18
     - 3.3V
     -
   * - 3
     - FPGA_GPIO2
     - N16
     - 3.3V
     -
   * - 4
     - FPGA_GPIO3
     - N17
     - 3.3V
     -
   * - 5
     - FPGA_GPIO4
     - M18
     - 3.3V
     - Shared with FPGA_LED2_G
   * - 6
     - FPGA_GPIO5
     - R18
     - 3.3V
     - Shared with FPGA_LED2_R
   * - 7
     - FPGA_GPIO6
     - T17
     - 3.3V
     - Shared with FPGA_LED3_G
   * - 8
     - FPGA_GPIO7
     - R17
     - 3.3V
     - Shared with FPGA_LED3_R
   * - 9
     - GND
     -
     -
     - Ground pin
   * - 10
     -
     -
     -
     - Selectable power net (3.3V or 5V). Default 3.3V

Additional 2 GPIOs are connected to 5-pin header on the board edge.

FPGA GPIO edge header (J4) information is listed in Table 13. 

.. list-table:: Table 13. FPGA EGPIO connector (J4) pins
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
     - Ground pin
   * - 2
     - FPGA_EGPIO0
     - A10
     - 3.3V
     -
   * - 3
     - FPGA_EGPIO1
     - A8
     - 3.3V
     -
   * - 4
     - VCC3P3
     -
     - 3.3V
     - Power net (3.3V)
   * - 5
     - VCC5P0
     -
     - 5.0V
     - Power net (5.0V)