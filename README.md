# LimeSDR-Mini

![LimeSDR-Mini board](/images/LimeSDR-Mini_722w.jpg)

The [LimeSDR-Mini](https://myriadrf.org/projects/limesdr/) board provides a hardware platform for developing and prototyping high-performance and logic-intensive digital and RF designs using Altera’s MAX10 FPGA and Lime Microsystems transceiver.

* **FPGA Features**
  * 169-pin FBGA package
  * 16 K Les
  * 549 KB M9K memory
  * 2,368 KB user flash memory
  * 4 x fractional phase locked loops (PLLs)
  * 45 x 18x18-bit multipliers
  * 130 x general purpose input/output (GPIO)
  * Single supply voltage
  * Flash feature
  * FPGA configuration via JTAG
* **EEPROM memory:** 2 x 128 KB for RF transciever MCU firmware and data
* **Flash memory:** 1 x 4 MB flash memory for data
* **General user inputs/outputs:**
  * 2 x dual color (red + green) LED
  * 8 x FPGA GPIO pinheader (3.3 V)
* **Connectivity:**
  * USB 3.0 Type-A (FTDI FT601 controller)
  * 2 x coaxial RF (SMA) connectors (each can be switched between high and low frequency bands)
  * U.FL connector for external clock source
  * FPGA GPIO headers
  * FPGA JTAG connector
* **Clock system:**
  * 30.72 MHz onboard VCTCXO
  * Possibility to tune VCTCXO with onboard DAC
  * External clock input via U.FL connector
* **Board dimensions:** 69 mm x 31.4 mm

## Contents

The directory structure is as follows:

      hardware/<version>/
          Libraries/             - Component Libraries
          OutputJobs/            - Output jobs
          PCB/                   - PCB design
          Project Outputs/       - BOM, rule check reports, Gerbers, pick & place files, PDFs
          Schematics/            - Schematic diagrams

## Licensing

The hardware designs are licensed under a Creative Commons Attribution 3.0 Unported licence.
