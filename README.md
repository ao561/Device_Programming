# Device Programming

Activity 1: Programming the microcontroller to record a sequence of colours entered by the user, and then play it back. Here is the approach:  
1. The board starts by cycling the three LEDs, turning them on one at time, and switching every second: LED1 (green) for 1s –> LED2 (blue) for 1 sec –> LED3 (red) for 1s –> LED1 for 1 sec, etc.
2. While the colours are cycling, the user selects a colour by pressing the button. The colour that is ON at this time is recorded.
3. The process continues until N colours have been entered (the size of the sequence N is set in the code).
4. Once recording is completed, the recorded sequence is played back on the LEDs.

Activity 2: Using the I2C bus and protocol, a temperature sensor, and the microcontroller:  
1. Record a temperature value every second in an array that will contain the last minute of data (older data is replaced by new data once the array is full).
2. If the temperature goes above a threshold value of 28 degree Celsius, the sensor will trigger an interrupt which will get the LEDs on the microcontroller to flash an alarm signal, stop the recording, and transmit the last minute of data to your computer by USB serial communication, so that the log can be analysed.
