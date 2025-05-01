<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Pra vc, Vic</title>
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
    }

    .container {
      padding: 30px 20px;
      max-width: 700px;
      opacity: 0;
      animation: fadeInText 1.5s ease-in-out forwards;
      animation-delay: 0.4s;
    }

    img {
      width: 180px;
      height: auto;
      border-radius: 20px;
      margin-bottom: 20px;
      box-shadow: 0 4px 15px rgba(0,0,0,0.2);
    }

    h1 {
      font-size: 26px;
      color: #d6336c;
      margin-top: 80px;
      margin-bottom: 20px;
      animation: fadeInText 1.2s ease-in-out forwards;
    }

    p {
      font-size: 18px;
      line-height: 1.7;
      margin-bottom: 20px;
    }

    .final {
      font-weight: bold;
      font-size: 20px;
      color: #b20043;
      margin-top: 30px;
    }

    .buttons, .open-btn {
      margin-top: 20px;
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

    .response {
      display: none;
      margin-top: 60px;
    }

    .final-message {
      font-size: 22px;
      font-weight: bold;
      color: #c2185b;
      margin-bottom: 30px;
      animation: fadeInText 1s ease-in-out forwards;
    }

    .heart-animated {
      display: none;
      margin: 0 auto;
      max-width: 180px;
      animation: fadeIn 1.2s ease-in-out forwards;
    }

    .heart-animated img {
      width: 100%;
    }

    @keyframes bounce {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-15px); }
    }

    @keyframes fadeIn {
      from { opacity: 0; }
      to { opacity: 1; }
    }

    @keyframes fadeInText {
      0% {
        opacity: 0;
        transform: translateY(20px);
      }
      100% {
        opacity: 1;
        transform: translateY(0);
      }
    }

    #main-content {
      display: none;
    }
  </style>
</head>
<body>
  <div class="container" id="intro" style="opacity: 1;">
    <h1 style="animation-delay: 0s;">Abre isso com carinho...</h1>
    <div class="open-btn">
      <button onclick="openHeart()">Abrir o coração de Gidelson</button>
    </div>
  </div>

  <div class="container" id="main-content">
    <img src="1000304699.png" alt="Vic">
    <p>Vic,</p>
    <p>Desde que você chegou, parece que a vida ficou com uma cor diferente. Como se tudo ficasse mais leve, mais bonito... mais cheio de sentido.</p>
    <p>Você tem um brilho que é só seu. Uma luz tão única que ilumina até os cantos mais escuros dos meus dias. É impossível não sorrir quando penso em você.</p>
    <p>Cada batida do meu coração sussurra o seu nome, como se ele soubesse desde sempre que foi feito pra te amar.</p>
    <p>Você é o meu pensamento favorito, o meu lugar seguro, minha calmaria no caos. É com você que eu quero dividir os silêncios, os sonhos, os medos e as vitórias.</p>
    <p>Quero te abraçar forte quando o mundo pesar, quero te lembrar todos os dias o quanto você é linda por dentro e por fora. Quero cuidar de você como quem cuida de algo raro e precioso — porque é isso que você é pra mim.</p>
    <p>Quero te fazer sorrir nos dias bons e te segurar firme nos dias difíceis. Quero ouvir suas inseguranças e transformá-las em carinho, te mostrar com gestos e palavras que você nunca tá sozinha.</p>
    <p>Se eu pudesse, colocaria o mundo nas suas mãos... Mas como não posso, eu coloco o meu coração. Inteiro. Sem reservas.</p>
    <p class="final">Vic, você aceita namorar comigo?</p>
    <div class="buttons">
      <button onclick="showResponse()">Sim, eu aceito!</button>
      <button onclick="showResponse()">Claro, amor!</button>
    </div>
    <div class="response" id="response">
      <div class="final-message">
        Meu coração tá transbordando de felicidade! Esse meu amor por vc só me faz querer viver momentos lindos ao seu lado 💖
      </div>
      <div class="heart-animated" id="heart">
        <img src="https://media.tenor.com/xu1Ldt6oWk0AAAAi/peach-goma-love.gif" alt="Coração fofo" />
      </div>
    </div>
    <audio id="bg-music" src="https://cdn.pixabay.com/download/audio/2023/01/05/audio_735dfb77d4.mp3" autoplay loop></audio>
  </div>

  <script>
    function openHeart() {
      document.getElementById("intro").style.display = "none";
      document.getElementById("main-content").style.display = "block";
    }

    function showResponse() {
      document.getElementById("response").style.display = "block";
      document.getElementById("heart").style.display = "block";
    }
  </script>
</body>
</html>
