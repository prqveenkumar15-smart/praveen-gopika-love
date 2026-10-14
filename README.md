
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Praveen ❤️ Gopika</title>
<style>
*{box-sizing:border-box}
body{
  margin:0;font-family:Arial,sans-serif;text-align:center;
  color:#8b174b;
  background:linear-gradient(135deg,#ffe0ec,#fff0f5,#ffc4da);
  min-height:100vh;
}
header{padding:65px 15px 35px}
h1{font-size:clamp(32px,8vw,52px);margin:10px}
p{line-height:1.8}
button{
  border:0;border-radius:30px;padding:14px 22px;
  background:#ed4c89;color:white;font-size:16px;
  cursor:pointer;margin:10px;
}
section{padding:25px 15px}
.gallery{
  display:grid;grid-template-columns:repeat(2,minmax(0,1fr));
  gap:12px;max-width:700px;margin:auto;
}
.gallery img{
  width:100%;height:220px;object-fit:cover;
  border-radius:18px;border:3px solid white;
  background:#ffc4da;cursor:pointer;
}
.note{
  max-width:600px;margin:20px auto;padding:25px;
  background:#ffffffbb;border-radius:20px;
  box-shadow:0 5px 20px #d65b8b30;
}
#letter{display:none}
#viewer{
  display:none;position:fixed;inset:0;background:#000e;
  z-index:10;align-items:center;justify-content:center;
  padding:20px;
}
#viewer img{max-width:95%;max-height:80vh;border-radius:15px}
.heart{position:fixed;bottom:-30px;animation:float 7s linear infinite;
pointer-events:none;z-index:2}
@keyframes float{
  to{transform:translateY(-110vh) rotate(25deg);opacity:0}
}
footer{padding:30px}
@media(max-width:420px){
 .gallery img{height:160px}
}
</style>
</head>
<body>

<header>
  <div style="font-size:55px">💖</div>
  <h1>Praveen ❤️ Gopika</h1>
  <p>Two hearts, one beautiful love story ✨</p>
  <p>Every moment with you is special, Gopika! 🥹💕</p>
  <button onclick="showLetter()">Open My Love Letter 💌</button>
</header>

<section>
  <h2>Our Memories 📸</h2>
  <p>Every picture holds a little piece of our love ❤️</p>

  <div class="gallery">
    <img src="photos/photo1.jpg" alt="Our memory 1" onclick="zoom(this)">
    <img src="photos/photo2.jpg" alt="Our memory 2" onclick="zoom(this)">
    <img src="photos/photo3.jpg" alt="Our memory 3" onclick="zoom(this)">
    <img src="photos/photo4.jpg" alt="Our memory 4" onclick="zoom(this)">
    <img src="photos/photo5.jpg" alt="Our memory 5" onclick="zoom(this)">
    <img src="photos/photo6.jpg" alt="Our memory 6" onclick="zoom(this)">
  </div>
</section>

<section id="letter" class="note">
  <h2>My Dear Gopika 💗</h2>
  <p>
    Nee en life-la vandhadhukku romba thanks, chellam. ❤️<br>
    Un smile enakku happiness; un love enakku strength.<br>
    Namma rendu perum eppovum sandhoshama irukkanum.<br>
    Un kooda innum neraya beautiful memories create pannanum.<br>
    I love you so much, Gopika! 🫶💋
  </p>
  <h3>Forever Yours, Praveen ❤️</h3>
  <button onclick="hideLetter()">Close 💕</button>
</section>

<div id="viewer" onclick="this.style.display='none'">
  <img id="bigPhoto" alt="Our photo">
</div>

<footer>
  <h3>Made with ❤️ by Praveen</h3>
  <p>One love. Two hearts. Forever. ♾️</p>
</footer>

<script>
function showLetter(){
  document.getElementById('letter').style.display='block';
  document.getElementById('letter').scrollIntoView({behavior:'smooth'});
}
function hideLetter(){
  document.getElementById('letter').style.display='none';
}
function zoom(photo){
  document.getElementById('bigPhoto').src=photo.src;
  document.getElementById('viewer').style.display='flex';
}
setInterval(()=>{
  const h=document.createElement('div');
  h.className='heart';
  h.textContent=['❤️','💕','💗','💖'][Math.floor(Math.random()*4)];
  h.style.left=Math.random()*100+'vw';
  h.style.fontSize=(18+Math.random()*25)+'px';
  document.body.appendChild(h);
  setTimeout(()=>h.remove(),7000);
},600);
</script>

</body>
</html>
