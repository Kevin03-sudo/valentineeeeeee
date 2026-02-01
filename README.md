<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Valentine?</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #ffe6e6;
      height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      text-align: center;
      overflow: hidden;
    }

    .container {
      background: white;
      padding: 40px;
      border-radius: 15px;
      box-shadow: 0 10px 30px rgba(0,0,0,0.1);
    }

    h1 {
      color: #cc0000;
    }

    .buttons {
      margin-top: 30px;
      position: relative;
      height: 100px;
    }

    #yesBtn {
      font-size: 20px;
      padding: 15px 40px;
      background-color: #ff4d4d;
      color: white;
      border: none;
      border-radius: 10px;
      cursor: pointer;
    }

    #noBtn {
      font-size: 12px;
      padding: 8px 16px;
      background-color: #cccccc;
      color: black;
      border: none;
      border-radius: 8px;
      cursor: pointer;
      position: absolute;
      left: 60%;
      top: 20px;
    }

    .shy-text {
      margin-top: 20px;
      font-style: italic;
      color: #666;
    }

    .heart {
      font-size: 100px;
      color: red;
      margin-top: 20px;
      display: none;
    }
  </style>
</head>
<body>

  <div class="container">
    <h1>Pheladi, will you be my valentine? ❤️</h1>

    <div class="buttons">
      <button id="yesBtn">YES</button>
      <button id="noBtn">no</button>
    </div>

    <div class="shy-text">no seems a bit shy</div>

    <div class="heart" id="heart">❤️</div>
  </div>

  <script>
    const noBtn = document.getElementById("noBtn");
    const yesBtn = document.getElementById("yesBtn");
    const heart = document.getElementById("heart");

    noBtn.addEventListener("mouseover", () => {
      const x = Math.random() * 300 - 150;
      const y = Math.random() * 150 - 75;

      noBtn.style.transform = `translate(${x}px, ${y}px)`;
    });

    yesBtn.addEventListener("click", () => {
      heart.style.display = "block";
    });
  </script>

</body>
</html>
