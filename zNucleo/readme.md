## Test Harness

### VUT MODEL - Test Harness:

* Airsupply-sub-systems -> sub-systems -> AS_Assembly.slx
* VUT model inputs are in percentage (0.0 - 1.0)

[TEST HARNESS EXAMPLE VID](https://www.youtube.com/watch?v=-Cw67kBXxxk)

### LINKS:

# zTEST:

**NOTE** - Physical test models running on control board hardware (TESTED)

### 1_PID

* **STM32_Nucleo** Pinouts
* Individual Pressure Sensor + PID + Motor Controller test (without entire system attached)
* PID negative feedback value = Pressure Sensor (SPI_0 [P8])
* Open & Closed Loop PID models included -> Closed-Loop = HIL

### 2_Mtr

* Simple blower motor control model (StateFlow)
* Square wave input (0-200 @ approx. 2sec)
* Blink LED every 3 sec (removed LED output)

### 3_mtr **THIS ONE**

* Blower motor control model (StateFlow) (on-3sec / off-3sec)
* Pressure Sensor input (SPI) (200 motor = 3 sensor?)

### 4_mtr

* All functions from '3_mtr' except motor test
* Motor output value: start: 20
* Every 2 seconds increment by 20 (limited at 250)
* Shutdown at 30 sec & sim for 35 sec