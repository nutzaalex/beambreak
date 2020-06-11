# Boosted Board Reverse Engineering
BeamBREak is an attempt at REing the various components of Boosted Board's electronics to keep boards running, due to their uncertain future.

Feel free to raise an issue or send me a message on Twitter [@robertscullin](https://twitter.com/robertscullin) if you have questions or more info.

# Getting Started
I'm in the process of splitting documentation to https://beambreak.org , and using this GitHub repo for code and issues. Links to existing documentation here won't be broken, but will have a notice added at the top referencing the moved page at some point in the future.

## Firmware
[Known Firmware Versions](https://beambreak.org/articles/known_firmware_versions/) is a list of V2+ firmware versions seen. Please note: as of April 2020, there is no known way to update you board or battery firmware, as Boosted shut down the authorization and firmware update server.

## CAN Bus
The Boosted Board has two CAN Buses, running at 250kbaud. One is used for BMS<->ESC communication, and the other is used for the Accessory Port.

The [CAN Bus](CAN%20Bus/) folder has the bulk of the research and scripts, including a [SR Battery DBC file](CAN%20Bus/SR_Battery.dbc), a [SR Battery Emulator](CAN%20Bus/sr_battery_emulator.py) Python script, documentation of the [SR Battery CAN IDs](CAN%20Bus/SR%20Battery%20CAN%20Bus.md) in human-readable format, and info on the [physical connectors](CAN%20Bus/README.md).

Additionally, the Accessory port is [partially documented](Accessory/README.md), including an [Arduino sketch to emulate the Beams](Accessory/beams_emulator.ino).

## Batteries
The [Hardware](Hardware/) folder has information about the [XR battery pack](Hardware/XR%20Battery.md), including the cells and some of the major ICs used by the pack. I also wrote a [XR RLOD FAQ](https://beambreak.org/articles/xr_rlod_faq/) that covers how the balancing works, how to attempt to prevent RLODs, and more.