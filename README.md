# Blitz-Coin
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>TapSwap Game</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #f0f0f0;
        }
        h1 {
            color: #4CAF50;
        }
        .game-container {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            grid-gap: 10px;
            width: 300px;
            margin: 20px auto;
        }
        .game-item {
            width: 80px;
            height: 80px;
            background-color: #4CAF50;
            border-radius: 10px;
            cursor: pointer;
            transition: background-color 0.3s ease;
        }
        .game-item.active {
            background-color: #f44336;
        }
        .score-container {
            margin-top: 20px;
        }
        .score {
            font-size: 24px;
            color: #333;
        }
        .btn {
            padding: 10px 20px;
            background-color: #4CAF50;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        .btn:hover {
            background-color: #45a049;
        }
    </style>
</head>
<body>
    <h1>TapSwap Game</h1>
    <div class="game-container">
        <!-- Game items (clickable boxes) will be added here dynamically -->
    </div>
    <div class="score-container">
        <p class="score">Score: <span id="score">0</span></p>
        <button class="btn" id="resetButton">Reset Game</button>
    </div>

    <script>
        // Variables for the game
        const gameContainer = document.querySelector('.game-container');
        const scoreDisplay = document.getElementById('score');
        const resetButton = document.getElementById('resetButton');

        let score = 0;
        let activeItems = [];

        // Function to create game items
        function createGameItems() {
            // Clear previous items
            gameContainer.innerHTML = '';
            activeItems = [];

            // Create 9 game items (3x3 grid)
            for (let i = 0; i < 9; i++) {
                const item = document.createElement('div');
                item.classList.add('game-item');
                item.addEventListener('click', () => handleItemClick(item));
                gameContainer.appendChild(item);
            }
        }

        // Function to handle item click
        function handleItemClick(item) {
            // If the item is already active (clicked previously), do nothing
            if (item.classList.contains('active')) return;

            // Increase score and make the item active
            score++;
            item.classList.add('active');
            scoreDisplay.textContent = score;

            // If 3 items are active, end the game
            if (score === 3) {
                alert('You Win! Game Over');
                resetGame();
            }
        }

        // Reset the game
        function resetGame() {
            score = 0;
            scoreDisplay.textContent = score;
            createGameItems();
        }

        // Reset button functionality
        resetButton.addEventListener('click', resetGame);

        // Start the game when the page loads
        createGameItems();
    </script>
</body>
</html>
        
