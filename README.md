<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Pra vc, Vic</title>
  <link href="https://fonts.googleapis.com/css2?family=Pacifico&family=Quicksand:wght@400;600&display=swap" rel="stylesheet"/>
  <style>
    body {
      margin: 0;
      padding: 0;
      font-family: 'Quicksand', sans-serif;
      background: url('https://i.postimg.cc/02yn4XPg/Selfie-no-estilo-unic-rnio.png') no-repeat center center fixed;
      background-size: cover;
      color: #000000;
      display: flex;
      flex-direction: column;
      align-items: center;
      text-align: center;
      overflow-x: hidden;
      position: relative;
      transition: background-color 5s ease-in-out;
    }

    .container {
      padding: 30px 20px;
      max-width: 700px;
      animation: fadeIn 1s ease;
      border-radius: 16px;
      margin-top: 40px;
    }

    #main-content, #response, #closing-message {
      display: none;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }

    @keyframes pulse {
      0% { transform: scale(1); opacity: 1; }
      50% { transform: scale(1.1); opacity: 0.8; }
      100% { transform: scale(1); opacity: 1; }
    }

    @keyframes floatHeart {
      from { transform: translateY(0); opacity: 1; }
      to { transform: translateY(-300px); opacity: 0; }
    }

    h1 {
      font-family: 'Pacifico', cursive;
      font-size: 32px;
      color: #d6336c;
      margin-top: 100px;
      animation: bounce 1.5s infinite alternate;
    }

    p {
      font-size: 18px;
      line-height: 1.7;
      margin-bottom: 20px;
    }

    .final {
      font-weight: bold;
      font-size: 22px;
      margin-top: 30px;
    }

    .buttons {
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

    .message-final {
      font-size: 24px;
      color: #000000;
      font-weight: bold;
      margin-top: 20px;
      animation: pulse 1.5s infinite ease-in-out;
    }

    .heart {
      position: absolute;
      font-size: 24px;
      color: red;
      animation: floatHeart 4s linear infinite;
    }

    #closing-message {
      font-size: 24px;
      color: #ffffff;
      font-weight: bold;
      margin-top: 20px;
      opacity: 0;
      transition: opacity 3s ease-in-out;
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
    <p>Desde q vc chegou, parece q a vida ficou com uma cor diferente. Como se tudo ficasse mais leve, mais bonito... mais cheio de sentido.</p>
    <p>Vc tem um brilho q é só seu. Uma luz tão única q ilumina até os cantos mais escuros dos meus dias. É impossível não sorrir quando penso em vc.</p>
    <p>Cada batida do meu coração sussurra o seu nome, como se ele soubesse desde sempre q foi feito pra te amar.</p>
    <p>Vc é o meu pensamento favorito, o meu lugar seguro, minha calmaria no caos. É com vc q eu quero compartilhar momentos, os medos e as vitórias.</p>
    <p>Se eu pudesse, colocaria o mundo nas suas mãos... Mas como não posso, eu coloco o meu coração.</p>

    <p class="final">Vic, vc aceita namorar comigo?</p>
    <div class="buttons">
      <button onclick="showResponse()">Sim, eu aceito!</button>
      <button onclick="showResponse()">Claro, amor!</button>
    </div>
  </div>

  <div class="container" id="response">
    <div class="message-final">Meu coração tá transbordando de felicidade! Esse meu amor por vc só me faz querer viver momentos lindos ao seu lado. 💖</div>
  </div>

  <div class="container" id="closing-message">
    <p>A mágica do pedido chegou ao fim, mas nossa história mágica acaba de começar. ✨💖</p>
  </div>

  <audio id="bg-music" src="https://cdn.pixabay.com/download/audio/2023/01/05/audio_735dfb77d4.mp3" autoplay loop></audio>

  <script>
    function openHeart() {
      document.getElementById("intro").style.display = "none";
      document.getElementById("main-content").style.display = "block";
    }

    function showResponse() {
      document.getElementById("main-content").style.display = "none";
      document.getElementById("response").style.display = "block";
      createHearts();
      setTimeout(showClosingMessage, 10000);
    }

    function createHearts() {
      const interval = setInterval(() => {
        let heart = document.createElement("div");
        heart.classList.add("heart");
        heart.innerHTML = "❤️";
        heart.style.left = Math.random() * window.innerWidth + "px";
        heart.style.top = window.innerHeight + "px";
        heart.style.animationDuration = (Math.random() * 2 + 3) + "s";
        document.body.appendChild(heart);
        setTimeout(() => heart.remove(), 5000);
      }, 300);

      setTimeout(() => clearInterval(interval), 10000);
    }

    function showClosingMessage() {
      document.getElementById("response").style.display = "none";
      document.body.style.backgroundColor = "#000000";
      const message = document.getElementById("closing-message");
      message.style.display = "block";
      setTimeout(() => {
        message.style.opacity = "1";
      }, 500);
      setTimeout(() => {
        window.close();
      }, 10000);
    }
  </script>
</body>
</html>
