# Car Automatic Lights
This project simulates car automatic lights using Arduino Uno R3 and other components in Tinkercad (see documentation.pdf for the brief note). A photoresistor measures the light around the car. When it is darker than the threshold, the front lights (two orange LEDs) are turned on through a relay. The threshold is set with a potentiometer and a set button, and it is saved in EEPROM, so it is still there after power off.

## Features
- Photoresistor measures the light every 100 ms (Timer1 interrupt)
- Relay (controlled by TIP120 transistor) turns the front lights on in the dark and off in the light
- Potentiometer + set button change the threshold
- Threshold is saved in EEPROM and loaded when Arduino starts (with version check and value validation)
- Serial monitor shows light value, potentiometer value, threshold and lights state (ON/OFF)
- No delay() in the code, only timer interrupt, flags and debounce with millis()

## How to use
1. Open this project in Tinkercad (or upload the code to Arduino Uno);
2. Start the simulation and open the Serial Monitor;
3. Click the photoresistor and change the light level - the lights turn on when the value is lower than the threshold;
4. Turn the potentiometer to the wanted value and press the set button to save it as the new threshold;
5. Press restart button built-in Arduino Uno R3 board - the last threshold is still the same.

## Files
- car_automatic_lights.ino - full project (Arduino) code
- documentation.pdf - brief note
