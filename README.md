# Blitz-Coin
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mini App</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
        }
    </style>
</head>
<body>
    <h1>Welcome to My Mini App!</h1>
    <button onclick="Telegram.WebApp.showAlert('Hello World!')">Show Alert</button>
    <script src="https://telegram.org/js/telegram-web-app.js"></script>
    <script>
        Telegram.WebApp.ready();
    </script>
</body>
</html>
