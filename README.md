This project is constructed with the challenge where an RGB LED should be controlled by two or less input mechanisms.
This challenge can be overcome in many innovative ways, I chose this joystick technique.
Although it may feel like only one input device is being utilized, a joystick is made of two potentiometers indicating the X and Y axes with a re-centering mechanism.

Components used:
One Arduino Uno R3
One analog joystick
One RGB LED
One 16x2 LCD display
One potentiometer (used for setting the brightness of the LCD)

The project works as follows:
The first thing the user sees is the red-green-blue values displayed as a selection menu on the LCD.
This is achieved with the LiquidCrystal library and many if statements and prints for a refined user experience. 

After that, the user can use the X-axis (left-right) of the joystick to select among the main colors.
A 500 ms delay after a high X input so the users don't overshoot while trying to select their options.

The selected main color's brightness can go up and down based on the joystick's Y-axis input.
The lower limit for the LED is 0 and the upper limit is 255 for each color.

The joystick has a natural offset on its rest position created by physical imperfections. 
This means that when users expect (0, 0) on a rest position, it is around (9, 8) out of 1024 on our value in our case.
To eliminate this problem, a dead zone value is set to 30. 
The analog input also helps with smoother brightness selection where the user can pull the joystick halfway through for a slower change of brightness value.




