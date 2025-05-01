<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Coração Animado</title>
    <style>
        /* Estilo geral da página */
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #f0f0f0; /* Cor de fundo */
            font-family: Arial, sans-serif; /* Fonte padrão */
            margin: 0; /* Remove margens padrão */
        }
        /* Estilo do contêiner */
        .container {
            text-align: center; /* Centraliza o texto */
            background-color: #fff; /* Fundo branco */
            border-radius: 10px; /* Bordas arredondadas */
            padding: 20px; /* Espaçamento interno */
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1); /* Sombra suave */
        }
        /* Estilo da mensagem final */
        .message-final {
            margin-top: 20px; /* Espaçamento acima da mensagem */
            font-size: 20px; /* Tamanho da fonte */
            color: #ff4d4d; /* Cor da fonte */
            font-weight: bold; /* Negrito */
        }
        /* Estilo do GIF */
        #heart-gif {
            width: 200px; /* Ajuste o tamanho do GIF conforme necessário */
            animation: pulse 1s infinite; /* Animação de pulsar */
        }
        /* Definição da animação de pulsar */
        @keyframes pulse {
            0% { transform: scale(1); } /* Tamanho original */
            50% { transform: scale(1.1); } /* Aumenta o tamanho */
            100% { transform: scale(1); } /* Retorna ao tamanho original */
        }
    </style>
</head>
<body>
    <div class="container" id="response">
        <!-- GIF de coração -->
        <img id="heart-gif" src="https://drive.google.com/uc?id=1lBox6RTL1e59nva547a3-O4S7DZ9Na1N" alt="Coração fofo animado">
        
        <!-- Mensagem que aparece abaixo do GIF -->
        <div class="message-final">Meu coração tá transbordando de felicidade! Esse meu amor por você só me faz querer viver momentos lindos ao seu lado 💖.</div>
    </div>
</body>
</html>
