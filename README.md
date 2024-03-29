# ccontrol
ccontrol is a library designed for creating text-based user interfaces in Python. It simplifies the rendering of text to the screen, user input processing, and interacting with terminal functionalities without directly exposing the underlying complexity.
## Features
- Easy to use functions for displaying text with various attributes such as color and style
- Functions to initialize custom terminal screen settings
- Helper functions for creating input boxes and handling key presses
## Installation
This library is designed to work as a part of a Python project. Perfect for applications that require direct terminal manipulations for text-based interfaces.

To use ccontrol, you will need to ensure that you have Python installed on your system. No additional packages or curses-specific modules are required to be mentioned as dependencies for the basic running of ccontrol.
## Quick Start
Here's a quick example on how you can utilize the ccontrol library:
```
import ccontrol

# Initialize the screen with default settings
stdscr = ccontrol.initialize_screen()

try:
    # Display text at a specific location with color and bold style
    ccontrol.text(stdscr, x=10, y=5, text="Hello, ccontrol!", color_pair=ccontrol.BLUE, style=ccontrol.BOLD)

    # Create an input box for user input
    user_input = ccontrol.input_box(stdscr, x=10, y=10, width=20, title="Input:")
    print("User input:", user_input)

    # Wait for a key press
    key = ccontrol.get_key(stdscr)
    print("Key pressed:", key)

finally:
    # Make sure to end the ccontrol application
    ccontrol.exit_programm()
```
Note that while the ccontrol library uses the curses module internally, its API abstracts away the curses-specific details, providing a straightforward interface for building text user interfaces.
## Documentation
Functions provided by ccontrol include, but are not limited to:

- initialize_screen:
  Accepts various boolean flags to customize terminal settings such as hiding the cursor or enabling the keypad for special keys.
- text:
  Outputs text at a given screen location with the provided colors and styling attributes.
- input_box:
  Renders a simple input box at the specified screen location and accepts user input.
- get_key:
  Waits for a user key press and returns the pressed key's keycode.
## Color and Style Constants
The ccontrol library comes with predefined constants for colors and text attributes:

- Colors:
  - WHITE
  - RED
  - YELLOW
  - GREEN
  - BLUE
  - CYAN
  - MAGENTA
- Styles:
  - NORMAL
  - BOLD
  - UNDERLINE
  - REVERSE
  - BLINK

These can be used to modify the text output's appearance on the terminal.
## Contributing
Contributions to the ccontrol library are welcome. If you have a suggestion that would make this library better, please fork the repo and create a pull request.
## License
Licensed under the MIT License. See the LICENSE file for more details.

