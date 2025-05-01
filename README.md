<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Pra vc, Vic</title>
  <link href="https://fonts.googleapis.com/css2?family=Quicksand:wght@300;500&family=Sacramento&display=swap" rel="stylesheet">
  <style>
    body {
      margin: 0;
      padding: 0;
      font-family: 'Quicksand', sans-serif;
      background: linear-gradient(to bottom, #ffe6f0, #ffe0e9);
      color: #4a2c2a;
      display: flex;
      flex-direction: column;
      align-items: center;
      text-align: center;
      height: 100vh;
      justify-content: center;
    }
    .container {
      padding: 30px 20px;
      max-width: 700px;
      text-align: center;
    }
    img {
      width: 180px;
      height: auto;
      border-radius: 50%;
      margin-bottom: 20px;
      box-shadow: 0 4px 15px rgba(0,0,0,0.2);
    }
    h1 {
      font-size: 36px;
      font-family: 'Sacramento', cursive;
      color: #d6336c;
      margin-top: 50px;
      animation: fadeInText 2s ease-in-out;
    }
    p {
      font-size: 20px;
      line-height: 1.7;
      margin-bottom: 20px;
      animation: fadeInText 2s ease-in-out;
      font-family: 'Quicksand', sans-serif;
    }
    .final {
      font-weight: bold;
      font-size: 22px;
      color: #b20043;
      margin-top: 30px;
      animation: fadeInText 2s ease-in-out;
      font-family: 'Quicksand', sans-serif;
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
      border-radius: 50px;
      color: white;
      cursor: pointer;
      transition: 0.3s;
      font-family: 'Quicksand', sans-serif;
    }
    button:hover {
      background-color: #ff77a9;
    }
    .response {
      display: none;
      margin-top: 30px;
      font-size: 20px;
      font-weight: bold;
      color: #c2185b;
      animation: fadeIn 1s ease-in-out;
    }
    .heart-animated {
      display: none;
      width: 80px;
      height: 80px;
      background: red;
      position: relative;
      animation: bounce 2s infinite, kiss 2s 1, hug 2s infinite;
      transform-origin: center;
      border-radius: 50%;
      margin: 20px auto 0;
    }
    .heart-animated::before, .heart-animated::after {
      content: "";
      position: absolute;
      top: 0;
      width: 50px;
      height: 80px;
      background: red;
      border-radius: 50%;
    }
    .heart-animated::before {
      left: 50px;
      transform: rotate(-45deg);
      transform-origin: bottom right;
    }
    .heart-animated::after {
      left: 0;
      transform: rotate(45deg);
      transform-origin: bottom left;
    }
    @keyframes bounce {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-15px); }
    }
    @keyframes kiss {
      0% { transform: scale(1); }
      50% { transform: scale(1.1); }
      100% { transform: scale(1); }
    }
    @keyframes hug {
      0%, 100% { transform: scale(1); }
      50% { transform: scale(1.2); }
    }
    @keyframes fadeIn {
      from { opacity: 0; }
      to { opacity: 1; }
    }
    @keyframes fadeInText {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }
    #main-content {
      display: none;
    }
    #intro {
      background: rgba(255, 255, 255, 0.8);
      padding: 50px;
      border-radius: 15px;
      box-shadow: 0 0 20px rgba(0, 0, 0, 0.3);
      animation: fadeIn 2s ease-in-out;
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
    <img src="1000304699.png" alt="Vic">
    <p>Vic,</p>
    <p>Desde que você chegou, minha vida ganhou novas cores. Tudo ficou mais leve, mais bonito... mais cheio de amor e significado. Você tem uma luz que ilumina até os cantos mais escuros dos meus dias. Cada vez que penso em você, um sorriso espontâneo surge em meu rosto.</p>
    <p>Cada batida do meu coração sussurra seu nome, como se ele soubesse, desde sempre, que foi feito para te amar. Você é o meu pensamento favorito, meu lugar seguro, minha calmaria no caos. Eu quero dividir com você todos os momentos da minha vida, os sonhos, os medos, as vitórias e os silêncios.</p>
    <p>Eu te amo mais do que palavras podem expressar. Quero estar ao seu lado, abraçando você nos dias difíceis, te fazendo sorrir nos dias bons e cuidando de você com todo o meu carinho e amor. Quero te lembrar todos os dias do quanto você é linda, tanto por dentro quanto por fora.</p>
    <p>Se eu pudesse, colocaria o mundo inteiro em suas mãos, mas como não posso, te dou o meu coração. Inteiro. Sem reservas. Porque você é tudo para mim, Vic.</p>
    <p class="final">Vic, você aceita namorar comigo? 💖</p>
    <div class="buttons">
      <button onclick="showResponse()">Sim, eu aceito!</button>
      <button onclick="showResponse()">Claro, amor!</button>
    </div>
    <div class="response" id="response">
      Meu coração está transbordando de felicidade! Esse meu amor por você só me faz querer viver momentos lindos ao seu lado. ❤️
      <div class="heart-animated" id="heart"></div>
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
