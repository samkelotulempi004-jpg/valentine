<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Be My Valentine ❤️</title>
  <style>
    body {
      margin: 0;
      height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      background: linear-gradient(135deg, #ff9a9e, #fad0c4);
      font-family: Arial, sans-serif;
    }

    .card {
      background: white;
      padding: 30px;
      border-radius: 20px;
      box-shadow: 0 10px 30px rgba(0,0,0,0.2);
      text-align: center;
      width: 320px;
    }

    h1 {
      color: #e60073;
    }

    .buttons {
      margin-top: 20px;
      position: relative;
      height: 100px;
    }

    button {
      padding: 12px 22px;
      font-size: 16px;
      border: none;
      border-radius: 30px;
      cursor: pointer;
      position: absolute;
    }

    #yesBtn {
      background: #e60073;
      color: white;
      left: 50%;
      transform: translateX(-50%);
    }

    #noBtn {
      background: #ccc;
      color: #333;
      left: 10px;
      top: 50px;
    }

    .sticker {
      display: none;
      margin-top: 25px;
      font-size: 50px;
      animation: pop 0.5s ease-out;
    }

    @keyframes pop {
      0% { transform: scale(0); }
      100% { transform: scale(1); }
    }
  </style>
</head>
<body>

  <div class="card">
    <h1>Sphume, will you be my Valentine? 💘</h1>

    <div class="buttons">
      <button id="yesBtn" onclick="sayYes()">YES 💖</button>
      <button id="noBtn" onmouseover="runAway()">NO 😅</button>
    </div>

    <div class="sticker" id="sticker">🎉 YEY!!! 💕🥰 <br>
  ⏰ Clock it!</div>
  </div>

  <script>
    function sayYes() {
      document.getElementById("sticker").style.display = "block";
    }

    function runAway() {
      const noBtn = document.getElementById("noBtn");
      const container = document.querySelector(".buttons");

      const maxX = container.clientWidth - noBtn.offsetWidth;
      const maxY = container.clientHeight - noBtn.offsetHeight;

      const randomX = Math.random() * maxX;
      const randomY = Math.random() * maxY;

      noBtn.style.left = randomX + "px";
      noBtn.style.top = randomY + "px";
    }
  </script>

</body>
</html>
