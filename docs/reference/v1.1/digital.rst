RF Transceiver Digital
######################

The `LMS7002M`_ digital interface and control signals are described below.

Digital Interface
*****************

Digital Interface Signals: LMS7002 is using data bus LMS_DIQ1_D[11:0] and LMS_DIQ2_D[11:0], LMS_ENABLE_IQSEL1 and LMS_ENABLE_IQSEL2, LMS_FCLK1 and LMS_FCLK2, LMS_MCLK1 and LMS_MCLK2 signals to transfer data to/from FPGA. Indexes 1 and 2 indicate transceiver digital data PORT-1 or PORT-2. Any of these ports can be used to transmit or receive data. By default PORT-1 is selected as transmit port and PORT-2 is selected as receiver port. The FCLK# is input clock and MCLK# is output clock for LMS7002M transceiver. TXNRX signals sets ports directions. For LMS7002M interface timing details refer to LMS7002M transceiver datasheet page 12-13. [link].

Control
*******

These signals are used for the following functions within the LMS7002 RFIC:

* LMS_RXEN, LMS_TXEN – receiver and transmitter enable/disable signals connected to FPGA Bank 8 (VDIO_LMS_FPGA; 2.5V).
* LMS_RESET – LMS7002M reset connected to FPGA Bank 7 (VDIO_LMS_FPGA; 2.5V).
* SPI Interface: LMS7002M transceiver is configured via 4-wire SPI interface; FPGA_SPI_SCLK, FPGA_SPI_MOSI, FPGA_SPI_MISO, FPGA_SPI_LMS_SS. The SPI interface controlled from FPGA Bank 2 (VDIO_LMS_FPGA; 2.5V).
* LMS I2C Interface: can be used for LMS EEPROM content modifying or for debug purposes. The signals LMS_I2C_SCL, LMS_I2C_DATA connected to FPGA Bank 2 (VDIO_LMS_FPGA; 2.5V).

LMS7002M Pins
*************

.. list-table:: Table 2. LMS7002M RF transceiver digital interface pins
   :header-rows: 1
   :stub-columns: 1

   * - Chip pin (IC1)
     - Chip reference (IC1)
     - Schematic signal name
     - FPGA pin
     - FPGA I/O standard
     - Comment
   * - E5
     - xoscin_tx
     - TxPLL_CLK
     - 
     - 1.8V
     - Connected to 40.00 MHz clock
   * - AB34
     - MCLK1
     - LMS_MCLK1
     - G5
     - 2.5V
     - 
   * - AA33
     - FCLK1
     - LMS_FCLK1
     - L3
     - 2.5V
     - 
   * - V32
     - TXNRX1
     - LMS_TXNRX1
     - J8
     - 2.5V
     - 
   * - U29
     - TXEN
     - LMS_TXEN
     - K6
     - 2.5V
     - 
   * - 1Y32
     - ENABLE_IQSEL1
     - LMS_ENABLE_IQSEL1
     - M8
     - 2.5V
     - 
   * - AG31
     - DIQ1_D0
     - LMS_DIQ1_D0
     - M12
     - 2.5V
     - 
   * - AF30
     - DIQ1_D1
     - LMS_DIQ1_D1
     - N12
     - 2.5V
     - 
   * - AF34
     - DIQ1_D2
     - LMS_DIQ1_D2
     - N10
     - 2.5V
     - 
   * - AE31
     - DIQ1_D3
     - LMS_DIQ1_D3
     - L10
     - 2.5V
     - 
   * - AD30
     - DIQ1_D4
     - LMS_DIQ1_D4
     - M10
     - 2.5V
     - 
   * - AC29
     - DIQ1_D5
     - LMS_DIQ1_D5
     - M13
     - 2.5V
     - 
   * - AE33
     - DIQ1_D6
     - LMS_DIQ1_D6
     - N9
     - 2.5V
     - 
   * - AD32
     - DIQ1_D7
     - LMS_DIQ1_D7
     - N8
     - 2.5V
     - 
   * - AC31
     - DIQ1_D8
     - LMS_DIQ1_D8
     - M7
     - 2.5V
     - 
   * - AC33
     - DIQ1_D9
     - LMS_DIQ1_D9
     - N7
     - 2.5V
     - 
   * - AB30
     - DIQ1_D10
     - LMS_DIQ1_D10
     - M9
     - 2.5V
     - 
   * - AB32
     - DIQ1_D11
     - LMS_DIQ1_D11
     - N6
     - 2.5V
     - 
   * - AM24
     - xoscin_rx
     - RxPLL_CLK
     - -
     - 1.8V
     - Connected to 40.00 MHz clock
   * - P34
     - MCLK2
     - LMS_MCLK2
     - H4
     - 2.5V
     - 
   * - R29
     - FCLK2
     - LMS_FCLK2
     - M3
     - 2.5V
     - 
   * - U31
     - TXNRX2
     - LMS_TXNRX2
     - H5
     - 2.5V
     - 
   * - V34
     - RXEN
     - LMS_RXEN
     - M11
     - 2.5V
     - 
   * - R33
     - ENABLE_IQSEL2
     - LMS_ENABLE_IQSEL2
     - N3
     - 2.5V
     - 
   * - H30
     - DIQ2_D0
     - LMS_DIQ2_D0
     - M2
     - 2.5V
     - 
   * - J31
     - DIQ2_D1
     - LMS_DIQ2_D1
     - M4
     - 2.5V
     - 
   * - K30
     - DIQ2_D2
     - LMS_DIQ2_D2
     - M1
     - 2.5V
     - 
   * - K32
     - DIQ2_D3
     - LMS_DIQ2_D3
     - J1
     - 2.5V
     - 
   * - L31
     - DIQ2_D4
     - LMS_DIQ2_D4
     - N2
     - 2.5V
     - 
   * - K34
     - DIQ2_D5
     - LMS_DIQ2_D5
     - K1
     - 2.5V
     - 
   * - M30
     - DIQ2_D6
     - LMS_DIQ2_D6
     - L2
     - 2.5V
     - 
   * - M32
     - DIQ2_D7
     - LMS_DIQ2_D7
     - J2
     - 2.5V
     - 
   * - N31
     - DIQ2_D8
     - LMS_DIQ2_D8
     - N4
     - 2.5V
     - 
   * - N33
     - DIQ2_D9
     - LMS_DIQ2_D9
     - K2
     - 2.5V
     - 
   * - P30
     - DIQ2_D10
     - LMS_DIQ2_D10
     - L5
     - 2.5V
     - 
   * - P32
     - DIQ2_D11
     - LMS_DIQ2_D11
     - L4
     - 2.5V
     - 
   * - U33
     - CORE_LDO_EN
     - LMS_CORE_LDO_EN
     - N11
     - 2.5V
     - 
   * - E27
     - RESET
     - LMS_RESET
     - L1
     - 2.5V
     - 
   * - D28
     - SEN
     - FPGA_SPI_LMS_SS
     - J5
     - 2.5V
     - SPI interface
   * - C29
     - SCLK
     - FPGA_SPI_SCLK
     - K5
     - 2.5V
     - SPI interface
   * - F30
     - SDIO
     - FPGA_SPI_MOSI
     - J7
     - 2.5V
     - SPI interface
   * - F28
     - SDO
     - FPGA_SPI_MISO
     - J6
     - 2.5V
     - SPI interface
   * - D26
     - SDA
     - LMS_I2C_SDA
     - N5
     - 2.5V
     - Connected to EEPROM
   * - C27
     - SCL
     - LMS_I2C_SCL
     - M5
     - 2.5V
     - Connected to EEPROM