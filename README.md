# Speed Typing Test

This is a command-line typing test game built using the `curses` library in Python. The game presents the player with a target sentence, and the player must type the sentence as accurately and quickly as possible. The game calculates the player's typing speed in words per minute (WPM) and displays it on the screen.

## Installation

This game requires Python 3 and the `curses` library. To install `curses`, run the following command:

```
pip install windows-curses
```

For other operating systems, the installation process may vary. Please refer to the `curses` library documentation for more information.

## Usage

To start the game, simply run the following command:

```
python speed_typing_test.py
```

The game will begin with a welcome screen. Press any key to continue to the typing test. Once the test has begun, type the target text as quickly and accurately as you can. The game will automatically calculate your WPM and display it on the screen. Once you have completed the target text, the game will display your final WPM and prompt you to continue by pressing any key (or exit the game by pressing the ESC key).

## Code Analysis

The `speed_typing_test.py` script imports the `curses` library and defines three functions: `start_screen`, `display_text`, and `wpm_test`. The script then calls the `wrapper` function from `curses`, passing in the `main` function as an argument.

The `start_screen` function simply clears the screen and displays a welcome message. It waits for any key to be pressed before continuing.

The `display_text` function displays the target text, the player's current typing progress, and their WPM on the screen. It iterates over each character in the player's current progress and highlights any incorrect characters in red.

The `wpm_test` function is the core of the game. It initializes the target text, sets up the necessary variables, and enters a loop that updates the screen with the player's typing progress in real-time. It calculates the player's WPM by dividing the length of the current progress by the time elapsed since the start of the test. If the player completes the target text, the loop exits and the function returns the player's final WPM.

The `main` function initializes three color pairs using the `curses.init_pair` function. It then displays the welcome screen and enters a loop that continually calls the `wpm_test` function until the player decides to quit by pressing the ESC key. Once the player completes the target text, the function displays a message prompting the player to continue.

Overall, the code is well-structured and easy to read. The use of the `curses` library allows for real-time updating of the screen, and the implementation of color pairs and highlighting adds a nice touch to the game. The code could be further optimized by refactoring common code blocks into separate functions or classes, but for a simple typing test game, the current implementation is sufficient.
