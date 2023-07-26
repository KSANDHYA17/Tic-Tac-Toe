# Tic-Tac-Toe

1. The `board` is represented as a list of length 9, where each element represents a cell on the Tic-Tac-Toe board. Initially, all cells are set to "-". This will be used to track the current state of the game.

2. `currentPlayer` variable is initialized to "X", indicating that "X" will be the first player to make a move.

3. The `winner` variable is initialized to `None`. It will be used to track the winner of the game.

4. `gameRunning` is set to `True` to indicate that the game is ongoing.

5. The `printBoard()` function is defined to display the current state of the Tic-Tac-Toe board.

6. The `playerInput()` function is defined to take input from the current player and update the board based on their move. It validates the input and ensures that the move is valid.

7. Three functions, `checkHorizontal()`, `checkRow()`, and `checkDiagonal()`, are defined to check for a win condition. If any of these functions return `True`, the game is won by the current player, and the `winner` variable is updated accordingly.

8. The `checkTie()` function checks if the game is a tie, i.e., if no more moves are possible, and none of the players has won. If the game is a tie, it displays the board and prints a message indicating a tie.

9. The `checkWin()` function calls the win-checking functions and determines if the current player has won the game. If there is a winner, it displays a message indicating the winner.

10. The `switchPlayer()` function switches the value of `currentPlayer`, i.e., from "X" to "O" or from "O" to "X", so that the next player can make their move.

11. The main game loop starts with `while gameRunning:`. Inside the loop, it prints the board, takes input from the current player, checks for a win or tie condition, and switches the player. The loop continues until `gameRunning` is set to `False` (which happens when there is a winner or the game is a tie).

Overall, this code allows two players to play Tic-Tac-Toe game. It takes player input, displays the board after each move, checks for a win or tie condition, and announces the winner or tie when the game ends.
