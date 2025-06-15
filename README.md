<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Para vos, Vika</title>
  <link href="https://fonts.googleapis.com/css2?family=Pacifico&family=Quicksand:wght@400;600&display=swap" rel="stylesheet"/>
  <style>
    :root {
      --font-base: clamp(1rem, 2.5vw, 1.5rem);
      --font-title: clamp(2rem, 5vw, 3rem);
      --font-final: clamp(1.5rem, 4vw, 2rem);
    }

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

    .overlay-bg {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-color: rgba(255,255,255,0.7);
      z-index: 1;
      display: none;
    }

    .container {
      padding: 30px 20px;
      max-width: 700px;
      animation: fadeIn 1s ease;
      border-radius: 16px;
      margin-top: 40px;
      position: relative;
      z-index: 2;
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

    @juanntama floatHeart {
      from { transform: translateY(0); opacity: 1; }
      to { transform: translateY(-300px); opacity: 0; }
    }

    h1 {
      font-family: 'Pacifico', cursive;
      font-size: var(--font-title);
      color: #d6336c;
      margin-top: 100px;
      animation: bounce 1.5s infinite alternate;
    }

    p {
      font-size: var(--font-base);
      line-height: 1.7;
      margin-bottom: 20px;
      color: #000000;
    }

    .final {
      font-weight: bold;
      font-size: var(--font-final);
      margin-top: 30px;
    }

    .buttons {
      margin-top: 30px;
    }

    button {
      margin: 10px;
      padding: 12px 24px;
      font-size: var(--font-base);
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
      font-size: var(--font-final);
      color: #d63384;
      font-weight: bold;
      margin-top: 20px;
      animation: pulse 2s infinite ease-in-out;
      display: flex;
      justify-content: center;
      align-items: center;
      text-align: center;
      min-height: 200px;
      z-index: 12;
      text-shadow: 1px 1px 4px white;
      position: relative;
      opacity: 0;
      transition: opacity 4s ease-in-out;
      flex-direction: column;
    }

    .heart {
      position: absolute;
      font-size: 24px;
      color: red;
      animation: floatHeart 4s linear forwards;
    }

    #closing-message {
      display: none;
      opacity: 0;
      transition: opacity 3s ease-in-out;
      z-index: 12;
      text-align: center; /* Centraliza o texto */
      font-size: 2rem; /* Aumenta o tamanho da fonte */
    }

    #light-overlay {
      position: fixed;
      inset: 0;
      width: 100%;
      height: 100%;
      background: white;
      opacity: 0;
      pointer-events: none;
      transition: opacity 8s ease-in-out;
      z-index: 10;
    }

    @media (max-width: 600px) {
      h1 {
        font-size: 2rem;
      }

      .final {
        font-size: 1.5rem;
      }

      .message-final {
        font-size: 1.5rem;
      }
    }
  </style>
</head>
<body>
  <div class="overlay-bg" id="text-background"></div>

  <div class="container" id="intro">
    <h1>Abre esto con cariñoo...</h1>
    <div class="open-btn">
      <button onclick="openHeart()">Abrir el corazon de juan</button>
    </div>
  </div>

  <div class="container" id="main-content">
    <p>Vic,</p>
    <p>Desde que llegaste a mi . vida te ammo..</p>
    <p> panita te quier un monton cf.</p>
    <p> Te love you.</p>
    <p> mi pensa.meinto,favorito sos vos
    

    <p class="final">Vika, queres ser mi nobea >w< ?</p>
    <div class="buttons">
      <button onclick="showResponse()">Sim, eu aceito!</button>
      <button onclick="showResponse()">Claro, amor!</button>
    </div>
  </div>

  <div class="container" id="response">
    <div class="message-final">
      <span>Mi corazon te quiere we!</span>
      <span> ironía no es .</span>
    </div>
  </div>

  <div class="container" id="closing-message">
    <p>,</p>
    <p>✨💖</p>
  </div>

  <div id="light-overlay"></div>

  <audio id="bg-music" src="https://cdn.pixabay.com/download/audio/2023/01/05/audio_735dfb77d4.mp3" autoplay loop></audio>

  <script>
    function openHeart() {
      document.getElementById("intro").style.display = "none";
      document.getElementById("main-content").style.display = "block";
      document.getElementById("text-background").style.display = "block";
    }

    function showResponse() {
      document.getElementById("main-content").style.display = "none";
      document.getElementById("text-background").style.display = "none";
      document.getElementById("response").style.display = "block";
      createHearts();

      setTimeout(() => {
        document.getElementById("response").style.display = "none";
      }, 12000); // Aumentado para 12 segundos

      setTimeout(() => {
        document.getElementById("light-overlay").style.opacity = "1";
      }, 8000); // Aumentado para 8 segundos

      setTimeout(() => {
        document.getElementById("closing-message").style.display = "block";
        document.getElementById("closing-message").style.opacity = "1";
      }, 16000); // Aumentado para 16 segundos

      setTimeout(() => {
        window.close();
      }, 24000); // Aumentado para 24 segundos
    }

    function createHearts() {
      const heartInterval = setInterval(() => {
        const heart = document.createElement("div");
        heart.classList.add("heart");
        heart.style.left = Math.random() * 100 + "vw"; // Posição aleatória na largura
        heart.style.top = Math.random() * 100 + "vh"; // Posição aleatória na altura
        heart.textContent = "❤️";
        document.body.appendChild(heart);

        setTimeout(() => {
          heart.remove();
        }, 4000);
      }, 300);

      setTimeout(() => {
        clearInterval(heartInterval);
      }, 12000);
    }
  </script>
</body>
</html>
