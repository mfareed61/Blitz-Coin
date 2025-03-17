# Blitz-Coin
<!DOCTYPE html>
<html lang="English">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Blitz Coin</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #f0f0f0;
        }
        #game-container {
            width: 400px;
            height: 400px;
            border: 1px solid black;
            margin: 40px auto;
            background-image: url('hamster-background.png');
            background-size: cover;
        }
        .hamster-button {
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            background-color: #4CAF50;
            color: #fff;
            cursor: pointer;
        }
        .hamster-button:hover {
            background-color: #3e8e41;
        }
    </style>
</head>
<body>
    <h1>Blitz Coin</h1>
    <div id="game-container">
        <!-- Game canvas will be rendered here -->
    </div>
    <button class="hamster-button" onclick="Telegram.WebApp.showAlert('Blitz Coin is coming soon!')">Play Now</button>
    <script src="https://telegram.org/js/telegram-web-app.js"></script>
    <script>
        Telegram.WebApp.ready();
    </script>
</body>
</html>
