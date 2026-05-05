<!DOCTYPE html>
<html>
<head>
<title>Happy Birthday SAIQA 💖</title>

<style>
body {
  text-align: center;
  background: black;
  color: white;
  font-family: Arial;
  overflow: hidden;
}

h1 {
  font-size: 45px;
  margin-top: 50px;
  animation: glow 2s infinite alternate;
}

@keyframes glow {
  from { text-shadow: 0 0 10px pink; }
  to { text-shadow: 0 0 30px red; }
}

button {
  padding: 15px;
  margin: 10px;
  border-radius: 10px;
  border: none;
  cursor: pointer;
}

.balloon {
  width: 50px;
  height: 70px;
  border-radius: 50%;
  position: absolute;
  animation: float 6s infinite;
}

@keyframes float {
  from { bottom: -100px; }
  to { bottom: 100%; }
}

.heart {
  position: absolute;
  font-size: 20px;
  animation: fall 5s linear infinite;
}

@keyframes fall {
  from { top: -50px; }
  to { top: 100%; }
}

#cake { display:none; font-size:80px; }

#msg { margin-top:20px; font-size:22px; }

canvas {
  position: fixed;
  top:0;
  left:0;
}
</style>
</head>

<body>

<h1>🎂 Happy Birthday SAIQA 💖</h1>
<h2 id="msg"></h2>

<button onclick="start()">Start 🎉</button>
<button onclick="cake()">Cut Cake 🎂</button>

<div id="cake">🎂</div>

<audio id="music" src="https://www2.cs.uic.edu/~i101/SoundFiles/HappyBirthday.wav"></audio>

<canvas id="fire"></canvas>

<script>
// typing effect
let text = "You are my favorite person SAIQA 💖";
let i = 0;
function type() {
  if(i < text.length){
    document.getElementById("msg").innerHTML += text.charAt(i);
    i++;
    setTimeout(type,50);
  }
}

// start party
function start(){
  document.getElementById("music").play();
  type();

  for(let i=0;i<20;i++){
    let b=document.createElement("div");
    b.className="balloon";
    b.style.left=Math.random()*100+"vw";
    b.style.background="hsl("+Math.random()*360+",100%,
