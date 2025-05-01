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
      font-family: 'Comic Sans MS', cursive, sans-serif;
      background: linear-gradient(to bottom, #ffccdd, #ffe6f2);
      color: #d6336c;
      display: flex;
      flex-direction: column;
      align-items: center;
      text-align: center;
      overflow-x: hidden;
    }
    .container {
      padding: 30px 20px;
      max-width: 700px;
    }
    h1 {
      font-size: 30px;
      color: #e60073;
      margin-top: 100px;
      animation: fadeIn 2s ease-in-out;
    }
    .open-btn button {
      margin-top: 30px;
      padding: 15px 30px;
      font-size: 18px;
      background-color: #ff99bb;
      border: none;
      border-radius: 15px;
      color: white;
      cursor: pointer;
      transition: 0.3s;
      box-shadow: 0 0 15px rgba(255, 105, 180, 0.5);
    }
    .open-btn button:hover {
      background-color: #ff77a9;
    }
    .text {
      animation: textEntrance 2s ease forwards;
      opacity: 0;
    }
    .text p {
      font-size: 20px;
      line-height: 1.8;
      margin-bottom: 20px;
    }
    .final {
      font-weight: bold;
      font-size: 24px;
      color: #b20043;
      margin-top: 30px;
    }
    .buttons button {
      margin: 10px;
      padding: 14px 28px;
      font-size: 18px;
      background-color: #ff85b3;
      border: none;
      border-radius: 12px;
      color: white;
      cursor: pointer;
      transition: 0.3s;
    }
    .buttons button:hover {
      background-color: #ff5c97;
    }
    .response-container {
      display: none;
      margin-top: 50px;
      animation: fadeIn 2s ease-in-out;
    }
    .mensagem {
      font-size: 26px;
      font-weight: bold;
      background: rgba(255, 255, 255, 0.9);
      padding: 20px;
      border-radius: 20px;
      box-shadow: 0 0 20px rgba(255, 105, 180, 0.5);
      animation: brilho 2s infinite alternate;
      margin-bottom: 20px;
    }
    .heart-gif img {
      width: 200px;
      height: auto;
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
    @keyframes textEntrance {
      0% {
        opacity: 0;
        transform: translateY(30px);
      }
      100% {
        opacity: 1;
        transform: translateY(0);
      }
    }
    @keyframes fadeIn {
      from { opacity: 0; }
      to { opacity: 1; }
    }
    @keyframes brilho {
      from { box-shadow: 0 0 15px rgba(255, 105, 180, 0.5); }
      to { box-shadow: 0 0 25px rgba(255, 105, 180, 0.8); }
    }
    @keyframes flutuar {
      from { transform: translateY(0); }
      to { transform: translateY(-20px); }
    }
    #main-content {
      display: none;
    }
  </style>
</head>
<body>
  <div class="decoracao">
    <div class="coracao" style="top: 10%; left: 20%;">💖</div>
    <div class="coracao" style="top: 50%; left: 60%;">❤️</div>
  </div>

  <div class="container" id="intro">
    <h1>Abre isso com carinho...</h1>
    <div class="open-btn">
      <button onclick="openHeart()">Abrir o coração de Gidelson</button>
    </div>
  </div>

  <div class="container" id="main-content">
    <div class="text">
      <p>Vic,</p>
      <p>Desde que você chegou, parece que a vida ficou com uma cor diferente. Tudo ficou mais leve, mais bonito, mais cheio de sentido.</p>
      <p>Você tem um brilho que é só seu. Uma luz tão única que ilumina até os cantos mais escuros dos meus dias. É impossível não sorrir quando penso em você.</p>
      <p>Cada batida do meu coração sussurra seu nome, como se ele soubesse desde sempre que foi feito pra te amar.</p>
      <p>Você é meu pensamento favorito, meu lugar seguro, minha calmaria no caos. É com você que eu quero dividir os silêncios, os sonhos, os medos e as vitórias.</p>
      <p>Quero te abraçar forte quando o mundo pesar, te lembrar todos os dias o quanto você é linda por dentro e por fora. Quero cuidar de você como quem cuida de algo raro e precioso — porque é isso que você é pra mim.</p>
      <p>Quero te fazer sorrir nos dias bons e te segurar firme nos dias difíceis. Quero ouvir suas inseguranças e transformá-las em carinho, te mostrar com gestos e palavras que você nunca tá sozinha.</p>
      <p>Se eu pudesse, colocaria o mundo nas suas mãos... Mas como não posso, coloco o meu coração. Inteiro. Sem reservas.</p>
      <p class="final">Vic, você aceita namorar comigo?</p>
    </div>

    <div class="buttons">
      <button onclick="showResponse()">Sim, eu aceito!</button>
      <button onclick="showResponse()">Claro, amor!</button>
    </div>
  </div>

  <div class="response-container" id="response">
    <div class="mensagem">
      💖 Meu coração está explodindo de felicidade! Esse amor só me faz querer viver momentos inesquecíveis ao seu lado! 💖
    </div>
    <div class="heart-gif">
      <img src="https://media.tenor.com/IcF3TqRt_yUAAAAi/love-you-hearts.gif" alt="Coração animado fofo">
    </div>
  </div>

  <script>
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
