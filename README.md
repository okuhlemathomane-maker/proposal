<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Be My Valentine 💘</title>
  <style>
    body {
      margin: 0;
      height: 100vh;
      background: linear-gradient(135deg, #ff758c, #ff7eb3);
      display: flex;
      align-items: center;
      justify-content: center;
      font-family: 'Arial', sans-serif;
      color: white;
      text-align: center;
      overflow: hidden;
    }

    .card {
      background: rgba(255,255,255,0.15);
      padding: 30px;
      border-radius: 20px;
      box-shadow: 0 10px 30px rgba(0,0,0,0.2);
      width: 90%;
      max-width: 400px;
    }

    h1 {
      font-size: 28px;
      margin-bottom: 10px;
    }

    p {
      font-size: 18px;
      margin-bottom: 25px;
    }

    button {
      padding: 12px 25px;
      font-size: 16px;
      border: none;
      border-radius: 30px;
      cursor: pointer;
      margin: 10px;
      transition: 0.3s;
    }

    #yes {
      background: #ff2e63;
      color: white;
    }

    #no {
      background: white;
      color: #ff2e63;
      position: absolute;
    }

    .hidden {
      display: none;
    }
  </style>
</head>
<body>

  <div class="card" id="card">
    <h1>Hey ASIPHE 💕</h1>
    <p>Yes you…short stuff 😌</p>
    <p>I have one very important question for you…</p>
    <h2>Will you be my Valentine? 💌</h2>
    <button id="yes">YES 😍</button>
    <button id="no">NO 🙃</button>
  </div>

  <div class="card hidden" id="response">
    <h1>YAYYYY 🥰💖</h1>
    <p>I knew my short stuff wouldn’t say no 😉</p>
    <p>Happy Valentine’s Day, my love 🌹</p>
  </div>

  <script>
    const noBtn = document.getElementById("no");
    const yesBtn = document.getElementById("yes");
    const card = document.getElementById("card");
    const response = document.getElementById("response");

    noBtn.addEventListener("mouseover", () => {
      const x = Math.random() * (window.innerWidth - 100);
      const y = Math.random() * (window.innerHeight - 50);
      noBtn.style.left = x + "px";
      noBtn.style.top = y + "px";
    });

    yesBtn.addEventListener("click", () => {
      card.classList.add("hidden");
      response.classList.remove("hidden");
    });
  </script>

</body>
</html>
