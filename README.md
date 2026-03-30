# Asad-s-wedding
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Asad & Sania Royal Wedding</title>

<!-- Fonts -->
<link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@400;700&family=Playfair+Display:wght@400;700&display=swap" rel="stylesheet">

<style>
* {margin:0; padding:0; box-sizing:border-box;}
body {
  font-family: 'Playfair Display', serif;
  background:#0d0d0d;
  color: gold;
  overflow-x:hidden;
}

header {
  position:relative;
  height:100vh;
  display:flex;
  flex-direction:column;
  justify-content:center;
  align-items:center;
  text-align:center;
  background: url('https://picsum.photos/1600/900?random=1') no-repeat center/cover;
}

header::before {
  content:'';
  position:absolute;
  top:0; left:0; right:0; bottom:0;
  background: rgba(0,0,0,0.6);
}

header h1, header p {
  position:relative;
  z-index:1;
  animation:fadeInDown 2s ease forwards;
}

header h1 {font-size:60px; letter-spacing:3px;}
header p {font-size:24px; margin-top:15px;}

@keyframes fadeInDown {
  0% {opacity:0; transform: translateY(-50px);}
  100% {opacity:1; transform: translateY(0);}
}

.section {
  padding:60px 20px;
  text-align:center;
}

.card {
  background:#111;
  margin:20px auto;
  padding:30px;
  border-radius:15px;
  width:300px;
  border:1px solid gold;
  box-shadow:0 0 20px rgba(255,215,0,0.2);
  transition:0.4s;
}

.card:hover {
  transform:scale(1.05);
  box-shadow:0 0 30px gold;
}

.countdown {
  font-size:32px;
  margin-top:20px;
}

.gallery {
  display:flex;
  justify-content:center;
  gap:15px;
  flex-wrap:wrap;
  margin-top:30px;
}

.gallery img {
  width:180px;
  border-radius:15px;
  border:2px solid gold;
  transition:0.3s;
}

.gallery img:hover {
  transform:scale(1.05);
  box-shadow:0 0 25px gold;
}

footer {
  padding:30px;
  font-size:16px;
  background:#111;
}
</style>
</head>

<body>

<!-- Background Music -->
<audio autoplay loop>
  <source src="https://www.computerhope.com/jargon/m/example.mp3" type="audio/mpeg">
</audio>

<header>
  <h1>Asad Zaman ❤️ Sania Raza</h1>
  <p>Royal Wedding Celebration 👑</p>
  <div class="countdown" id="countdown"></div>
</header>

<section class="section">
  <h2>Wedding Events</h2>

  <div class="card">
    <h3>💛 Mehndi</h3>
    <p>24th</p>
    <p>Bangash Farm House</p>
  </div>

  <div class="card">
    <h3>❤️ Baraat</h3>
    <p>25th</p>
    <p>Bangash Farm House</p>
  </div>

  <div class="card">
    <h3>🤍 Walima</h3>
    <p>26th</p>
    <p>Fortress Marquee</p>
  </div>
</section>

<section class="section">
  <h2>Our Royal Moments</h2>
  <div class="gallery">
    <img src="https://picsum.photos/300/400?random=2" alt="Couple AI 1">
    <img src="https://picsum.photos/300/400?random=3" alt="Couple AI 2">
    <img src="https://picsum.photos/300/400?random=4" alt="Couple AI 3">
  </div>
</section>

<footer>
  <p>We warmly invite you to celebrate with us 💫</p>
</footer>

<script>
// Countdown Timer (Mehndi)
var weddingDate = new Date("April 24, 2026 00:00:00").getTime();

var countdown = setInterval(function(){
  var now = new Date().getTime();
  var distance = weddingDate - now;

  var days = Math.floor(distance/(1000*60*60*24));
  var hours = Math.floor((distance % (1000*60*60*24))/(1000*60*60));
  var minutes = Math.floor((distance % (1000*60*60))/(1000*60));

  document.getElementById("countdown").innerHTML = days + "d " + hours + "h " + minutes + "m ";

  if(distance<0){
    clearInterval(countdown);
    document.getElementById("countdown").innerHTML = "The Wedding Has Started 🎉";
  }
}, 1000);
</script>

</body>
</html>
