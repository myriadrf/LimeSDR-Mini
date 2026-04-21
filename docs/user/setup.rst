Hardware Setup
##############

Host Interface
**************

LimeSDR Mini should be plugged into a USB type-A socket slot on the host device.

The host must provide a USB 2.0 or higher interface, and supply power (5V, 900 mA) via the USB type-A connector.

.. note:: 
 A USB 3.0 interface is required to achieve the maximum supported data transfer rate.

Cooling
*******

Depending on the application, host system and ambient temperature, additional cooling may be required to ensure reliable operation of the LimeSDR Mini board. This may be in the form of airflow through the host system, or a dedicated heatsink fitted to the board.

The LimeFEA mPCIe adapter boards provide an integrated heatsink in the form of a large copper ground plane plus thermal pad.

.. note::
   In the event of errors, instability or reduced performance, check the board temperature to ensure that it is within the specified operating range.

RF Connections
**************

.. figure:: /images/LimeSDR-Mini_v1.2_RFCON.png
  :width: 600
  
  Figure 3: LimeSDR Mini v1.x board top with RF connector positions

.. table:: Table 1. RF Connectors

  +------------------+--------------------+-------------+---------------------+-------------------------------+
  | **Connector ID** | **Connector type** | **RF band** | **Frequency range** | **Note**                      |
  +==================+====================+=============+=====================+===============================+
  | J1               | SMA                | TX low      | 10 MHz - 2 GHz      | transmit low frequency range  |
  |                  |                    +-------------+---------------------+-------------------------------+
  |                  |                    | TX high     | 2 GHz - 3.5 GHz     | transmit high frequency range |
  +------------------+--------------------+-------------+---------------------+-------------------------------+
  | J2               | SMA                | RX wide     | 10 MHz - 2 MHz      | receive wide frequency range  |
  |                  |                    +-------------+---------------------+-------------------------------+
  |                  |                    | RX high     | 2 GHz - 3.5 GHz     | receive high frequency range  |
  +------------------+--------------------+-------------+---------------------+-------------------------------+

.. warning::
   Care should be taken when connecting external RF signals to the RX inputs, to ensure that the maximum safe input power of +10 dBm is not exceeded, as this may cause permanent damage to the device.

