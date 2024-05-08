# Tasmota-termostate

1. Ready file for upload to ESP8266  (Tasmota v13.4 develop)  - [firmware.bin](https://github.com/1638NimtE/Tasmota_AHT20/blob/main/firmware.bin)
2. To load into the board, use the [Tasmotizer](https://github.com/tasmota/tasmotizer)
  
## Changed for compilate firmware.bin:

#### add functions
    BMP180
    AHT10
    AHT20  - correct driver
    TM1637
    TM1638
    RC Switch
    termostate +timeprop
    PING
    MP3 player

#### clear 
    IR red

## Console command

#### Termostate activate
    ThermostatModeSet 1
0 - off

1 - on

#### control strategy
    ControllerModeSet 0
0 - Hybrid (default)

1 - PI 

2 - Ramp-Up

## Rule boot termostate
    ON Power1#boot DO Backlog sensorinputset 1;controllermodeset 2;thermostatmodeset 1;temptargetset %mem1% ENDON
