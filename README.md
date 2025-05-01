<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Pra você, Vic</title>
  <link href="https://fonts.googleapis.com/css2?family=Great+Vibes&display=swap" rel="stylesheet">
  <style>
    body {
      margin: 0;
      padding: 0;
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(to bottom, #ffe6f0, #ffe0e9);
      color: #4a2c2a;
      display: flex;
      flex-direction: column;
      align-items: center;
      text-align: center;
      overflow-x: hidden;
      position: relative;
    }

    .container {
      padding: 30px 20px;
      max-width: 700px;
      animation: fadeIn 1s ease;
      z-index: 2;
    }

    @keyframes fadeIn {
      from {
        opacity: 0;
        transform: translateY(20px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    h1 {
      font-size: 30px;
      color: #d6336c;
      margin-top: 100px;
      font-family: 'Great Vibes', cursive;
      animation: bounce 1.5s infinite alternate;
    }

    @keyframes bounce {
      from {
        transform: translateY(0);
      }
      to {
        transform: translateY(-10px);
      }
    }

    p {
      font-size: 18px;
      line-height: 1.7;
      margin-bottom: 20px;
      font-family: 'Great Vibes', cursive;
    }

    .final {
      font-weight: bold;
      font-size: 22px;
      color: #b20043;
      margin-top: 30px;
      font-family: 'Great Vibes', cursive;
    }

    .buttons, .open-btn {
      margin-top: 30px;
    }

    button {
      margin: 10px;
      padding: 12px 24px;
      font-size: 16px;
      background-color: #ff99bb;
      border: none;
      border-radius: 10px;
      color: white;
      cursor: pointer;
      transition: 0.3s;
    }

    button:hover {
      background-color: #ff77a9;
    }

    #heart-gif {
      width: 120px;
      height: auto;
      margin: 30px auto 0;
      display: block;
      animation: fadeIn 1.2s ease forwards;
    }

    #intro, #main-content, #response {
      display: none;
    }

    .message-final {
      font-size: 24px;
      color: #d6336c;
      font-weight: bold;
      margin-top: 20px;
      animation: fadeIn 1.5s ease;
    }

    /* Animação de corações e flores flutuando no fundo */
    .floating-objects {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      pointer-events: none;
      z-index: 1;
    }

    .floating-heart,
    .floating-flower {
      position: absolute;
      animation: float 10s linear infinite;
    }

    .floating-heart {
      width: 50px;
      height: 50px;
      background: url('https://media.tenor.com/images/4c39b8a3000535bcdfe3fc327c7fae4d/tenor.gif') no-repeat center;
      background-size: contain;
    }

    .floating-flower {
      width: 40px;
      height: 40px;
      background: url('https://media.tenor.com/images/d6818cc33ad364fe3500d1d050f01e4b/tenor.gif') no-repeat center;
      background-size: contain;
    }

    @keyframes float {
      0% {
        transform: translateY(0) translateX(0);
      }
      50% {
        transform: translateY(-100px) translateX(50px);
      }
      100% {
        transform: translateY(0) translateX(0);
      }
    }
  </style>
</head>
<body>
  <div class="floating-objects">
    <div class="floating-heart" style="top: 20%; left: 10%; animation-duration: 8s;"></div>
    <div class="floating-heart" style="top: 50%; left: 30%; animation-duration: 12s;"></div>
    <div class="floating-heart" style="top: 70%; left: 70%; animation-duration: 14s;"></div>
    <div class="floating-heart" style="top: 30%; left: 50%; animation-duration: 16s;"></div>
    <div class="floating-heart" style="top: 60%; left: 80%; animation-duration: 18s;"></div>
    <div class="floating-flower" style="top: 10%; left: 50%; animation-duration: 10s;"></div>
    <div class="floating-flower" style="top: 60%; left: 70%; animation-duration: 14s;"></div>
  </div>

  <div class="container" id="intro">
    <h1>Abre isso com carinho...</h1>
    <div class="open-btn">
      <button onclick="openHeart()">Abrir o coração de Gidelson</button>
    </div>
  </div>

  <div class="container" id="main-content">
    <p>Vic,</p>
    <p>Desde que você chegou, parece que a vida ficou com uma cor diferente. Como se tudo ficasse mais leve, mais bonito... mais cheio de sentido.</p>
    <p>Você tem um brilho que é só seu. Uma luz tão única que ilumina até os cantos mais escuros dos meus dias. É impossível não sorrir quando penso em você.</p>
    <p>Cada batida do meu coração sussurra o seu nome, como se ele soubesse desde sempre que foi feito pra te amar.</p>
    <p>Você é o meu pensamento favorito, o meu lugar seguro, minha calmaria no caos. É com você que eu quero dividir os silêncios, os sonhos, os medos e as vitórias.</p>
    <p>Quero te abraçar forte quando o mundo pesar, quero te lembrar todos os dias o quanto você é linda por dentro e por fora. Quero cuidar de você como quem cuida de algo raro e precioso — porque é isso que você é pra mim.</p>
    <p>Quero te fazer sorrir nos dias bons e te segurar firme nos dias difíceis. Quero ouvir suas inseguranças e transformá-las em carinho, te mostrar com gestos e palavras que você nunca está sozinha.</p>
    <p>Se eu pudesse, colocaria o mundo nas suas mãos... Mas como não posso, eu coloco o meu coração. Inteiro. Sem reservas.</p>
    <p>Porque eu te amo. E é muito.</p>
    <p class="final">Vic, você aceita namorar comigo?</p>
    <div class="buttons">
      <button onclick="showResponse()">Sim, eu aceito!</button>
      <button onclick="showResponse()">Claro, amor!</button>
    </div>
  </div>

  <div class="container" id="response">
    <img id="heart-gif" src="https://media.tenor.com/HU8f1uVWHTIAAAAi/hug-heart.gif" alt="Coração fofo animado">
    <div class="message-final">Meu coração tá transbordando de felicidade! Esse meu amor por você só me faz querer viver momentos lindos ao seu lado. 💖</div>
  </div>

  <audio id="bg-music" src="https://cdn.pixabay.com/download/audio/2023/01/05/audio_735dfb77d4.mp3" autoplay loop></audio>

  <script>
    window.onload = function() {
      document.getElementById("intro").style.display = "block";
      document.getElementById("main-content").style.display = "none";
      document.getElementById("response").style.display = "none";
    }

    function openHeart() {
      document.getElementById("intro").style.display = "none";
      document.getElementById("main-content").style.display = "block";
    }

    function showResponse() {
      document.getElementById("main-content").style.display = "none";
      document.getElementById("response").style.display = "block";
    }
  </script>
</body>
</html>
