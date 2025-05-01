<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Pra você, Vic</title>
  <link href="https://fonts.googleapis.com/css2?family=Pacifico&family=Quicksand:wght@400;600&display=swap" rel="stylesheet">
  <style>
    body {
      margin: 0;
      padding: 0;
      font-family: 'Quicksand', sans-serif;
      background: url('https://chat.openai.com/mnt/data/1000304699.png') no-repeat center center fixed;
      background-size: cover;
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
      background: rgba(255, 255, 255, 0.85);
      border-radius: 16px;
      margin-top: 40px;
    }

    h1 {
      font-family: 'Pacifico', cursive;
      font-size: 32px;
      color: #d6336c;
      margin-top: 50px;
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
      transition: background-color 0.3s;
    }

    button:hover {
      background-color: #ff77a9;
    }

    .heart {
      position: absolute;
      width: 20px;
      height: 20px;
      background: url('https://i.imgur.com/ZpUj36F.png') no-repeat center;
      background-size: contain;
      animation: float 6s linear infinite;
      pointer-events: none;
    }

    @keyframes float {
      0% { transform: translateY(100vh) scale(0.5); opacity: 0; }
      50% { opacity: 1; }
      100% { transform: translateY(-10vh) scale(1); opacity: 0; }
    }

    #heart-gif {
      width: 120px;
      margin: 30px auto 0;
      display: none; /* Escondido inicialmente */
    }

    #response {
      display: none;
    }

    .message-final {
      font-size: 24px;
      color: #d6336c;
      font-weight: bold;
      margin-top: 20px;
    }
  </style>
</head>
<body>
  <div class="container" id="intro">
    <h1>Abre isso com carinho...</h1>
    <button onclick="openHeart()">Abrir o coração de Gidelson</button>
  </div>

  <div class="container" id="main-content" style="display: none;">
    <p>Vic,</p>
    <p>Desde que você chegou, parece que a vida ficou com uma cor diferente. Como se tudo ficasse mais leve, mais bonito... mais cheio de sentido.</p>
    <p>Você tem um brilho que é só seu. Uma luz tão única que ilumina até os cantos mais escuros dos meus dias. É impossível não sorrir quando penso em você.</p>
    <p>Cada batida do meu coração sussurra o seu nome, como se ele soubesse desde sempre que foi feito pra te amar.</p>
    <p>Você é o meu pensamento favorito, o meu lugar seguro, minha calmaria no caos. É com você que eu quero dividir os silêncios, os sonhos, os medos e as vitórias.</p>
    <p>Quero te abraçar forte quando o mundo pesar, quero te lembrar todos os dias o quanto você é linda por dentro e por fora.</p>
    <p>Quero cuidar de você como quem cuida de algo raro e precioso — porque é isso que você é pra mim.</p>
    <p>Se eu pudesse, colocaria o mundo nas suas mãos... Mas como não posso, eu coloco o meu coração. Inteiro. Sem reservas.</p>
    <p>Porque eu te amo. E é muito.</p>
    <p class="final">Vic, você aceita namorar comigo?</p>
    <div class="buttons">
      <button onclick="showResponse()">Sim, eu aceito!</button>
      <button onclick="showResponse()">Claro, amor!</button>
    </div>
  </div>

  <div class="container" id="response">
    <img id="heart-gif" src="https://i.imgur.com/j5kV1pG.gif" alt="Coração fofo animado">
    <div class="message-final">Meu coração tá transbordando de felicidade! Esse meu amor por você só me faz querer viver momentos lindos ao seu lado.</div>
  </div>

  <audio id="bg-music" src="https://cdn.pixabay.com/download/audio/2023/01/05/audio_735dfb77d4.mp3" autoplay loop></audio>

  <script>
    window.onload = function() {
      document.getElementById("intro").style.display = "block";
    }

    function openHeart() {
      document.getElementById("intro").style.display = "none";
      document.getElementById("main-content").style.display = "block";

      // Criar corações flutuantes
      for (let i = 0; i < 20; i++) {
        let heart = document.createElement("div");
        heart.className = "heart";
        heart.style.left = Math.random() * 100 + "vw";
        heart.style.animationDuration = (Math.random() * 3 + 4) + "s"; // Duração aleatória
        heart.style.animationDelay = (Math.random() * 3) + "s"; // Atraso aleatório
        document.body.appendChild(heart);

        // Remover o coração após 10 segundos
        setTimeout(() => heart.remove(), 10000);
      }
    }

    function showResponse() {
      document.getElementById("main-content").style.display = "none";
      document.getElementById("response").style.display = "block";
      document.getElementById("heart-gif").style.display = "block"; // Exibe o gif do coração
    }
  </script>
</body>
</html>
