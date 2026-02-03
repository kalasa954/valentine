<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Virginia 💖</title>
  <style>
    body {
      background-color: #ffe6f0;
      font-family: 'Comic Sans MS', cursive, sans-serif;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
    }

    .card {
      background: white;
      padding: 40px;
      border-radius: 20px;
      text-align: center;
      box-shadow: 0 10px 25px rgba(0,0,0,0.15);
      width: 380px;
      position: relative;
    }

    h1 {
      color: #ff4d88;
      font-size: 26px;
    }

    p {
      font-size: 18px;
    }

    .buttons {
      margin-top: 30px;
      position: relative;
      height: 120px;
    }

    button {
      font-size: 18px;
      padding: 12px 28px;
      border-radius: 30px;
      border: none;
      cursor: pointer;
      position: absolute;
    }

    #yes {
      background-color: #ff4d88;
      color: white;
      left: 50%;
      transform: translateX(-50%);
    }

    #no {
      background-color: #ddd;
      color: black;
      left: 30px;
      top: 70px;
    }

    .hidden {
      display: none;
    }

    .celebrate {
      font-size: 20px;
      color: #ff4d88;
    }

    img {
      width: 200px;
      margin-top: 20px;
      border-radius: 15px;
    }
  </style>
</head>
<body>

  <!-- QUESTION CARD -->
  <div class="card" id="card">
    <h1>Virginia 💕</h1>
    <p><strong>Will you be my Valentine?</strong></p>

    <div class="buttons">
      <button id="yes">Yes 💖</button>
      <button id="no">No 😈</button>
    </div>

    <p style="margin-top:20px; font-size:14px; color:#888;">
      “No” seems a bit shy 😏
    </p>
  </div>

  <!-- SUCCESS CARD -->
  <div class="card hidden" id="success">
    <h1>YAAAY!!! 🎉💘</h1>
    <p class="celebrate">
      Virginia, I knew you’d say yes 😍 <br><br>
      Happy Valentine’s Day, my love ❤️
    </p>

    <img src="https://media.giphy.com/media/3o6ZtpxSZbQRRnwCKQ/giphy.gif" alt="Celebration GIF">
  </div>

  <script>
    const noBtn = document.getElementById("no");
    const yesBtn = document.getElementById("yes");
    const card = document.getElementById("card");
    const success = document.getElementById("success");

    noBtn.addEventListener("mouseover", () => {
      const x = Math.random() * 260;
      const y = Math.random() * 90;
      noBtn.style.left = x + "px";
      noBtn.style.top = y + "px";
    });

    yesBtn.addEventListener("click", () => {
      card.classList.add("hidden");
      success.classList.remove("hidden");
    });
  </script>

</body>
</html>
