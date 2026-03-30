<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Signet Wallet</title>
    <script src="https://telegram.org/js/telegram-web-app.js"></script>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@600&display=swap" rel="stylesheet">
    <style>
        body {
            background-color: #1a1a1a;
            color: #e0e0e0;
            font-family: sans-serif;
            margin: 0;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            min-height: 100vh;
        }
        .header { 
            font-family: 'Playfair Display', serif;
            font-size: 24px; 
            letter-spacing: 5px; 
            color: #c5a059;
            text-transform: uppercase;
            margin-bottom: 40px;
        }
        .card {
            background: #222222;
            width: 85%;
            max-width: 320px;
            padding: 40px 10px;
            text-align: center;
            border: 1px solid rgba(197, 160, 89, 0.4);
            box-shadow: 0 10px 30px rgba(0,0,0,0.5);
        }
        .balance-label { color: #888; font-size: 11px; text-transform: uppercase; letter-spacing: 2px; margin-bottom: 10px; }
        .balance-value { font-family: 'Playfair Display', serif; font-size: 44px; color: #c5a059; }
        .btn-group { display: flex; gap: 15px; width: 85%; max-width: 320px; margin-top: 30px; }
        .btn {
            background: transparent;
            color: #c5a059;
            border: 1px solid #c5a059;
            padding: 15px;
            flex: 1;
            text-transform: uppercase;
            font-weight: bold;
            font-size: 13px;
        }
    </style>
</head>
<body>
    <div class="header">SIGNET</div>
    <div class="card">
        <div class="balance-label">Баланс</div>
        <div class="balance-value">0.00 ₽</div>
    </div>
    <div class="btn-group">
        <button class="btn">Ввод</button>
        <button class="btn">Вывод</button>
    </div>
    <script>
        const tg = window.Telegram.WebApp;
        tg.ready();
        tg.expand();
    </script>
</body>
</html>
