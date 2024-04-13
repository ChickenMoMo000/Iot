This Arduino code is designed to measure both current and voltage using analog sensors, and it displays the voltage on an OLED display. Here's a breakdown of what the code does:
Libraries
The code includes several libraries:
Wire.h: Allows communication with I2C devices, in this case, the OLED display.
Adafruit_GFX.h: Graphics library for the OLED display.
Adafruit_SSD1306.h: Library for controlling the SSD1306 OLED display.
SoftwareSerial.h: Library for serial communication.
Constants and Variables
It defines constants for the OLED display dimensions and reset pin.
Defines pins for current and voltage sensors.
Defines variables for reference voltage and resistor values.
Sets a minimum current threshold.
Setup Function
Initializes serial communication at a baud rate of 9600.
Sets the pinMode for current and voltage sensor pins.
Initializes the OLED display.
Clears the display and sets text color to white.
Loop Function
Reads analog values from the current and voltage sensors.
Calculates current and voltage values using the analog readings and the reference voltage.
Applies the voltage divider formula to calculate the actual voltage.
If the voltage exceeds 6 volts, it sends "HighVoltage" signal over serial communication.
Displays the voltage on the OLED display.
Prints voltage values over serial.
Includes a delay of 1000 milliseconds.
Additional Notes
The voltage divider formula is used to measure higher voltages by scaling down the voltage to a measurable range.
Adjustments may be needed for the threshold and delay based on specific project requirements.
The OLED display is updated with the voltage reading every loop iteration.
Overall, this code allows you to monitor voltage levels and trigger actions based on certain conditions (e.g., high voltage).
