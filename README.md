# Introduction_to_robotics
A repository for my third year course, "Introduction to Robotics"

## Homework 1) EV Charger

_1.1 Description_

In this project, you need to simulate a charging station for an electric vehicle using multiple LEDs and buttons. In this task, you must consider the button states and use debouncing, while also coordinating all components as in a real-life scenario.

_1.2 Components_

4x LEDs (to simulate the charging percentage)

1x RGB LED (to indicate free or occupied status)

2x Buttons (for starting and stopping the charging process)

9x Resistors (7x 220 ohm, 2x 1K)

Breadboard

Connection wires

_1.3 Technical Details_

 The RGB LED represents the availability of the station. If the station is free, the LED will be green; if the station is occupied, it will turn red.
 
 The simple LEDs represent the battery charge level, which we will simulate through a progressive loader (L1 = 25%, L2 = 50%, L3 = 75%, L4 = 100%). The loader charges by successively turning on the LEDs at a fixed interval of 3 seconds. The LED corresponding to the current charge percentage will blink, while the previous LEDs will stay continuously on, and the others will remain off.
 
 A short press of the start button will begin the charging process. Pressing this button during charging will have no effect.
 
 A long press of the stop button will forcibly stop the charging and reset the station to the free state. Pressing this button while the station is free will do nothing.
 
_1.4 Flow_

The station's state is ‘free’. The loader is off, and the availability LED is green.

The start button is pressed.

The availability LED turns red, and the charging process begins by lighting up the first LED (L1).

The first LED blinks for 3 seconds, while the others remain off.

After charging the first 25%, the first LED stays on and the process moves to the next LED, which starts blinking.

Upon completion of the charging process, all LEDs will blink simultaneously 3 times, then turn off to signal the end of the process.

The availability LED turns green again.

If at any point from the start of the charging process to its completion the stop button is pressed and held (for at least 1 second), the charging process will be interrupted by the final animation (all LEDs blink 3 times), and the availability LED will turn green.

_Wokwi configuration_
![64C3A504-2BFD-45B2-92D1-FB4B7033BAA6](https://github.com/user-attachments/assets/81338534-1bf1-43a5-a29e-e8c89dfdfc46)

_Physical configuration_
![5921B127-2379-4B8D-BD58-FA8FBD70D639](https://github.com/user-attachments/assets/926b46dd-b35a-4500-8b9e-abf79f108c15)

_Demonstration video_
https://drive.google.com/file/d/1-nfJHyRTKYhNsfqe5cAyOKlRrkdF_UZ_/view?usp=drivesdk
