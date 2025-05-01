<!DOCTYPE html>
<html lang="pt">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pedido Aceito</title>
    <style>
        body {
            background-color: #ffe6f2;
            text-align: center;
            font-family: 'Comic Sans MS', cursive, sans-serif;
            color: #d63384;
        }
        .container {
            position: relative;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            min-height: 100vh;
        }
        .mensagem {
            font-size: 24px;
            font-weight: bold;
            background-color: #fff;
            padding: 20px;
            border-radius: 15px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
        }
        .gif {
            margin-top: 20px;
        }
        .decoracao {
            position: absolute;
            width: 100%;
            height: 100%;
            overflow: hidden;
            z-index: -1;
        }
        .coracao, .flor {
            position: absolute;
            width: 30px;
            height: 30px;
            opacity: 0.8;
            animation: flutuar 5s infinite alternate;
        }
        @keyframes flutuar {
            from { transform: translateY(0); }
            to { transform: translateY(-30px); }
        }
    </style>
</head>
<body>
    <div class="decoracao">
        <!-- Corações e flores animadas -->
        <div class="coracao" style="top: 10%; left: 20%;">❤️</div>
        <div class="coracao" style="top: 50%; left: 60%;">💖</div>
        <div class="flor" style="top: 30%; left: 80%;">🌸</div>
        <div class="flor" style="top: 70%; left: 40%;">🌺</div>
    </div>
    <div class="container">
        <div class="mensagem">
            💖 "Meu coração está explodindo de felicidade! Esse amor só me faz querer viver momentos inesquecíveis ao seu lado!" 💖
        </div>
        <div class="gif">
            <img src="https://face-oculta.github.io/Vic-te-amo/" alt="Coraçãozinho pulando de alegria" width="200">
        </div>
    </div>
</body>
</html>
