# Working Principle

The system uses a 4×4 matrix keypad to accept user input.
Each key press is read by the Arduino and stored in memory.

The entered digits are masked on the LCD for basic security.
Once four digits are entered, pressing the D key submits the password.

If the password matches the predefined value (1234),
the servo motor rotates to simulate door opening.
Incorrect passwords result in an error message.

The system allows resetting input using the # key
and closing the door using the C key.
