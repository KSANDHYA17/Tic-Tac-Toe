# Tic-Tac-Toe
The algorithm for the Tic-Tac-Toe game code:

1. Define a function `p_board(board)` that takes the current state of the board as input and prints it.

2. Define a function `c_winner(board)` that takes the current state of the board as input and checks for a winner.

   a. Check rows:
      - For each row in the board:
        - If the first element of the row is equal to the second and third elements, and not an empty space, return the first element as the winner.

   b. Check columns:
      - For each column in the board:
        - If the first element of the column is equal to the second and third elements, and not an empty space, return the first element as the winner.

   c. Check diagonals:
      - If the first element of the top-left to bottom-right diagonal is equal to the second and third elements, and not an empty space, return the first element as the winner.
      - If the first element of the top-right to bottom-left diagonal is equal to the second and third elements, and not an empty space, return the first element as the winner.

   d. If no winner is found, return `None`.

3. Define a function `play_game()` that controls the gameplay.

   a. Initialize the board as a 3x3 grid with empty spaces.

   b. Set the initial player as 'X' and the winner as `None`.

   c. Start a game loop that continues until there is a winner.

      i. Print the current state of the board using `p_board(board)`.

      ii. Prompt the current player to enter their move by providing the row and column numbers.

      iii. Check if the chosen cell is already occupied. If it is, print an error message and continue to the next iteration of the loop.

      iv. If the chosen cell is valid, update the board by assigning the current player's symbol to the corresponding cell.

      v. Check for a winner by calling `c_winner(board)`. If a winner is found, assign the winner's symbol to the `winner` variable and break the game loop.

      vi. Switch the current player. If it is 'X', change it to 'O', and vice versa.

   d. After the game loop ends, print the final state of the board and display the winner.

4. Call the `play_game()` function to start the game.

That's the algorithm for the Tic-Tac-Toe game code. It outlines the steps involved in playing the game and determining the winner.
