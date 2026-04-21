Clock Distribution
##################

LimeSDR Mini board clock distribution block diagram is presented in Figure 6. LimeSDR-Mini board has onboard 40.00 MHz VCTCXO that is reference clock for LMS and FPGA PLLs.

.. figure:: /images/LimeSDR-Mini_v1.2_clock.png
  :width: 600

  Figure 6. LimeSDR Mini v1.2 board clock distribution block diagram

VCTCXO frequency can be tuned by using DAC (IC9). Buffered VCTCXO clock is connected to RF transceiver, FPGA. Buffered VCTCXO clock is also connected to connector J9 (REF_CLK_OUT) and can be fed to external hardware for synchronisation. VCTCXO can be disconnected from clock buffer input (remove R59 and solder R62) and external reference clock can be supplied from connector J8 (REF_CLK_IN).

.. table:: Table 3. LimeSDR Mini clock pins

  +----------------------+------------------------+------------------+--------------+---------------------------------+
  |      **Source**      | **Schematic net name** | **I/O standard** | **FPGA pin** |         **Description**         |
  +======================+========================+==================+==============+=================================+
  | External             | REF_CLK_IN             |                  |              | External reference clock input  |
  +----------------------+------------------------+------------------+--------------+---------------------------------+
  | Board                | Board                  | 2.5V (3.3V)      |              | Buffered reference clock output |
  +----------------------+------------------------+------------------+--------------+---------------------------------+
  | Clock buffer (IC7)   | LMK_CLK                | 2.5V (3.3V)      | H6           | Buffered reference clock output |
  +----------------------+------------------------+------------------+--------------+---------------------------------+
  | RF transceiver (IC1) | RxPLL_CLK              | 2.5V (3.3V)      |              | Buffered reference clock output |
  |                      +------------------------+------------------+--------------+---------------------------------+
  |                      | TxPLL_CLK              | 2.5V (3.3V)      |              | Buffered reference clock output |
  |                      +------------------------+------------------+--------------+---------------------------------+
  |                      | LMS_MCLK1              | 2.5V (3.3V)      | G5           |                                 |
  |                      +------------------------+------------------+--------------+---------------------------------+
  |                      | LMS_FCLK1              | 2.5V (3.3V)      | L3           |                                 |
  |                      +------------------------+------------------+--------------+---------------------------------+
  |                      | LMS_MCLK2              | 2.5V (3.3V)      | H4           |                                 |
  |                      +------------------------+------------------+--------------+---------------------------------+
  |                      | LMS_FCLK2              | 2.5V (3.3V)      | M3           |                                 |
  +----------------------+------------------------+------------------+--------------+---------------------------------+
  | USB3.0 controller    | FT_CLK                 | 3.3V             | G9           | 100 MHz                         |
  +----------------------+------------------------+------------------+--------------+---------------------------------+

External clock notes. External clock capabilities on LimeSDR-Mini board are defined by LMK00105 clock buffer specification. User must ensure voltage levels are in the range of LMK00105 capabilities. Ideally, a phase detector circuitry should be used to synchronize on board TCXO to the external clock but there simply is no space on LimeSDR-Mini for this functionality. Hence decision was made just to provide an input to LMK clock buffer for external clock connection. This means that user should pay attention on how external signal is connected, ensure proper voltage levels etc. If you supply external clock signal from signal generator, signal level should be around 10dBm. Note please, that LMK clock buffer expects positive voltage amplitude, while your generator may supply +/- voltage.

The proper way to supply the external reference clock: supply external clock firstfirst and then turn the board on. This is the only way to have proper operation of the board with external clock. If frequency is changed on the fly, CPU inside of FPGA gets messed up hence no control over the board.

