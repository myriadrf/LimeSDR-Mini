USB 3.0 Controller
##################

Software controls LimeSDR Mini board via the USB 3.0 controller (`FTDI USB 3.0 to FIFO interface bridge chip FT601 <https://ftdichip.com/products/ft600q-b/>`_). The controller signals description showed below:

* FT_D[31:0] – FTDI 32-bit data interface is connected to FPGA.
* FT_TXEn, FT_RXFn, FT_SIWUn, FT_WRn, FT_RDn, FT_OEn, FT_BE[3:0] – FTDI interface control signals.
* FT_CLK – FTDI interface clock. Clock from FTDI is fed to FPGA.

More information about USB 3.0 controller (FTDI) pins, schematic signal names, FPGA interconnections and I/O standards is given in Table 4.

.. list-table:: Table 4. USB 3.0 controller interface
   :header-rows: 1
   :stub-columns: 1

   * - Chip pin (IC6)
     - Chip reference (IC6)
     - Schematic signal name
     - FPGA pin
     - I/O standard
     - Comment
   * - 40
     - DATA_0
     - FT_D0
     - A2
     - 3.3V
     - 
   * - 41
     - DATA_1
     - FT_D1
     - B6
     - 3.3V
     - 
   * - 42
     - DATA_2
     - FT_D2
     - B3
     - 3.3V
     - 
   * - 43
     - DATA_3
     - FT_D3
     - B5
     - 3.3V
     - 
   * - 44
     - DATA_4
     - FT_D4
     - A3
     - 3.3V
     - 
   * - 45
     - DATA_5
     - FT_D5
     - B4
     - 3.3V
     - 
   * - 46
     - DATA_6
     - FT_D6
     - E6
     - 3.3V
     - 
   * - 47
     - DATA_7
     - FT_D7
     - A4
     - 3.3V
     - 
   * - 50
     - DATA_8
     - FT_D8
     - B12
     - 3.3V
     - 
   * - 51
     - DATA_9
     - FT_D9
     - H8
     - 3.3V
     - 
   * - 52
     - DATA_10
     - FT_D10
     - E9
     - 3.3V
     - 
   * - 53
     - DATA_11
     - FT_D11
     - B2
     - 3.3V
     - 
   * - 54
     - DATA_12
     - FT_D12
     - D9
     - 3.3V
     - 
   * - 55
     - DATA_13
     - FT_D13
     - J9
     - 3.3V
     - 
   * - 56
     - DATA_14
     - FT_D14
     - A9
     - 3.3V
     - 
   * - 57
     - DATA_15
     - FT_D15
     - H9
     - 3.3V
     - 
   * - 60
     - DATA_16
     - FT_D16
     - A7
     - 3.3V
     - 
   * - 61
     - DATA_17
     - FT_D17
     - F8
     - 3.3V
     - 
   * - 62
     - DATA_18
     - FT_D18
     - A6
     - 3.3V
     - 
   * - 63
     - DATA_19
     - FT_D19
     - E10
     - 3.3V
     - 
   * - 64
     - DATA_20
     - FT_D20
     - A5
     - 3.3V
     - 
   * - 65
     - DATA_21
     - FT_D21
     - F9
     - 3.3V
     - 
   * - 66
     - DATA_22
     - FT_D22
     - E8
     - 3.3V
     - 
   * - 67
     - DATA_23
     - FT_D23
     - A8
     - 3.3V
     - 
   * - 69
     - DATA_24
     - FT_D24
     - K11
     - 3.3V
     - 
   * - 70
     - DATA_25
     - FT_D25
     - K12
     - 3.3V
     - 
   * - 71
     - DATA_26
     - FT_D26
     - J12
     - 3.3V
     - 
   * - 72
     - DATA_27
     - FT_D27
     - G12
     - 3.3V
     - 
   * - 73
     - DATA_28
     - FT_D28
     - L13
     - 3.3V
     - 
   * - 74
     - DATA_29
     - FT_D29
     - G13
     - 3.3V
     - 
   * - 75
     - DATA_30
     - FT_D30
     - J13
     - 3.3V
     - 
   * - 76
     - DATA_31
     - FT_D31
     - H13
     - 3.3V
     - 
   * - 58
     - CLK
     - FT_CLK
     - G9
     - 3.3V
     - 
   * - 4
     - BE_0
     - FT_BE0
     - B11
     - 3.3V
     - 
   * - 5
     - BE_1
     - FT_BE1
     - C12
     - 3.3V
     - 
   * - 6
     - BE_2
     - FT_BE2
     - A12
     - 3.3V
     - 
   * - 7
     - BE_3
     - FT_BE3
     - B13
     - 3.3V
     - 
   * - 8
     - TXE_N
     - FT_TXEn
     - C13
     - 3.3V
     - 
   * - 9
     - RXF_N
     - FT_RXFn
     - A12
     - 3.3V
     - 
   * - 10
     - SIWU_N
     - FT_SIWUn
     - 
     - 3.3V
     - 10k pull up
   * - 11
     - WR_N
     - FT_WRn
     - E12
     - 3.3V
     - 
   * - 12
     - RD_N
     - FT_RDn
     - D12
     - 3.3V
     - 
   * - 13
     - OE_N
     - FT_OEn
     - F12
     - 3.3V
     - 
   * - 15
     - RESET_N
     - FT_RESETn
     - L12
     - 3.3V
     - 
   * - 16
     - WAKEP_N
     - FT_WAKEUPn
     - H10
     - 3.3V
     - 