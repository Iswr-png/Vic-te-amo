<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Pra você, Vic</title>
  <link href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@600&family=Segoe+UI&display=swap" rel="stylesheet">
  <style>
    body {
      margin: 0;
      padding: 0;
      font-family: 'Segoe UI', sans-serif;
      background: url('1000304699.png') no-repeat center center fixed;
      background-size: cover;
      color: #4a2c2a;
      display: flex;
      flex-direction: column;
      align-items: center;
      text-align: center;
      overflow-x: hidden;
      position: relative;
    }

    .overlay {
      position: absolute;
      inset: 0;
      background: rgba(255, 255, 255, 0.6);
      backdrop-filter: blur(5px);
      z-index: 0;
    }

    .container {
      padding: 30px 20px;
      max-width: 700px;
      animation: fadeIn 1s ease;
      z-index: 1;
      position: relative;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }

    h1 {
      font-size: 34px;
      color: #d6336c;
      margin-top: 100px;
      font-family: 'Dancing Script', cursive;
      animation: bounce 1.5s infinite alternate;
    }

    @keyframes bounce {
      from { transform: translateY(0); }
      to { transform: translateY(-10px); }
    }

    p {
      font-size: 18px;
      line-height: 1.7;
      margin-bottom: 20px;
    }

    .final {
      font-weight: bold;
      font-size: 22px;
      color: #b20043;
      margin-top: 30px;
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
      width: 150px;
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

    /* Corações e flores flutuantes */
    .floating {
      position: fixed;
      width: 30px;
      height: 30px;
      background-size: contain;
      animation: floatUp 6s linear infinite;
      z-index: 0;
    }

    @keyframes floatUp {
      0% { transform: translateY(100vh); opacity: 1; }
      100% { transform: translateY(-10vh); opacity: 0; }
    }
  </style>
</head>
<body>
  <div class="overlay"></div>

  <!-- Corações e flores flutuando -->
  <script>
    const elements = 20;
    const images = [
      "https://i.imgur.com/wO0YQfT.png", // Coração
      "https://i.imgur.com/5LVf3gQ.png"  // Flor
    ];

    for (let i = 0; i < elements; i++) {
      const item = document.createElement("div");
      item.classList.add("floating");
      item.style.left = Math.random() * 100 + "vw";
      item.style.animationDelay = Math.random() * 5 + "s";
      item.style.width = "30px";
      item.style.height = "30px";
      item.style.backgroundImage = `url('${images[Math.floor(Math.random() * images.length)]}')`;
      document.body.appendChild(item);
    }
  </script>

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
    <p>Você é o meu pensamento favorito, o meu lugar seguro, minha paz e minha alegria.</p>
    <p>Quero te abraçar forte quando o mundo pesar, quero te lembrar todos os dias o quanto você é linda por dentro e por fora.</p>
    <p>Porque eu te amo. E é muito.</p>
    <p class="final">Vic, você aceita namorar comigo?</p>
    <div class="buttons">
      <button onclick="showResponse()">Sim, eu aceito!</button>
      <button onclick="showResponse()">Claro, amor!</button>
    </div>
  </div>

  <div class="container" id="response">
    <img id="heart-gif" src="https://i.imgur.com/hQIw3dJ.gif" alt="Coração fofo animado">
    <div class="message-final">Meu coração tá transbordando de felicidade! 💖</div>
  </div>

  <audio id="bg-music" src="https://cdn.pixabay.com/download/audio/2023/01/05/audio_735dfb77d4.mp3" autoplay loop></audio>

  <script>
    window.onload = function() {
      document.getElementById("intro").style.display = "block";
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
