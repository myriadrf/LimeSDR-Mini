Peripheral Interfaces
#####################

LimeSDR Mini board peripheral interfaces interfaces are presented in Figure 8. The latter block diagrams depict the main ICs, corresponding IC pin numbers, data buses and serial protocol addresses.

.. figure:: /images/LimeSDR-Mini_v1.2_LSI.png
  :width: 600

  Figure 8. LimeSDR Mini v1.2 peripheral interfaces block diagram

There are several SPI interfaces with their slave devices:

* FPGA_SPI: this SPI interface are connected to FPGA and slave devices can be accessed by transferring data to internal FPGA NIOS CPU. This bus has these slave devices RFIC (IC1) and DAC (IC9).
* FPGA_QSPI: this SPI interface is connected to Quad SPI flash memory (IC11).
* Internal FPGA SPI module: FPGA has its own SPI module and can be controlled as regular SPI device. By using FPGA SPI it is possible to control FPGA modes etc.
* FPGA_I2C: used to control external clock temperature sensor and EEPROM on LimeSDR-Mini board.

In the tables below are listed FPGA_SPI pins, schematic signal names, FPGA interconnections and I/O standards.

.. list-table:: Table 5. FPGA_SPI interface pins
   :header-rows: 1
   :stub-columns: 1

   * - Schematic signal name
     - FPGA pin
     - I/O standard
     - Comment
   * - FPGA_SPI_SCLK
     - K5
     - 2.5V (3.3V)
     - Serial Clock (FPGA output)
   * - FPGA_SPI_MOSI
     - J7
     - 2.5V (3.3V)
     - Data (FPGA output)
   * - FPGA_SPI_MISO
     - J6
     - 2.5V (3.3V)
     - Data (FPGA input)
   * - FPGA_SPI_LMS_SS
     - J5
     - 2.5V (3.3V)
     - IC1 (LMS7002) SPI slave select (FPGA output)
   * - FPGA_SPI_DAC_SS
     - K8
     - 2.5V (3.3V)
     - IC9 SPI slave select (FPGA output)

In the tables below are listed FPGA_QSPI pins, schematic signal names, FPGA interconnections and I/O standards.

.. list-table:: Table 6. FPGA_QSPI interface pins
   :header-rows: 1
   :stub-columns: 1

   * - Schematic signal name
     - FPGA pin
     - I/O standard
     - Comment
   * - FPGA_QSPI_SCLK
     - F1
     - 1.8V
     - Serial Clock (FPGA output)
   * - FPGA_QSPI_IO0
     - D1
     - 1.8V
     - 
   * - FPGA_QSPI_IO1
     - C1
     - 1.8V
     - 
   * - FPGA_QSPI_IO2
     - B1
     - 1.8V
     - 
   * - FPGA_QSPI_FLASH_SS
     - E1
     - 1.8V
     - FPGA_QSPI_FLASH_SS

n the tables below are listed FPGA_I2C interface slave devices and their other information.

.. list-table:: Table 7. FPGA_I2C interface pins
   :header-rows: 1
   :stub-columns: 1

   * - I2C slave device
     - Slave device
     - I2C address
     - I/O standard
     - Comment
   * - IC8
     - Temperature sensor
     - 1 0 0 1 0 0 0 RW
     - 3.3V
     - LM75
   * - IC10
     - EEPROM
     - 1 0 1 0 0 0 0 RW
     - 3.3V
     - M24128

8 GPIOs from FPGA are connected to 10 pin 0.05” header. Additional 2 pins are dedicated for power. Another 2 GPIOs are connected to 5 header on the board edge. In the tables below are listed FPGA_GPIO (J5) and FPGA_EGPIO (J6) information.

.. list-table:: Table 8. FPGA GPIO connector (J5) pins
   :header-rows: 1
   :stub-columns: 1

   * - Connector pin
     - Schematic signal name
     - FPGA pin
     - I/O standard
     - Comment
   * - 1
     - FPGA_GPIO0
     - A11
     - 3.3V
     - 
   * - 2
     - FPGA_GPIO1
     - B10
     - 3.3V
     - 
   * - 3
     - FPGA_GPIO2
     - C10
     - 3.3V
     - 
   * - 4
     - FPGA_GPIO3
     - D11
     - 3.3V
     - 
   * - 5
     - FPGA_GPIO4
     - E13
     - 3.3V
     - 
   * - 6
     - FPGA_GPIO5
     - F13
     - 3.3V
     - 
   * - 7
     - FPGA_GPIO6
     - F10
     - 3.3V
     - 
   * - 8
     - FPGA_GPIO7
     - G10
     - 3.3V
     - 
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


.. list-table:: Table 9. FPGA GPIO connector (J5) pins
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
     - B7
     - 3.3V
     - 
   * - 3
     - FPGA_EGPIO1
     - D6
     - 3.3V
     - 
   * - 4
     - VCC3P3
     - 
     - 3.3V
     - Power net (3.3V)
   * - 5
     - VCC1P8
     - 
     - 1.8V
     - Power net (1.8V)