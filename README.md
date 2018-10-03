## Door-unlock-using-Arduino-Uno
A simple project to unlock the door using 4*4 keypad and Arduino. User will input the password,if it matches the door will be unlocked. Otherwise it will not unlock

## How Does the Keyless Door Lock System Work?

Whenever the keys are pressed, they are matched with the keys already stored. If the keys that are pressed match the initial password stored in the EEPROM which is ‘1234’, then the lock will open up. If the password does not match, then it will print “access denied” on the LCD. 
If the ‘#’ key will be pressed, it will ask you to enter the current password and if it matches, then it will ask you to enter the new password and the password will be changed.

![screenshot 196](https://user-images.githubusercontent.com/18008644/37867447-04df40cc-2fc3-11e8-892c-aaacab2c760b.png)


## Components:
1.	Arduino	Uno	
2.	4x4 keypad		
3.	16*2 LCD		
4.	DC Lock		
5.	Relay		
6.	9V battery		
7.  10k potentiometer		
8.	220-ohm resistor

## Circuit Diagram
First, connect the 4X4 keypad to the Arduino; connect the first six pins on the 4X4 keypad with the A0 and A5 pins on the Arduino. Then connect the last two pins on the 4X4 keypad module to digital pins 3 and 2 on the Arduino.

After that, connect the LCD to the Arduino. The connections for connecting the LCD with the Arduino are as follows:
```
1. Connect pin 1 on the LCD, which is the VSS pin, to GND on the Arduino
2. Connect pin 2, which is the VDD pin, to the 5V pin on the Arduino
3. Connect pin 3, which is the V0, to the middle of the 10k potentiometer and connect the other two pins on 
the potentiometer to 5V and GND on the Arduino. This pin is for setting the LCD's contrast.
4. Connect pin 4, which is the RS pin, to pin 7 on the Arduino
5. Connect pin 5, which is the R/W pin, to the GND pin on the Arduino
6. Connect pin 6, which is the Enable pin, to pin 6 on the Arduino
7. Connect pins 11, 12, 13, and 14 which are the data pins, to the pins 5, 4, 3, and 2 on the Arduino
8. Connect pin 15, which is the LCD's backlight pin, to 5V on the Arduino through the 220-ohm resistor
9. Connect pin 16 on the Arduino, which is the negative pin of the backlight, to GND on the Arduino
```
Last, we will connect the DC lock with the Arduino. The Lock operates on a voltage from 7 to 12V, so we cannot directly connect it to the Arduino. To connect it to the Arduino, we will require a relay and a battery. 

Connect the signal pin of the relay to pin 10 on the Arduino and the lock's VCC and GND to 5V and GND on the Arduino. Then on the other end of the relay, connect the negative of the battery to the common on the relay and the NO (Normally open) on the relay to one side of the lock. Then connect the other side of the lock to the positive terminal on the battery.



![screenshot 195](https://user-images.githubusercontent.com/18008644/37867445-ff09980a-2fc2-11e8-8059-49d974500f1f.png)

## Arduino Keypad Lock Code
The initial password is 1234. for code, [see here](https://github.com/NeloyNSU/Door-unlock-using-Arduino-Uno/blob/master/door.ino)


