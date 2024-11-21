## Homework 3) Quick Time
_3.1 Description_

In this project, as a team we created a competitive reflex game for two players, where both participants compete to achieve the highest score by testing their reaction speed. The project will be carried out in teams of two.

Each player will have their own buttons and LEDs, and the game will consist of multiple rounds. The objective of each player is to press the button corresponding to the color displayed on their RGB LED as quickly as possible. The score for each player will be displayed on an LCD and updated throughout the game. At the end of the game, the player with the highest score will be declared the winner.

_3.2 Components_

-6x LEDs (2 groups of 3 LEDs, each group must have different colors)

-2x RGB LEDs (1 for each player)

-6x Buttons (3 for each player)

-1x LCD

-1x Servo motor

-2x Breadboards

-Wires

-2x Arduino Uno

_3.3 Flow_

_Initialization_

The game starts by displaying a welcome message on the LCD. Pressing a button triggers the start of the game.

To start the game, the start button can be implemented in one of the following flexible ways, at the team's discretion:

Any button starts the game: The game begins when any button is pressed.
A specific button starts the game: A clearly marked button on the breadboard is designated to start the game.
A dedicated 7th button: An additional button is added exclusively for starting the game.

_Round Progression_

Each player has three buttons, each associated with an LED of a different color, and a fourth RGB LED.
During each round, one player is active.
The active player's RGB LED lights up in a color corresponding to one of their buttons. The player must press the button matching the color of the RGB LED as quickly as possible to score points. Faster reactions yield higher scores.
At the end of each round, the LCD displays the updated scores of both players.
Throughout the game, the LCD continuously shows the score of each player.

_Timing and Game Conclusion_

The servo motor rotates throughout the game, indicating progress. A full rotation of the servo motor marks the end of the game (you decide how fast it moves).
At the end of the game, the LCD displays the winner's name and final score for a few seconds, then returns to the start screen with the welcome message.

_3.4 Technical Details_

SPI Communication

This project involves many connections—so many that a single Arduino Uno does not provide enough GPIO pins. Therefore, this project requires two Arduino Uno boards that will communicate using SPI.

The master Arduino will be responsible for controlling the LCD, servo motor, and keeping track of the game's state (e.g., each player’s score, the LED to be lit, etc.).
The slave Arduino will control the buttons and LEDs, receiving messages from the master Arduino to know which LED to light and sending back messages about which button was pressed.

Buttons

Starting the Game: The start button can be implemented in various ways:
Any button can start the game.

A specific button is designated to start the game (it should be clearly marked on the breadboard).

A dedicated 7th button can be added to start the game.

While the game is ongoing, buttons should only be used for game control and not reset progress.

Only the active player's buttons should control the game during their turn.

Due to limited GPIO pins even with 2 Arduinos, button multiplexing using resistors is recommended (see this video).

LEDs

Each button is associated with an LED of a different color. During the game, these LEDs must remain lit to show which color corresponds to each button.

The RGB LED must light up in one of the three button colors during the player’s round.

The RGB LED must turn off when it is not the active player’s turn.

LCD

Use the LiquidCrystal library to control the LCD.

Ensure the brightness and contrast are set appropriately to make the text visible.

Only pins D4-D7 will be used for the LCD data lines.

During the game, the LCD must display the scores of both players.

Servo Motor

The servo motor will start at a position of 0 degrees and move counterclockwise to indicate the passage of time.

Be cautious with the value sent to the servo motor. Using the Servo.h library, commands sent to the servo motor specify absolute rotation, not relative to the current position.

_TinkerCad configuration_

![image](https://github.com/user-attachments/assets/c3702f54-e465-430a-aa4b-0fd46d32cd99)


_Physical configuration_

![image](https://github.com/user-attachments/assets/dfcdf8e9-825b-4c38-9af8-44bbc6d0edb5)

