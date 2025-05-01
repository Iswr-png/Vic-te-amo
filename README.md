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
    }
    img {
      width: 180px;
      height: auto;
      border-radius: 20px;
      margin-bottom: 20px;
      box-shadow: 0 4px 15px rgba(0,0,0,0.2);
    }
    h1 {
      font-size: 24px;
      color: #d6336c;
      margin-bottom: 20px;
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
    .buttons {
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
      margin-top: 30px;
      font-size: 20px;
      font-weight: bold;
      color: #c2185b;
      animation: fadeIn 1s ease-in-out;
    }
    .heart {
      display: inline-block;
      color: #ff4d6d;
      font-size: 40px;
      animation: pulse 1s infinite;
      margin-top: 10px;
    }
    @keyframes pulse {
      0% { transform: scale(1); }
      50% { transform: scale(1.2); }
      100% { transform: scale(1); }
    }
    @keyframes fadeIn {
      from { opacity: 0; }
      to { opacity: 1; }
    }
  </style>
</head>
<body>
  <div class="container">
    <img src="1000304699.png" alt="Vic">
    <h1>Abre isso com carinho...</h1>
    <p>Vic,</p>
    <p>Desde q vc chegou, parece q a vida ficou com uma cor diferente. Como se tudo ficasse mais leve, mais bonito... mais cheio de sentido.</p>
    <p>Vc tem um brilho q é só seu. Uma luz tão única q ilumina até os cantos mais escuros dos meus dias. É impossível não sorrir quando penso em vc.</p>
    <p>Cada batida do meu coração sussurra o seu nome, como se ele soubesse desde sempre q foi feito pra te amar.</p>
    <p>Vc é o meu pensamento favorito, o meu lugar seguro, minha calmaria no caos. É com vc q eu quero dividir os silências, os sonhos, os medos e as vitórias.</p>
    <p>Quero te abraçar forte quando o mundo pesar, quero te lembrar todos os dias o qto vc é linda por dentro e por fora. Quero cuidar de vc como quem cuida de algo raro e precioso — pq é isso q vc é pra mim.</p>
    <p>Quero te fazer sorrir nos dias bons e te segurar firme nos dias difíceis. Quero ouvir suas inseguranças e transformá-las em carinho, te mostrar com gestos e palavras q vc nunca tá sozinha.</p>
    <p>Se eu pudesse, colocaria o mundo nas suas mãos... Mas como não posso, eu coloco o meu coração. Inteiro. Sem reservas.</p>
    <p class="final">Vic, vc aceita namorar comigo?</p>
    <div class="buttons">
      <button onclick="showResponse()">Sim, eu aceito!</button>
      <button onclick="showResponse()">Claro, amor!</button>
    </div>
    <div class="response" id="response">
      Vc acabou de fazer meu coração dançar! <div class="heart">&#10084;</div>
    </div>
    <audio id="bg-music" src="https://cdn.pixabay.com/download/audio/2023/01/05/audio_735dfb77d4.mp3" autoplay loop></audio>
  </div>

  <script>
    function showResponse() {
      document.getElementById("response").style.display = "block";
    }
  </script>
</body>
</html>
