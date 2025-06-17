<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Una página muy especial 💖</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      background: url('1000029809.jpg') center/cover no-repeat;
      font-family: 'Comic Sans MS', cursive, sans-serif;
      color: #fff;
      text-align: center;
      height: 100vh;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      overflow: hidden;
    }

    h1 {
      background: rgba(255, 105, 180, 0.8);
      padding: 20px;
      border-radius: 20px;
      font-size: 24px;
      max-width: 90%;
    }

    .question {
      margin-top: 20px;
      font-size: 20px;
    }

    .buttons {
      margin-top: 30px;
    }

    button {
      font-size: 18px;
      padding: 10px 20px;
      margin: 10px;
      border: none;
      border-radius: 10px;
      cursor: pointer;
      transition: all 0.3s ease;
    }

    .yes {
      background-color: #ff69b4;
      color: white;
    }

    .no {
      background-color: #ccc;
      color: black;
      position: relative;
    }

    .celebrate, .sad {
      display: none;
      font-size: 32px;
      margin-top: 20px;
    }

    .show {
      display: block;
      animation: fadeIn 1s ease;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: scale(0.8); }
      to { opacity: 1; transform: scale(1); }
    }
  </style>
</head>
<body>
  <h1>La verdad me pareciste una chica muy linda y me caíste muy bien y quisiera llegar a algo más contigo si tú quisieras 💌</h1>
  <div class="question">¿Podemos seguir hablando?</div>

  <div class="buttons">
    <button class="yes">Sí 💕</button>
    <button class="no">No 💔</button>
  </div>

  <div class="celebrate">🎉 ¡Yay! Me alegra mucho 😄</div>
  <div class="sad">😢 Qué triste... pero igual te deseo lo mejor 😔</div>

  <script>
    const yesBtn = document.querySelector(".yes");
    const noBtn = document.querySelector(".no");
    const celebrate = document.querySelector(".celebrate");
    const sad = document.querySelector(".sad");

    yesBtn.addEventListener("click", () => {
      celebrate.classList.add("show");
      sad.classList.remove("show");
    });

    noBtn.addEventListener("click", () => {
      sad.classList.add("show");
      celebrate.classList.remove("show");
    });

    noBtn.addEventListener("mouseover", () => {
      const x = Math.random() * (window.innerWidth - 100);
      const y = Math.random() * (window.innerHeight - 50);
      noBtn.style.position = "absolute";
      noBtn.style.left = `${x}px`;
      noBtn.style.top = `${y}px`;
    });
  </script>
</body>
</html>
