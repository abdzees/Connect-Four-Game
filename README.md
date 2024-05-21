# Connect 4 Game in Python

## Overview

This project is a Python implementation of the classic Connect 4 game. Players take turns dropping discs into a vertically suspended grid, aiming to connect four of their discs in a row either horizontally, vertically, or diagonally. The game features a customizable board size and interactive gameplay for two players.

## Features

- Customizable board size (rows and columns).
- Interactive CLI for player input.
- Alternating turns between two players: Player 0 (Red) and Player 1 (Yellow).
- Automatic detection of winning conditions.

## Requirements

- Python 3.x

## Setup

1. **Clone the repository:**
    ```sh
    git clone https://github.com/your-username/connect-4-python.git
    cd connect-4-python
    ```

2. **Run the game:**
    ```sh
    python connect4.py
    ```

## How to Play

1. **Start the game:**
    Run the script and you will be prompted to enter the number of rows and columns for the game board.

2. **Player turns:**
    - Player 0 (Red) starts the game.
    - Each player will be asked to choose a column to drop their disc.
    - The game checks for a winning condition after every move.

3. **Winning the game:**
    The game ends when a player connects four discs in a row or when the board is full, resulting in a draw.

## Code Description

### Main Functions

- `checkWinningState(field: List[List[Union[int, str]]]) -> bool`: Checks if there is a winning state in the game field.
- `generateField(nrow: int, ncol: int) -> List[List[str]]`: Generates a new game field with the specified number of rows and columns.
- `drawField(field: List[List[str]])`: Prints the game field.
- `doMove(player: int, field: List[List[str]])`: Handles player moves and updates the game field.
- `check_board(field: List[List[str]]) -> bool`: Checks if the board is full.
- `checkEmptySlot(col: int, field: List[List[str]]) -> int`: Finds the next empty slot in the specified column.
- `startGame(field: List[List[str]], nrow: int, ncol: int) -> int`: Main game loop that handles game progression and determines the winner.

## Example

```
Welcome to Connect-four! Please choose number of rows and columns for your board:
Rows: 6
Columns: 7

C O N N E C T 4 * * * *
Player-0 plays Red. Player-1 plays Yellow.
Red starts

Please input the column 0-6: 3
```


The game continues with players alternating turns until a winner is determined or the game ends in a draw.
