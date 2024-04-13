# Landshark's Controller Library
This code originally comes from [TensorKart's utils.py](https://github.com/kevinhughes27/TensorKart/blob/master/utils.py), which is under the MIT License. 

The code has been adapted to fit our needs, but remains under the MIT License.

## General Changes:
- Checking if the controller is plugged in at the start/ever gets unplugged or disconnected somehow
- Stopping the program by checking if the monitor thread is no longer alive, with a message to the user!

## Dict Values:
- `"a"`: A Button
- `"b"`: B Button
- `"x"`: X Button
- `"y"`: Y Button
- `"ls"`: Left Joystick Pushed
- `"rs"`: Right Joystick Pushed
- `"back"`: "View" (Double Square) Button
- `"start"`: "Menu" (Hamburger/3 Lines) Button
- `"share"`: Share Button (Below Xbox Button, Series X/S Only)
- `"xbox"`: Xbox Logo Button
- `"lb"`: Left Bumper
- `"rb"`: Right Bumper
- `"dx"`: D-Pad X
- `"dy"`: D-Pad Y
- `"lt"`: Left Trigger (0 to 1)
- `"rt"`: Right Trigger (0 to 1)
- `"lsx"`: Left Joystick X (-1 to 1)
- `"lsy"`: Left Joystick Y (-1 to 1)
- `"rsx"`: Right Joystick X (-1 to 1)
- `"rsy"`: Right joystick Y (-1 to 1)


## Example Usage:

```python
from controller import XboxController

controller = XboxController()

readDict = controller.read()
print(readDict["lsy"]) # Print the value of the left joystick y
# EX: 0.672638 (This will be a range of -1 to 1, inclusive)

print(int(round(readDict["lsy"], 2) * 100)) # Print the value of the left joystick y but rounded to 2 spots and multiplied by 100
# EX: 67 (This will be a range of -100 to 100, inclusive, and never have decimals)
```
