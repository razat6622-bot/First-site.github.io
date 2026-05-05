<!DOCTYPE html>
<html>
<head>
<title>Happy Birthday 🎉</title>
<style>
body {
  text-align: center;
  background: linear-gradient(45deg, #ff4e50, #f9d423);
  font-family: Arial;
  color: white;
}
h1 {
  font-size: 40px;
  margin-top: 50px;
}
button {
  padding: 15px 25px;
  font-size: 18px;
  border: none;
  background: white;
  color: black;
  border-radius: 10px;
}
.balloon {
  width: 50px;
  height: 70px;
  background: red;
  border-radius: 50%;
  position: absolute;
  animation: float 5s infinite;
}
@keyframes float {
  from { bottom: -100px; }
  to { bottom: 100%; }
}
</style>
</head>

<body>

<h1>🎂 Happy Birthday 🎉</h1>

<button onclick="startParty()">Click Here 🎁</button>

<audio id="music" src="https://www2.cs.uic.edu/~i101/SoundFiles/HappyBirthday.wav"></audio>

<script>
function startParty() {
  document.getElementById("music").play();

  for (let i = 0; i < 10; i++) {
    let balloon = document.createElement("div");
    balloon.className = "balloon";
    balloon.style.left = Math.random() * 100 + "vw";
    balloon.style.background = "hsl(" + Math.random()*360 + ",100%,50%)";
    document.body.appendChild(balloon);
  }

  alert("🎉 Surprise!!! 🎂");
}
</script>

</body>
</html># First-site.github.io
