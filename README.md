<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>KitKat's Secret Page</title>
  <style>
    body {
      margin: 0;
      font-family: 'Comic Sans MS', cursive, sans-serif;
      background-color: #fff0f5;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      height: 100vh;
    }
    .container {
      background: #ffccf9;
      border: 3px dashed #ff69b4;
      padding: 40px;
      border-radius: 20px;
      box-shadow: 0 0 20px #ff69b4;
      text-align: center;
      max-width: 400px;
      width: 90%;
    }
    input[type="password"] {
      padding: 10px;
      border: none;
      border-radius: 10px;
      font-size: 16px;
      width: 100%;
      box-sizing: border-box;
    }
    button {
      margin-top: 20px;
      padding: 10px 20px;
      background: #ff69b4;
      color: white;
      border: none;
      border-radius: 10px;
      cursor: pointer;
      font-size: 16px;
      width: 100%;
    }
    .hint {
      font-size: 14px;
      margin-top: 10px;
      color: #ff1493;
    }
  </style>
</head>
<body>
  <div class="container">
    <p class="hint">Aap ke pasandida mard ne aap ka jo naam rakha tha woh password hai</p>
    <input type="password" id="password" placeholder="Enter password" />
    <button onclick="checkPassword()">Unlock</button>
  </div>

  <script>
    function checkPassword() {
      const pass = document.getElementById("password").value.toLowerCase();
      if (pass === "kitkat") {
        document.body.innerHTML = `
          <div style="
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh;
            background-color: white;
            font-family: 'Comic Sans MS', cursive;
          ">
            <h1 style="font-size: 2.5rem; color: black;">I love you KitKat</h1>
            <div style="font-size: 5rem; color: red;">❤️</div>
          </div>
        `;
      } else {
        alert("Galat password! Yah website aap ke liye nahi hai");
      }
    }
  </script>
</body>
</html>
