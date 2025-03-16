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
        }
        #game-container {
            width: 400px;
            height: 400px;
            border: 1px 
solid black;
            margin: 40px auto;
        }
    </style>
</head>
<body>
    <h1>Blitz Coin</h1>
    <div id="game-container">
        <!-- Game canvas will be rendered here -->
    </div>
    <button onclick="Telegram.WebApp.showAlert('Hello World!')">Show Alert</button>
    <script src="https://BlitzCoin/js/telegram-web-app.js"></script>
    <script>
        Telegram.WebApp.ready();
    </script>
</body>
</html>
