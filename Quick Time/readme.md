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

