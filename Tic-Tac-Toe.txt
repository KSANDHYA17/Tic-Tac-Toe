def p_board(board):
    for row in board:
        print(' | '.join(row))
        print('-' * 9)

def c_winner(board):
    # Check rows
    for row in board:
        if row[0] == row[1] == row[2] != ' ':
            return row[0]

    # Check columns
    for col in range(3):
        if board[0][col] == board[1][col] == board[2][col] != ' ':
            return board[0][col]

    # Check diagonals
    if board[0][0] == board[1][1] == board[2][2] != ' ':
        return board[0][0]
    if board[0][2] == board[1][1] == board[2][0] != ' ':
        return board[0][2]

    return None

def play_game():
    board = [[' ', ' ', ' '],
             [' ', ' ', ' '],
             [' ', ' ', ' ']]

    c_player = 'X'
    winner = None

    while not winner:
        p_board(board)

        # Get player's move
        row = int(input("Enter the row (0-2): "))
        col = int(input("Enter the column (0-2): "))

        # Check if the move is valid
        if board[row][col] != ' ':
            print("Invalid move. Try again.")
            continue

        # Update the board
        board[row][col] = c_player

        # Check for a winner
        winner = c_winner(board)

        # Switch players
        c_player = 'O' if c_player == 'X' else 'X'

    p_board(board)
    print(f"Player {winner} wins!")

play_game()
