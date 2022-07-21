# B-G431B-ESC1-FOC Firmware

## CAN Frames

| CAN ID | Frame          |
| ------ | -------------- |
| 0x08   | Mode control   |
| 0x40   | Position info  |
| 0x41   | Velocity info  |



### 0x08 Mode Control Frame

| Bytes | Field                         | R/W |
| ----- | ----------------------------- | --- |
| 7..1  | UNUSED                        | R   |
| 0     | mode                          | RW  |

#### mode

- 0x00: `FOC_MODE_IDLE`

- 0x01: `FOC_MODE_CALIBRATION`

- 0x02: `FOC_MODE_TORQUE`

- 0x03: `FOC_MODE_VELOCITY`

- 0x04: `FOC_MODE_POSITION`

### 0x40 Position Info Frame

| Bytes | Field                         | R/W |
| ----- | ----------------------------- | --- |
| 7..4  | position_measured             | R   |
| 3..0  | position_setpoint             | RW  |

### 0x41 Velocity Info Frame

| Bytes | Field                         | R/W |
| ----- | ----------------------------- | --- |
| 7..4  | velocity_measured             | R   |
| 3..0  | velocity_setpoint             | RW  |
