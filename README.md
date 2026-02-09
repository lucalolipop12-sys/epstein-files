<!DOCTYPE html>
<html lang="de">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>2. Date?</title>
  <style>
    body {
      margin: 0;
      height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      background: linear-gradient(135deg, #ff9a9e, #fad0c4);
      font-family: Arial, Helvetica, sans-serif;
    }

    .card {
      background: white;
      padding: 30px 25px;
      border-radius: 20px;
      box-shadow: 0 10px 30px rgba(0,0,0,0.2);
      text-align: center;
      max-width: 320px;
      width: 100%;
    }

    h1 {
      font-size: 1.6rem;
      margin-bottom: 20px;
    }

    .buttons {
      display: flex;
      gap: 15px;
      justify-content: center;
    }

    button {
      border: none;
      border-radius: 999px;
      padding: 12px 22px;
      font-size: 1rem;
      cursor: pointer;
      transition: all 0.2s ease;
    }

    #yesBtn {
      background: #4CAF50;
      color: white;
      font-size: 1.1rem;
    }

    #noBtn {
      background: #f44336;
      color: white;
    }

    .message {
      margin-top: 20px;
      font-size: 1.2rem;
      display: none;
    }
  </style>
</head>
<body>
  <div class="card">
    <h1>Willst du mit mir auf ein 2. Date? 💖</h1>
    <div class="buttons">
      <button id="yesBtn">Ja 😍</button>
      <button id="noBtn">Nein 🙃</button>
    </div>
    <div class="message" id="message">
      Yaaay! Ich freu mich 🥰
    </div>
  </div>

  <script>
    const yesBtn = document.getElementById("yesBtn");
    const noBtn = document.getElementById("noBtn");
    const message = document.getElementById("message");

    let yesScale = 1;

    noBtn.addEventListener("click", () => {
      yesScale += 0.2;
      yesBtn.style.transform = `scale(${yesScale})`;
    });

    yesBtn.addEventListener("click", () => {
      message.style.display = "block";
      yesBtn.style.display = "none";
      noBtn.style.display = "none";
    });
  </script>
</body>
</html>
