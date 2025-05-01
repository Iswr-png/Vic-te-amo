<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Para Vic</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(135deg, #ffe0ec, #ffe6f2);
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      overflow: hidden;
    }
    .container {
      text-align: center;
      max-width: 90%;
      padding: 2rem;
      background: white;
      border-radius: 20px;
      box-shadow: 0 0 20px rgba(0,0,0,0.1);
      animation: fadeIn 1s ease-in-out;
    }
    .hidden {
      display: none;
    }
    h1, p {
      color: #ff4081;
    }
    button {
      background-color: #ff4081;
      border: none;
      color: white;
      padding: 1rem 2rem;
      margin-top: 1rem;
      font-size: 1rem;
      border-radius: 10px;
      cursor: pointer;
    }
    button:hover {
      background-color: #e91e63;
    }
    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }
  </style>
</head>
<body>
  <div class="container" id="screen1">
    <h1>Clique para descobrir o que meu coração quer te dizer...</h1>
    <button onclick="nextScreen(1)">Começar</button>
  </div>

  <div class="container hidden" id="screen2">
    <p>Vic, você ilumina meus dias com o brilho único que só você tem...</p>
    <button onclick="nextScreen(2)">Próximo</button>
  </div>

  <div class="container hidden" id="screen3">
    <p>Meu coração chama seu nome a cada batida...</p>
    <button onclick="nextScreen(3)">Próximo</button>
  </div>

  <div class="container hidden" id="screen4">
    <p>Você é tudo pra mim, e eu queria ser tudo pra você.</p>
    <button onclick="nextScreen(4)">Próximo</button>
  </div>

  <div class="container hidden" id="screen5">
    <p>Quero estar com você e cuidar de cada medo e insegurança...</p>
    <button onclick="nextScreen(5)">Próximo</button>
  </div>

  <div class="container hidden" id="screen6">
    <p>Quero te dar carinho e te fazer sentir a pessoa mais especial e única do mundo. Porque é assim que você é pra mim.</p>
    <button onclick="nextScreen(6)">Próximo</button>
  </div>

  <div class="container hidden" id="screen7">
    <h1>Vic, você quer namorar comigo?</h1>
    <button onclick="resposta('Sim')">Sim</button>
    <button onclick="resposta('Claro que sim')">Claro que sim</button>
  </div>

  <div class="container hidden" id="screen8">
    <h1>Meu coração é todo seu!</h1>
    <p>Prepare-se pra ser a pessoa mais amada do universo.</p>
  </div>

  <script>
    function nextScreen(current) {
      document.getElementById(`screen${current}`).classList.add('hidden');
      document.getElementById(`screen${current + 1}`).classList.remove('hidden');
    }
    function resposta(opcao) {
      document.getElementById('screen7').classList.add('hidden');
      document.getElementById('screen8').classList.remove('hidden');
    }
  </script>
</body>
</html>

