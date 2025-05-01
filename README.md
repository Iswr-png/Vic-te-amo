<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Surpresa para Vic</title>
    <style>
        /* Manter o estilo básico do seu site */
        body {
            margin: 0;
            padding: 0;
            background: #fff;
            font-family: Arial, sans-serif;
            overflow: hidden;
        }

        #site {
            position: relative;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            flex-direction: column;
            text-align: center;
        }

        /* Texto principal em preto */
        #texto-principal {
            color: black;
            font-size: 40px;
            font-weight: bold;
            opacity: 0;
            animation: fadeIn 2s ease-in-out forwards;
        }

        @keyframes fadeIn {
            to {
                opacity: 1;
            }
        }

        /* Mensagem de alegria (com brilho e pulsação) */
        #mensagem-alegria {
            display: none;
            font-size: 50px;
            font-weight: bold;
            color: #ff66cc;
            text-shadow: 0 0 10px #ff66cc, 0 0 20px #ff66cc, 0 0 30px #ff66cc;
            animation: pulsar 1.5s ease-in-out infinite, brilho 2s ease-in-out infinite;
        }

        @keyframes pulsar {
            0% {
                transform: scale(1);
            }
            50% {
                transform: scale(1.2);
            }
            100% {
                transform: scale(1);
            }
        }

        @keyframes brilho {
            0% {
                text-shadow: 0 0 10px #ff66cc, 0 0 20px #ff66cc, 0 0 30px #ff66cc;
            }
            50% {
                text-shadow: 0 0 20px #ff66cc, 0 0 40px #ff66cc, 0 0 60px #ff66cc;
            }
            100% {
                text-shadow: 0 0 10px #ff66cc, 0 0 20px #ff66cc, 0 0 30px #ff66cc;
            }
        }

        /* Corações subindo pela tela */
        #coracoes {
            position: absolute;
            bottom: -100px;
            left: 50%;
            transform: translateX(-50%);
            animation: subir 5s infinite;
        }

        @keyframes subir {
            0% {
                bottom: -100px;
                opacity: 0;
            }
            50% {
                bottom: 40%;
                opacity: 1;
            }
            100% {
                bottom: 100%;
                opacity: 0;
            }
        }

        /* Luz que toma conta da tela */
        #luz {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(255, 255, 255, 0.8);
            opacity: 0;
            animation: luz 5s forwards;
        }

        @keyframes luz {
            0% {
                opacity: 0;
            }
            80% {
                opacity: 1;
            }
            100% {
                opacity: 0;
            }
        }

        /* Frase final com fade-in */
        #frase-final {
            display: none;
            font-size: 50px;
            font-weight: bold;
            text-align: center;
            opacity: 0;
            animation: fadeInFinal 2s ease-in-out forwards;
        }

        @keyframes fadeInFinal {
            0% {
                opacity: 0;
            }
            100% {
                opacity: 1;
            }
        }

        /* Fechar o site */
        @keyframes fecharSite {
            0% {
                opacity: 1;
            }
            100% {
                opacity: 0;
            }
        }

        #site.fechar {
            animation: fecharSite 3s forwards;
        }
    </style>
</head>
<body>
    <div id="site">
        <!-- Texto principal -->
        <div id="texto-principal">Uma surpresa para Vic!</div>
        
        <!-- Mensagem de alegria -->
        <div id="mensagem-alegria">Você é incrível!</div>

        <!-- Corações -->
        <div id="coracoes">❤️❤️❤️</div>

        <!-- Luz -->
        <div id="luz"></div>

        <!-- Frase final -->
        <div id="frase-final">Te amo, Vic! ❤️</div>
    </div>

    <script>
        window.onload = function() {
            // Mostrar o texto principal
            setTimeout(() => {
                document.getElementById("texto-principal").style.opacity = 1;
            }, 500);

            // Mostrar a mensagem de alegria
            setTimeout(() => {
                document.getElementById("mensagem-alegria").style.display = 'block';
            }, 2000); // Após o fade-in do texto principal

            // Mostrar os corações
            setTimeout(() => {
                document.getElementById("coracoes").style.display = 'block';
            }, 2000); // Após o texto principal e mensagem de alegria

            // Exibir luz
            setTimeout(() => {
                document.getElementById("luz").style.display = 'block';
            }, 4000); // Após a animação da mensagem de alegria e corações

            // Exibir a frase final
            setTimeout(() => {
                document.getElementById("frase-final").style.display = 'block';
            }, 8000); // Após a luz desaparecer

            // Fechar o site
            setTimeout(() => {
                document.getElementById("site").classList.add("fechar");
            }, 12000); // Após a frase final
        };
    </script>
</body>
</html>
