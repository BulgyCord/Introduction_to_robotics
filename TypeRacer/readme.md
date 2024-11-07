## Homework 2) TypeRacer
_2.1 Description_

In this project, we will create a game similar to TypeRacer.

_2.2 Components_

-Arduino UNO (ATmega328P microcontroller)

-1x RGB LED (to signal if the word is typed correctly or not)

-2x Buttons (for starting/stopping the round and selecting difficulty level)

-5x Resistors (3x 330 ohm, 2x 1000 ohm)

-Breadboard

-Jumper wires

_2.3 Technical Details_

RGB LED - Status Indicator:

In standby mode, the LED will be white.

When the start button is pressed, the LED will blink for 3 seconds, indicating a countdown until the round begins.

During a round: The LED will be green if the text is entered correctly and will turn red in case of an error.

Start/Stop Button:


Standby Mode: If the game is stopped, pressing the button will start a new round after a 3-second countdown.

During a Round: If the round is active, pressing the button will stop it immediately.

Difficulty Button:

The difficulty button controls the speed at which words appear and can only be used in standby mode.

Each press cycles the difficulty level through: (Easy, Medium, Hard).

When the difficulty level changes, a message will be sent via serial: “Easy/Medium/Hard mode on!”

Word Generation:

A word dictionary will be created.

During a round, words will appear in the terminal in a random order.

If the current word is typed correctly, a new word will appear immediately. If not, a new word will appear after a time interval determined by the difficulty level.

Other Observations:

Each round lasts 30 seconds.

At the end of each round, the terminal will display how many words were typed correctly.

_2.4 Flow_

The game is in standby mode, and the RGB LED is white.

Select the game difficulty using the difficulty button, and the terminal will display “Easy/Medium/Hard mode on!”

Press the start/stop button.

The LED blinks for 3 seconds, and a countdown appears in the terminal: 3, 2, 1.

The LED turns green, and words start appearing to type.

When a word is typed correctly, the next word appears immediately. If the word isn’t typed within the time set by the difficulty level, a new word will appear.

An error turns the LED red. Use the Backspace key to correct the word.

After 30 seconds, the round ends, and the terminal displays the score: the total number of correctly typed words.

The game can be stopped at any time with the start/stop button.

_TinkerCad configuration_
![image](https://github.com/user-attachments/assets/f9160b20-b89c-4f9d-9450-bcec8dedf7ff)

_Physical configuration_
![image](https://github.com/user-attachments/assets/7fb12ed9-4127-4b42-9272-1f3a1895fce1)

_Demonstration video_
https://drive.google.com/file/d/1H_E1QWaYHdAx_HK017IXydU99ZK-ljaA/view?usp=sharing
