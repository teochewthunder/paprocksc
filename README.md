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
- `start`:
- `stop`:
- `showOptions`: Uses `range` to decide which symbol buttons to show.
- `chooseSymbol`
- `showSymbol`
- `showScore`
- `showColor`
- `whowins`
- `xbeatsy`
