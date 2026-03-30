<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>SIGNET</title>
    <script src="https://telegram.org/js/telegram-web-app.js"></script>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@600&display=swap" rel="stylesheet">
    <style>
        body {
            background-color: #1a1a1a;
            color: #ffffff;
            font-family: -apple-system, BlinkMacSystemFont, sans-serif;
            margin: 0;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            min-height: 100vh;
        }
        .header { 
            font-family: 'Playfair Display', serif;
            font-size: 22px; 
            letter-spacing: 6px; 
            color: #c5a059;
            text-transform: uppercase;
            margin-bottom: 40px;
        }
        .card {
            background: #222222;
            width: 80%;
            max-width: 300px;
            padding: 40px 20px;
            text-align: center;
            border: 1px solid rgba(197, 160, 89, 0.3);
            box-shadow: 0 10px 40px rgba(0,0,0,0.5);
        }
        .balance-label { 
            color: #888; 
            font-size: 11px; 
            text-transform: uppercase; 
            letter-spacing: 2px; 
            margin-bottom: 15px; 
        }
        .balance-value { 
            font-family: 'Playfair Display', serif;
            font-size: 48px; 
            color: #c5a059;
            line-height: 1;
        }
        .currency {
            font-size: 24px;
            display: block;
            margin-top: 10px;
        }
        .btn-group { 
            display: flex; 
            gap: 15px; 
            width: 80%; 
            max-width: 300px; 
            margin-top: 40px; 
        }
        .btn {
            background: transparent;
            color: #c5a059;
            border: 1px solid #c5a059;
            padding: 15px;
            flex: 1;
            text-transform: uppercase;
            font-size: 12px;
            letter-spacing: 1px;
            font-weight: 600;
        }
    </style>
</head>
<body>
    <div class="header">SIGNET</div>

    <div class="card">
        <div class="balance-label">Баланс</div>
        <div class="balance-value">
            0.00
            <span class="currency">₽</span>
        </div>
    </div>

    <div class="btn-group">
        <button class="btn" onclick="tgAlert()">Ввод</button>
        <button class="btn" onclick="tgAlert()">Вывод</button>
    </div>

    <script>
        const tg = window.Telegram.WebApp;
        tg.ready();
        tg.expand();
        function tgAlert() {
            tg.HapticFeedback.impactOccurred('medium');
            tg.showAlert("Система SIGNET готовится к запуску.");
        }
    </script>
</body>
</html>
