# Battleship

## Setup

These commands are a helpful quick start. You may choose to ignore them completely and create your own directory structure. If you choose to use this recommendation, just copy the commands below and paste. It doesn't matter what directory you are currently in.


```bash
mkdir -p ~/workspace/exercises/rich-browser/battleship && cd $_
```

## Instructions

Create a working 2 player battleship game.

### MVP

1.  Game must keep track of Player 1 and Player 2
1.  Each player gets 5 ships - destroyer (2 holes), submarine (3 holes), cruiser (3 holes), battleship (4 holes), carrier (5 holes) - which they can place on their game board where they want, oriented horizontally
1.  Players should be able to see a representation of their board and the board they are attacking.
1. Use Firebase to keep track of player moves.
1. Use SASS for all styling of the board, and pieces.

### Bonus Features

1.  Players should be able to rotate their ships either horizontally or vertically.
1.  Add in user authentication, so that each player should be able to use their own computer to play.
1.  Add a leaderboard feature to keep track of player scores.