# VL53L0X Register Map

A crowd sourced extended API documentation for "VL53L0X".
Did you already have experience with the sensor in one of your projects and had to find the register mapping yourself? 
Then feel free to contribute this knowledge here in the form of a commit or issue.


## Register map of VL53L0X

| Register Name | Address | Description |
|----|----|----|
| SYSRANGE_START | 0x00 | `0x00`: `0`: single shot mode<br>`0x01`: `1`: <br>&nbsp;&nbsp;&nbsp;&nbsp;*@continuous mode*: toggle state <br>&nbsp;&nbsp;&nbsp;&nbsp;*@singleshot mode*: arm next shot<br>`0x02`: `1`: back-to-back operation mode<br>`0x04`: timed operation mode<br>`0x08`: histogram operation mode |
| SYSTEM_THRESH_HIGH |  0x0C |  |
| SYSTEM_THRESH_LOW |  0x0E |  |
| SYSTEM_SEQUENCE_CONFIG |  0x01 |  |
| SYSTEM_RANGE_CONFIG |  0x09 |  |
| SYSTEM_INTERMEASUREMENT_PERIOD |  0x04 |  |
| **GPIO config** |
| SYSTEM_INTERRUPT_GPIO_CONFIG |  0x0A | `0x00`: Disabled<br>`0x01`: Low level<br>`0x02`: High level<br>`0x03`: Out of window<br>`0x04`: New sample ready |
| GPIO_HV_MUX_ACTIVE_HIGH |          0x84 |  |
| SYSTEM_INTERRUPT_CLEAR |           0x0B |  |
| I2C_SLAVE_DEVICE_ADDRESS |  0x8a |  |
| I2C_MODE |  0x88 | `0`: i2c standard mode |
| **Result registers** |
| RESULT_INTERRUPT_STATUS |          0x13 |  |
| RESULT_RANGE_STATUS |              0x14 |  |
| RESULT_CORE_AMBIENT_WINDOW_EVENTS_RTN |   0xBC |  |
| RESULT_CORE_RANGING_TOTAL_EVENTS_RTN |    0xC0 |  |
| RESULT_CORE_AMBIENT_WINDOW_EVENTS_REF |   0xD0 |  |
| RESULT_CORE_RANGING_TOTAL_EVENTS_REF |    0xD4 |  |
| RESULT_PEAK_SIGNAL_RATE_REF |             0xB6 |  |
| **Algo register** |
| ALGO_PART_TO_PART_RANGE_OFFSET_MM |       0x28 |  |
| **Check Limit registers** |
| MSRC_CONFIG_CONTROL |                     0x60 |  |
| PRE_RANGE_CONFIG_MIN_SNR |                      0x27 |  |
| PRE_RANGE_CONFIG_VALID_PHASE_LOW |              0x56 |  |
| PRE_RANGE_CONFIG_VALID_PHASE_HIGH |             0x57 |  |
| PRE_RANGE_MIN_COUNT_RATE_RTN_LIMIT |            0x64 |  |
| FINAL_RANGE_CONFIG_MIN_SNR |                    0x67 |  |
| FINAL_RANGE_CONFIG_VALID_PHASE_LOW |            0x47 |  |
| FINAL_RANGE_CONFIG_VALID_PHASE_HIGH |           0x48 |  |
| FINAL_RANGE_CONFIG_MIN_COUNT_RATE_RTN_LIMIT |   0x44 |  |
| **PRE RANGE registers** |
| PRE_RANGE_CONFIG_SIGMA_THRESH_HI |              0x61 |  |
| PRE_RANGE_CONFIG_SIGMA_THRESH_LO |              0x62 |  |
| PRE_RANGE_CONFIG_VCSEL_PERIOD |                 0x50 |  |
| PRE_RANGE_CONFIG_TIMEOUT_MACROP_HI |            0x51 |  |
| PRE_RANGE_CONFIG_TIMEOUT_MACROP_LO |            0x52 |  |
| **Internal tuning registers** |
| INTERNAL_TUNING_?1 |  0x91 | |
| INTERNAL_TUNING_?2 |  0xFF | |
| **Unknown registers** |
| UNKNOWN_?1 |  0x85 | |
| UNKNONW_?2 |  0xcd | |
| UNKNONW_?3 |  0xcc | |
| UNKNONW_?4 |  0xbe | |
| **Other registers** |
| SYSTEM_HISTOGRAM_BIN |                          0x81 |  |
| HISTOGRAM_CONFIG_INITIAL_PHASE_SELECT |         0x33 |  |
| HISTOGRAM_CONFIG_READOUT_CTRL |                 0x55 |  |
| FINAL_RANGE_CONFIG_VCSEL_PERIOD |               0x70 |  |
| FINAL_RANGE_CONFIG_TIMEOUT_MACROP_HI |          0x71 |  |
| FINAL_RANGE_CONFIG_TIMEOUT_MACROP_LO |          0x72 |  |
| CROSSTALK_COMPENSATION_PEAK_RATE_MCPS |         0x20 |  |
| MSRC_CONFIG_TIMEOUT_MACROP |                    0x46 |  |
| SOFT_RESET_GO2_SOFT_RESET_N |                  0xbf |  |
| IDENTIFICATION_MODEL_ID |                       0xc0 |  |
| IDENTIFICATION_REVISION_ID |                    0xc2 |  |
| OSC_CALIBRATE_VAL |                             0xf8 |  |
| GLOBAL_CONFIG_VCSEL_WIDTH |          0x032 |  |
| GLOBAL_CONFIG_SPAD_ENABLES_REF_0 |   0x0B0 |  |
| GLOBAL_CONFIG_SPAD_ENABLES_REF_1 |   0x0B1 |  |
| GLOBAL_CONFIG_SPAD_ENABLES_REF_2 |   0x0B2 |  |
| GLOBAL_CONFIG_SPAD_ENABLES_REF_3 |   0x0B3 |  |
| GLOBAL_CONFIG_SPAD_ENABLES_REF_4 |   0x0B4 |  |
| GLOBAL_CONFIG_SPAD_ENABLES_REF_5 |   0x0B5 |  |
| GLOBAL_CONFIG_REF_EN_START_SELECT |   0xB6 |  |
| DYNAMIC_SPAD_NUM_REQUESTED_REF_SPAD | 0x4E |  |
| DYNAMIC_SPAD_REF_EN_START_OFFSET |    0x4F |  |
| POWER_MANAGEMENT_GO1_POWER_FORCE |    0x80 |  |
| VHV_CONFIG_PAD_SCL_SDA__EXTSUP_HV |     0x89 |  |
| ALGO_PHASECAL_LIM |                         0x30 |  |
| ALGO_PHASECAL_CONFIG_TIMEOUT |              0x30 |  |


## Error list of VL53L0X

| Error Name | Error Number | Description |
|----|----|----|
| NONE                        | 0 | No error occurred |
| VCSELCONTINUITYTESTFAILURE  | 1 | |
| VCSELWATCHDOGTESTFAILURE    | 2 | |
| NOVHVVALUEFOUND             | 3 | |
| MSRCNOTARGET                | 4 | |
| SNRCHECK                    | 5 | |
| RANGEPHASECHECK             | 6 | |
| SIGMATHRESHOLDCHECK         | 7 | |
| TCC                         | 8 | |
| PHASECONSISTENCY            | 9 | |
| MINCLIP                     | 10 | |
| RANGECOMPLETE               | 11 | |
| ALGOUNDERFLOW               | 12 | |
| ALGOOVERFLOW                | 13 | |
| RANGEIGNORETHRESHOLD        | 14 | |

###### The here written knowledge is not a copy of any file. It is free written. Possible matches of labels from other documents are accidental. In the event of infringements of the rights of third parties, I would ask you to inform me about this.
