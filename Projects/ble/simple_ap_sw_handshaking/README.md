SimpleAP with UART Software Handshaking
====================

This project is a duplicate of the SimpleAP project in the SDK, and is aimed at adding software handshaking to the NPI protocol on the TI CC2640 BLE SoC. This allows the device to wake up on the UART RX line and enter power saving mode without needing hardware flow control.

This project is built to run on the SmartRF06 Evaluation Board with a CC2650 7x7 Evaluation Module or CC2650 SensorTag. To use a different board, exchange the Board.c file and change the search path for the board files.

The SAP library must be built before building the SimpleAP project. The modified SAP library with software handshaking added can be found in the sap_lib_sw_handshaking folder. See links below for more information about the SAP library and how it functions.

All the files in the project are referenced from their location within the BLE SDK, with the exception of the modified NPI files in this repository: `/Components/npi/**/*swhs.*`

The functionality can be added to an existing project by swapping out the applicable files in your IDE with their `_swhs.*` counterpart, and adding the include search paths.

More information on Unified NPI with UART Software handshaking:
[Unified NPI with UART Software Handshaking](../../../Components/npi/unified)

More information about the SimpleAP and SimpleNP projects:
[http://processors.wiki.ti.com/index.php/SimpleAP%2BSNP](http://processors.wiki.ti.com/index.php/SimpleAP%2BSNP)
