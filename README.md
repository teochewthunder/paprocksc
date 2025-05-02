# Paper Rock Scissors Game (TBA)

## Images used
- `symbol.jpg` default image
- `symbol_paper.jpg` image for Paper
- `symbol_rock.jpg` image for Rock
- `symbol_scissors.jpg` image for Scissors
- `symbol_spock.jpg` image for Spock
- `symbol_lizard.jpg` image for Lizard

## HTML

## CSS

## JavaScript
- `symbols`: An array of all possible symbols. Each symbol is an object with the properties...
  - `name `: THis is a string which is the name of the current symbol. e.g, "rock"
  - `beats`: This is an array containing strings. These strings are the names of symbols that the current symbol beats. e.g, ["scissors", "lizard"]
- `range`: This is either 3 or 5. It represents the first `n` elements of the `symbols` array that will be in use.
- `score`: This is an array with two elements. The first element is an integer representing how many rounds the user has won. The second element is an integer representing how many rounds the computer has won. 
- `round`: This is an array with two elements. The first element is a string representing the symbol that the user is using. The second element is a string representing the symbol that the computer is using.
- `active`: A boolean that determiens if buttons are clickable.
- `timer`: Used to set an interval if mode is Auto.
- `start()`:
  - determine if game is in Classic or Extended Mode. (`range` is then set)
  - determine if game is in Auto Mode. (`auto` is then set)
  - hide Start button, show Stop button.
  - set `active` to `true`.
  - if game is in Auto Mode:
    - run `chooseSymbol()` with "auto" as an argument, every 1.5 seconds.
    -  otherwise, run `showOptions()`.
- `stop()`:
- `showOptions()`: Uses `range` to decide which symbol buttons to show.
- `chooseSymbol(symbol)`:
  - if `active` is `false`, exit method.
  - `symbol` can be "", "auto" or ("rock", "paper", "scissors", "spock", "lizard")
    - "": randomly select a symbol for the second element of `round`. Exit method.
    - "auto": randomly select a symbol for the first element of `round`. Then run `chooseSymbol()` recursively with "" as argument.
    - ("rock", "paper", "scissors", "spock", "lizard"): the value will be the first value of `round`. Then run `chooseSymbol()` recursively with "" as argument.
  - run `showSymbol()` to show the appropriate symbols in `round`.
  - run `whowins()`.
- `showSymbol(index, symbol)`: Uses `symbol` as the background image for the div referenced by `index`.
- `showScore()`: Displays the values of the `score` property in the appropriate placeholders.
- `showColor(index, colorCode)`: Uses `colorCode` as the outline color for the div referenced by `index`.
- `whowins()`:
- `xbeatsy(x, y)`: `x` references the element in `symbols` where `x` matches the `name` property. Returns `true` if `y` is in the `beats` array of that element, `false` otherwise.
