# praveen-gopika-love
A special love website for Gopika ❤️

<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Praveen ❤️ Gopika</title>
<style>
* { box-sizing: border-box; }
body {
  margin: 0;
  min-height: 100vh;
  font-family: Georgia, serif;
  color: white;
  text-align: center;
  background: linear-gradient(145deg, #240013, #8b174b, #ed789f);
  overflow-x: hidden;
}
main {
  padding: 65px 20px 40px;
  max-width: 650px;
  margin: auto;
}
.heart {
  font-size: 65px;
  animation: beat 1s infinite;
}
h1 {
  font-size: clamp(32px, 8vw, 52px);
  margin: 15px 0;
}
p {
  font-size: 18px;
  line-height: 1.8;
}
.card {
  margin-top: 28px;
  padding: 25px;
  border: 1px solid #ffffff66;
  border-radius: 24px;
  background: #ffffff18;
  box-shadow: 0 10px 35px #21000c55;
  backdrop-filter: blur(8px);
}
button {
  border: none;
  border-radius: 30px;
  padding: 15px 25px;
  margin-top: 18px;
  background: #fff0f5;
  color: #9d174d;
  font-size: 16px;
  font-weight: bold;
  cursor: pointer;
}
#message {
  display: none;
  white-space: pre-line;
  margin-top: 22px;
}
.floating {
  position: fixed;
  bottom: -30px;
  animation: floatUp 7s linear forwards;
  pointer-events: none;
}
@keyframes beat {
  50% { transform: scale(1.15); }
}
@keyframes floatUp {
  to { transform: translateY(-110vh) rotate(25deg); opacity: 0; }
}
footer {
  margin-top: 45px;
  font-size: 14px;
}
</style>
</head>
<body>
<main>
  <div class="heart">❤️</div>
  <h1>Praveen & Gopika</h1>
  <p>Two hearts, one beautiful story. 💕</p>

  <section class="card">
    <h2>En Uyir Gopika ❤️</h2>
    <p>
      Nee en life-la vandha azhagana gift.
      Un smile en happiness, un love en strength.
      Ovvoru naalum un kooda beautiful memories
      create pannanum nu aasai
      love u dii my dear pondatii😘.
    </p>
    <p>🌹 Forever begins with you 🌹</p>
    <button onclick="showLove()">
      Open My Love Letter 💌
    </button>
    <div id="message">
      Ennavale Gopika ❤️

      Enakku kidaicha azhagana varam nee.
      Un kooda sirikkanum, un kooda vazhanum,
      epvayum life full ha ona irrupom
      enakaga Neeyum unakaga nanum
      

      I love you dii gundathii! 💖

      Forever yours,
      Praveen ❤️
    </div>
  </section>

  <footer>
    Made with ❤️ by Praveen, just for Gopika
  </footer>
</main>

<script>
function showLove() {
  const msg = document.getElementById("message");
  msg.style.display = "block";
  msg.scrollIntoView({ behavior: "smooth", block: "center" });
}
function createHeart() {
  const h = document.createElement("span");
  h.className = "floating";
  h.textContent = ["❤️", "💕", "💗", "💖"][Math.floor(Math.random()*4)];
  h.style.left = Math.random() * 100 + "vw";
  h.style.fontSize = (16 + Math.random() * 22) + "px";
  h.style.animationDuration = (5 + Math.random() * 4) + "s";
  document.body.appendChild(h);
  setTimeout(() => h.remove(), 9000);
}
setInterval(createHeart, 600);
</script>
</body>
</html>
