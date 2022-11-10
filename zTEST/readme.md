## Test Harness

### VUT MODEL - Test Harness:

* Airsupply-sub-systems -> sub-systems -> AS_Assembly.slx
* VUT model inputs are in percentage (0.0 - 1.0)

[TEST HARNESS EXAMPLE VID](https://www.youtube.com/watch?v=-Cw67kBXxxk)

### LINKS:

[Create a Test Harness](mathworks.com/help/sltest/gs/create-a-test-harness.html)
Location: C:\Program Files\MATLAB\R2022a\examples\simulinktest\main\sltestCarRootInport 
# zTEST:

**NOTE** - Physical test models running on control board hardware (TESTED)

### 0_TSE_New

* Full system with new block structure

### 1_led

* Simple LED blinking (programmer & MCU test model)

### 1_com

* Simple LED blinking
* SPI: Read  - CH_0, CS(PA_4)
* I2C: Write - CH_0, Slave_Add: 0x55

### 2_Mtr

* Simple blower motor control model (StateFlow)
* Square wave input (0-200 @ approx. 2sec)
* Blink LED every 3 sec (removed LED output)

### 3_mtr

* Blower motor control model (converted to Nucleo)
* StateFlow based PID with Pressure Sensor input (SPI)
* Pressure Sensor monitoring setup for Arduino I2C in/out

### 4_full_sys

* Full system with all coms (in & out) commented out
* Except Pressure sensor (SPI_0) & Motor_Controller (I2C_2)

### 5_full_sys (delete)

* Same as Above with PID testing - Not Working, so delete

### 6_full_sys

* Pressure Sensor + PID + Motor_Contrller - (TESTED!)

### 7_PID

* **Control_Board** Pinouts
* Individual PID + motor controller test (without entire system attached)
* PID negative feedback value = "HMI input" = constant

### 8_full_sys

* "6_full_sys" + Exhalation Flow Controller (PWM) integrated - (TESTED!
)
### 9_TH_PID

* Test Harness for the "8_PID" model
* Allows for varying test input signals to generate output scope
* open_loop & closed_loop issues with PID outputs (solved in main model?)

### 10_TH_TSE

* Test Harness for Main (new) TSE control board model "0_TSE_New"
* Multiple varying input test signals: **Pressure1+2, Flow1+2, FiO2**

### SPI_Print

* Arduino UNO code for directly printing data received from the Control Board

### sys_test

* New system architecture for TSE model - MUST SEE!!