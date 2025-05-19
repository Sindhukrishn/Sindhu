
!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Happy Birthday Sindhu</title>
  <style>
    body {
      margin: 0;
      background: #fff0f5;
      font-family: 'Segoe UI', sans-serif;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
    }
    .card {
      width: 300px;
      height: 200px;
      background: pink;
      border-radius: 10px;
      box-shadow: 0 0 10px rgba(0,0,0,0.3);
      cursor: pointer;
      position: relative;
      transform-style: preserve-3d;
      transition: transform 1s;
    }
    .card.open {
      transform: rotateY(180deg);
    }
    .card .front, .card .back {
      position: absolute;
      width: 100%;
      height: 100%;
      backface-visibility: hidden;
      display: flex;
      justify-content: center;
      align-items: center;
      border-radius: 10px;
    }
    .card .front {
      background: #ffb6c1;
      color: white;
      font-size: 24px;
    }
    .card .back {
      background: white;
      transform: rotateY(180deg);
      flex-direction: column;
      padding: 20px;
      text-align: center;
      color: #c71585;
    }
    .back h1 {
      font-size: 22px;
      margin-bottom: 10px;
    }
    .back p {
      font-size: 16px;
    }
    audio {
      margin-top: 15px;
    }
  </style>
</head>
<body>
  <div class="card" onclick="openCard()">
    <div class="front">Tap to Open</div>
    <div class="back">
      <h1>Happy Birthday, Sindhu!</h1>
      <p>Wishing you joy, love, and sparkle today and always.</p>
      <audio controls autoplay>
        <source src="happy_birthday_voice.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
    </div>
  </div>

  <script>
    function openCard() {
      document.querySelector('.card').classList.add('open');
    }
  </script>
</body>
</html>

