---
{"dg-publish":true,"permalink":"/0-vault/1-notas-literais/anelo/scrabble-em-python-2/","tags":["ANELO"],"dgHomeLink":true,"dgShowLocalGraph":true,"dgShowFileTree":true,"dgEnableSearch":true,"noteIcon":""}
---

# Scrabble em python 2

## criado em: 
-  24-05-2023 - 09:44

### Conteúdo Relacionado
- notas: [[0 - VAULT/1 NOTAS LITERAIS/ANELO/Python Scrabble\|Python Scrabble]]
- tags: #ANELO 
- Fontes & Links: 

---

>Can you make a step by step guide to create a scrabble board, where I need to create a 2D array/grid to represent the board and handle the placing of words on the board. I will need help to create a way to validate the word placement on the board (e.g., checking if the word is connected to existing words, if it fits on the board, etc.).

Certainly! Here's a step-by-step guide to creating a Scrabble board with a 2D array/grid representation and handling the placement of words:

Step 1: Set up the board
- Define the size of the board (e.g., 15x15):
```python
BOARD_SIZE = 15
board = [[' ' for _ in range(BOARD_SIZE)] for _ in range(BOARD_SIZE)]
```

Step 2: Create helper functions
- Create a function to print the current state of the board:
```python
def print_board(board):
    for row in board:
        print(' '.join(row))
```
- Create a function to check if a given word placement is valid:
```python
def is_valid_word_placement(word, row, col, direction, board):
    # Check if the word exceeds the board boundaries
    if direction == 'across':
        if col + len(word) > BOARD_SIZE:
            return False
    elif direction == 'down':
        if row + len(word) > BOARD_SIZE:
            return False

    # Check if the word intersects with existing letters
    for i, letter in enumerate(word):
        if direction == 'across':
            if board[row][col + i] != ' ' and board[row][col + i] != letter:
                return False
        elif direction == 'down':
            if board[row + i][col] != ' ' and board[row + i][col] != letter:
                return False

    # Check if the word is connected to existing letters
    if direction == 'across':
        if col > 0 and board[row][col - 1] != ' ':
            return True
        if col + len(word) < BOARD_SIZE and board[row][col + len(word)] != ' ':
            return True
        for i in range(len(word)):
            if row > 0 and board[row - 1][col + i] != ' ':
                return True
            if row < BOARD_SIZE - 1 and board[row + 1][col + i] != ' ':
                return True
    elif direction == 'down':
        if row > 0 and board[row - 1][col] != ' ':
            return True
        if row + len(word) < BOARD_SIZE and board[row + len(word)][col] != ' ':
            return True
        for i in range(len(word)):
            if col > 0 and board[row + i][col - 1] != ' ':
                return True
            if col < BOARD_SIZE - 1 and board[row + i][col + 1] != ' ':
                return True

    return False
```

Step 3: Implement the game loop
- Set up a loop to keep the game running until a player decides to quit:
```python
while True:
    print_board(board)
    
    word = input("Enter a word (or 'q' to quit): ").upper()
    
    if word == 'Q':
        break
    
    row = int(input("Enter the row number (0-14): "))
    col = int(input("Enter the column number (0-14): "))
    direction = input("Enter the direction (across/down): ")
    
    if not is_valid_word_placement(word, row, col, direction, board):
        print("Invalid word placement. Try again.")
        continue
    
    # Place the word on the board
    for i, letter in enumerate(word):
        if direction == 'across':
            board[row][col + i] = letter
        elif direction == 'down':
            board[row + i][col] = letter
```

This guide provides

 a basic implementation of a Scrabble board with word placement validation. You can expand on this foundation by adding scoring, tracking player racks, dictionary validation, and other features to make the game more complete.

Yes, you can certainly create the Scrabble board using HTML and CSS. While designing the board in Adobe Illustrator and exporting it as a PNG file is one approach, it would be more flexible and scalable to create the board using HTML and CSS directly.

Here's a general outline of how you can create the Scrabble board using HTML and CSS:

Step 1: Set up the HTML structure
- Create an HTML file and define the basic structure:
```html
<!DOCTYPE html>
<html>
<head>
    <title>Scrabble Board</title>
    <link rel="stylesheet" type="text/css" href="styles.css">
</head>
<body>
    <div class="board">
        <!-- Add the grid squares here -->
    </div>
</body>
</html>
```

Step 2: Define the CSS styles
- Create a CSS file (e.g., "styles.css") and define the necessary styles:
```css
.board {
    display: grid;
    grid-template-columns: repeat(15, 40px);  /* Adjust the size as needed */
    grid-template-rows: repeat(15, 40px);  /* Adjust the size as needed */
    gap: 2px;  /* Adjust the gap between squares as needed */
    background-color: #f2f2f2;  /* Adjust the background color as needed */
    padding: 10px;  /* Adjust the padding as needed */
}

.square {
    background-color: #ffffff;  /* Adjust the square color as needed */
    border: 1px solid #cccccc;  /* Adjust the border color as needed */
    text-align: center;
    font-size: 16px;  /* Adjust the font size as needed */
    line-height: 40px;  /* Adjust the line height as needed */
    font-weight: bold;
}
```

Step 3: Generate the grid squares dynamically
- In the HTML file, use JavaScript or a server-side language like Python to generate the grid squares dynamically:
```html
<script>
    const boardSize = 15;  // Adjust the size as needed
    const boardContainer = document.querySelector('.board');
    
    // Generate the grid squares
    for (let i = 0; i < boardSize; i++) {
        for (let j = 0; j < boardSize; j++) {
            const square = document.createElement('div');
            square.classList.add('square');
            boardContainer.appendChild(square);
        }
    }
</script>
```

Step 4: Customize the board appearance
- Adjust the CSS styles in "styles.css" to match your desired design, including the background colors, border styles, font sizes, and other visual elements.

By following these steps, you can create a Scrabble board using HTML and CSS, allowing you to have more control and flexibility over the board's design and responsiveness.