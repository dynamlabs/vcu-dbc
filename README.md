# Dynam Labs DBC Files

DBC files for interfacing with Dynam Labs VCU+ (Vehicle Control Unit).

## Contents

The repository includes:

- `dynam-VCU+.dbc`: Defines CAN messages for vehicle state, torque control, gear selection, temperature monitoring, BMS data, GPS information, and error reporting.

## CAN Message Overview

| ID  | Name | Sender | Length (bytes) | Cycle Time (ms) | Description |
|-----|------|--------|----------------|-----------------|-------------|
| 0x64 | VCU_torque | MCU | 3 | 10 | Torque request |
| 0x65 | VCU_shift | MCU | 1 | - | Gear and drive-mode selection |
| 0x66 | VCU_state | VCU | 2 | 50 | Vehicle state information |
| 0xC8 | DI_state | VCU | 6 | 100 | Primary drive inverter state |
| 0xC9 | DIS_state | VCU | 4 | 100 | Secondary drive inverter state |
| 0xCA | DI_temperature | VCU | 4 | 100 | Primary drive inverter temperatures |
| 0xCB | DIS_temperatures | VCU | 4 | 100 | Secondary motor temperatures |
| 0x12C | BMS_info | VCU | 8 | 100 | Battery management system information |
| 0x190 | VCU_gps | VCU | 8 | 100 | GPS location and velocity data |
| 0x1F4 | VCU_error | VCU | 4 | - | Error reporting |

## Resources

For more information about Dynam Labs VCU, visit [dynamlabs.com/vcu](https://dynamlabs.com/vcu).
