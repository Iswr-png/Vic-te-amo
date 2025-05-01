<!DOCTYPE html>
<html lang="pt">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pedido Aceito</title>
    <style>
        body {
            background: linear-gradient(to bottom, #ffccdd, #ffe6f2);
            text-align: center;
            font-family: 'Comic Sans MS', cursive, sans-serif;
            color: #d63384;
            overflow: hidden;
        }
        .container {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            min-height: 100vh;
            position: relative;
        }
        .mensagem {
            font-size: 28px;
            font-weight: bold;
            background: rgba(255, 255, 255, 0.8);
            padding: 20px;
            border-radius: 15px;
            box-shadow: 0 0 15px rgba(255, 105, 180, 0.5);
            animation: brilho 2s infinite alternate;
        }
        @keyframes brilho {
            from { box-shadow: 0 0 15px rgba(255, 105, 180, 0.5); }
            to { box-shadow: 0 0 25px rgba(255, 105, 180, 0.8); }
        }
        .gif {
            margin-top: 20px;
        }
        .decoracao {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: -1;
        }
        .coracao {
            position: absolute;
            font-size: 30px;
            opacity: 0.7;
            animation: flutuar 3s infinite alternate;
        }
        .flor {
            position: absolute;
            font-size: 25px;
            opacity: 0.5;
            animation: cair 4s infinite linear;
        }
        @keyframes flutuar {
            from { transform: translateY(0); }
            to { transform: translateY(-20px); }
        }
        @keyframes cair {
            0% { transform: translateY(-50px); opacity: 1; }
            100% { transform: translateY(100vh); opacity: 0; }
        }
    </style>
</head>
<body>
    <div class="decoracao">
        <div class="coracao" style="top: 10%; left: 20%;">❤️</div>
        <div class="coracao" style="top: 50%; left: 60%;">💖</div>
        <div class="flor" style="top: -50px; left: 30%;">🌸</div>
        <div class="flor" style="top: -50px; left: 70%;">🌺</div>
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
