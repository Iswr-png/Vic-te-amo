<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Pra vc, Vic</title>
  <link href="https://fonts.googleapis.com/css2?family=Pacifico&family=Quicksand:wght@400;600&display=swap" rel="stylesheet">
  <style>
    body {
      margin: 0;
      padding: 0;
      font-family: 'Quicksand', sans-serif;
      background: url('https://example.com/sua-imagem-de-fundo.png') no-repeat center center fixed;
      background-size: cover;
      color: #4a2c2a;
      display: flex;
      flex-direction: column;
      align-items: center;
      text-align: center;
      overflow-x: hidden;
      position: relative;
    }

    /* Resto do CSS permanece o mesmo... */

    .heart {
      position: fixed;
      width: 20px;
      height: 20px;
      background: url('https://i.imgur.com/ZpUj36F.png') no-repeat center;
      background-size: contain;
      animation: float 6s linear infinite;
      pointer-events: none;
    }
  </style>
</head>
<body>
  <div class="container" id="intro">
    <h1>Abre isso com carinho...</h1>
    <div class="open-btn">
      <button onclick="openHeart()">Abrir o coração de Gidelson</button>
    </div>
  </div>

  <div class="container" id="main-content">
    <p>Vic,</p>
    <!-- Resto do conteúdo permanece o mesmo... -->
  </div>

  <div class="container" id="response">
    <img id="heart-gif" src="https://media.giphy.com/media/3o6Zt8A4h8M0g8g9uU/giphy.gif" alt="Coração fofo animado">
    <div class="message-final">Meu coração tá transbordando de felicidade! Esse meu amor por vc só me faz querer viver momentos lindos ao seu lado.</div>
  </div>

  <audio id="bg-music" src="https://cdn.pixabay.com/download/audio/2023/01/05/audio_735dfb77d4.mp3" autoplay loop></audio>

  <script>
    window.onload = function() {
      document.getElementById("intro").style.display = "block";
    }

    function openHeart() {
      document.getElementById("intro").style.display = "none";
      document.getElementById("main-content").style.display = "block";

      for (let i = 0; i < 20; i++) {
        let heart = document.createElement("div");
        heart.className = "heart";
        heart.style.left = Math.random() * 100 + "vw";
        heart.style.animationDuration = (Math.random() * 3 + 4) + "s";
        heart.style.animationDelay = (Math.random() * 3) + "s";
        document.body.appendChild(heart);

        setTimeout(() => heart.remove(), 10000);
      }
    }

    function showResponse() {
      document.getElementById("main-content").style.display = "none";
      document.getElementById("response").style.display = "block";
    }
  </script>
</body>
</html>
