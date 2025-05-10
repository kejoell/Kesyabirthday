# Kesyabirthday
<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Selamat Ulang Tahun Keysa!</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(135deg, #ff9a9e 0%, #fad0c4 100%);
      color: #fff;
      text-align: center;
      overflow-x: hidden;
    }

    h1 {
      font-size: 3em;
      margin-top: 80px;
      animation: fadeInDown 2s ease-out;
    }

    p {
      font-size: 1.5em;
      max-width: 700px;
      margin: 30px auto;
      animation: fadeIn 3s ease-in;
    }

    .love {
      font-size: 2.5em;
      color: #fff;
      animation: pulse 2s infinite;
    }

    @keyframes fadeInDown {
      from { opacity: 0; transform: translateY(-50px); }
      to { opacity: 1; transform: translateY(0); }
    }

    @keyframes fadeIn {
      from { opacity: 0; }
      to { opacity: 1; }
    }

    @keyframes pulse {
      0%, 100% { transform: scale(1); }
      50% { transform: scale(1.2); }
    }

    .balloons {
      position: absolute;
      bottom: -150px;
      left: 50%;
      transform: translateX(-50%);
      animation: rise 10s infinite linear;
    }

    @keyframes rise {
      from { transform: translate(-50%, 100%); }
      to { transform: translate(-50%, -200%); }
    }

    .button-container {
      margin-top: 40px;
    }

    .surprise-button {
      padding: 15px 30px;
      background-color: #fff;
      color: #ff6f91;
      border: none;
      border-radius: 30px;
      font-size: 1.2em;
      cursor: pointer;
      box-shadow: 0 4px 10px rgba(0,0,0,0.2);
      transition: background-color 0.3s;
    }

    .surprise-button:hover {
      background-color: #ffe2e9;
    }

    .message {
      display: none;
      margin-top: 30px;
      font-size: 1.5em;
      animation: fadeIn 2s ease-in-out;
    }
  </style>
</head>
<body>
  <h1>Selamat Ulang Tahun ke-18, Keysa!</h1>
  <p>Hari ini adalah hari yang spesial, karena 18 tahun lalu lahirlah seseorang yang sangat aku cintai. Semoga Keysa selalu bahagia, sehat, dan semua impianmu tercapai. Aku selalu ada buat kamu. I love you so much!</p>
  <div class="love">♥</div>

  <div class="button-container">
    <button class="surprise-button" onclick="showSurprise()">Klik untuk Kejutan!</button>
    <div class="message" id="surpriseMessage">Selamat ulang tahun sayang! Kamu adalah hadiah terindah dalam hidupku!</div>
  </div>

  <img class="balloons" src="https://i.imgur.com/5y7Y9rJ.png" alt="balon" width="150">

  <!-- Musik ulang tahun -->
  <audio autoplay loop>
    <source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3" type="audio/mpeg">
    Browser kamu tidak mendukung audio.
  </audio>

  <!-- Confetti effect -->
  <script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.6.0/dist/confetti.browser.min.js"></script>
  <script>
    function showSurprise() {
      const message = document.getElementById('surpriseMessage');
      message.style.display = 'block';

      // Tembakkan confetti
      confetti({
        particleCount: 150,
        spread: 100,
        origin: { y: 0.6 }
      });
    }
  </script>
</body>
</html>
