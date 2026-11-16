RF Network
##########

The RF network contains matching networks, RF switches, a loopback attenuator and two SMA connectors (J1 - TX and J2 - RX).

Frequency Range
===============

Each LMS7002M RF transceiver TX and RX port is connected to a dedicated RF path, and the appropriate path should be selected according to the operating frequency. On the receive side, the wideband path (RX1_W) is recommended for frequencies below 2 GHz and the high-band path (RX1_H) for frequencies of 2 GHz and above. On the transmit side, the TX1_2 path is recommended for frequencies below 2 GHz and the TX1_1 path for frequencies of 2 GHz and above. The recommended frequency ranges for all ports are summarised in Table 3.

.. note::
   The recommended frequency ranges are approximate values that cover most use cases, not hard limits of the RF paths. The optimum path may vary depending on other factors, such as the antenna and RF front-end parameters.

.. list-table:: Table 3. LMS7002M RF transceiver ports and recommended frequency ranges
   :header-rows: 1

   * - RF transceiver port
     - Recommended frequency range
   * - TX1_1
     - 2 GHz and above
   * - TX1_2
     - Below 2 GHz
   * - RX1_H
     - 2 GHz and above
   * - RX1_W
     - Below 2 GHz

Control
=======

The RF switches select which TX and RX ports are connected to the SMA connectors. The unused TX port can be connected to the unused RX port through a loopback path with a fixed -40 dB attenuator. RFSW_TX_V1 is in FPGA Bank 3 (VDIO_LMS_FPGA, 2.5 V by default) and the other control signals are in Banks 5 and 8 (VCC3P3, 3.3 V). RF network control signals are described in Table 4.

.. table:: Table 4. RF network control signals

  +------------------------+---------------------------+------------------+--------------+------------------------------------------------+
  | **Component**          | **Schematic signal name** | **I/O standard** | **FPGA pin** | **Description**                                |
  +========================+===========================+==================+==============+================================================+
  | RFSW_TX                | RFSW_TX_V1                | 2.5 V            | L11          | V1 high, V2 low: TX1_1 to TX, TX1_2 to ATT.    |
  |                        |                           |                  |              |                                                |
  | (SKY13411-374LF – IC3) |                           |                  |              | V1 low, V2 high: TX1_1 to ATT, TX1_2 to TX.    |
  |                        +---------------------------+------------------+--------------+                                                |
  |                        | RFSW_TX_V2                | 3.3 V            | C4           |                                                |
  +------------------------+---------------------------+------------------+--------------+------------------------------------------------+
  | RFSW_RX                | RFSW_RX_V1                | 3.3 V            | A10          | V1 high, V2 low: RX1_H to RX, RX1_W to ATT.    |
  |                        |                           |                  |              |                                                |
  | (SKY13411-374LF – IC4) |                           |                  |              | V1 low, V2 high: RX1_H to ATT, RX1_W to RX.    |
  |                        +---------------------------+------------------+--------------+                                                |
  |                        | RFSW_RX_V2                | 3.3 V            | C9           |                                                |
  +------------------------+---------------------------+------------------+--------------+------------------------------------------------+
  | Loopback attenuator    | TX_LB_AT                  | 3.3 V            | K10          | Not used, -25 dB path not fitted (VT1, R16).   |
  |                        +---------------------------+------------------+--------------+------------------------------------------------+
  |                        | TX_LB_SH                  | 3.3 V            | J10          | High: attenuator shunted to GND (VT3).         |
  +------------------------+---------------------------+------------------+--------------+------------------------------------------------+
