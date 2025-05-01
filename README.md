<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Pra vc, Vic
body {
margin: 0;
padding: 0;
font-family: 'Quicksand', sans-serif;
background: url('https://example.com/background-image.png') no-repeat center center fixed; /* Altere para uma URL válida */
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
animation: fadeIn 1s ease;
background: rgba(255, 255, 255, 0.85);
border-radius: 16px;
margin-top: 40px;
}
@keyframes fadeIn {
from { opacity: 0; transform: translateY(20px); }
to { opacity: 1; transform: translateY(0); }
}
h1 {
font-family: 'Pacifico', cursive;
font-size: 32px;
color: #d6336c;
margin-top: 100px;
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
/* Corações flutuantes */
.heart {
position: fixed;
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
</style>
<div class="container" id="intro">
Abre isso com carinho...
<button onclick="openHeart()">Abrir o coração de Gidelson<div class="container" id="main-content">
Vic,
Desde q vc chegou, parece q a vida ficou com uma cor diferente. Como se tudo ficasse mais leve, mais bonito... mais cheio de sentido.
Vc tem um brilho q é só seu. Uma luz tão única q ilumina até os cantos mais escuros dos meus dias. É impossível não sorrir quando penso em vc.
Cada batida do meu coração sussurra o seu nome, como se ele soubesse desde sempre q foi feito pra te amar.
Vc é o meu pensamento favorito, o meu lugar seguro, minha calmaria no caos. É com vc q eu quero dividir os silêncios, os sonhos, os medos e as vitórias.
Quero te abraçar forte quando o mundo pesar, quero te lembrar todos os dias o quanto vc é linda por dentro e por fora. Quero cuidar de vc como quem cuida de algo raro e precioso — pq é isso q vc é pra mim.
Quero te fazer sorrir nos dias bons e te segurar firme nos dias difíceis. Quero ouvir suas inseguranças e transformá-las em carinho, te mostrar com gestos e palavras q vc nunca tá sozinha.
Se eu pudesse, colocaria o mundo nas suas mãos... Mas como não posso, eu coloco o meu coração. Inteiro. Sem reservas.
Pq eu te amo. E é muito.
Vic, vc aceita namorar comigo?
<button onclick="showResponse()">Sim, eu aceito!<button onclick="showResponse()">Claro, amor!
Meu coração tá transbordando de felicidade! Esse meu amor por vc só me faz querer viver momentos lindos ao seu lado.
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
