<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8" />
  <title>2025.08.10.-My birthday🎂✨</title>
  <link rel="stylesheet" href="../style.css" />

  <style>
    body {
      background-color: #ffc0cb; /* ベビーピンク */
      color: #ff69b4; /* ショッキングピンク */
      font-family: sans-serif;
      margin: 0;
      padding: 20px;
    }

    p {
      color: #000; /* 本文の黒文字 */
      font-size: 1.1em;
      line-height: 1.6;
    }

    #blackout {
      display: none;
      position: fixed;
      inset: 0;
      background: black;
      z-index: 9999;
    }

    .gallery {
      display: flex;
      gap: 10px; /* 画像の間隔 */
      justify-content: center;
      flex-wrap: wrap; /* スマホで縦並びに */
    }

    .watermark-container {
      position: relative;
      width: 45%; /* 2枚が横に収まる */
      max-width: 400px;
    }

    .protected-photo {
      width: 100%;
      display: block;
      user-select: none;
      -webkit-user-drag: none;
      pointer-events: auto;
    }

    /* 全面ウォーターマーク */
    .watermark-container::before {
      content: "@HIKARUHIKARI ";
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      color: rgba(255, 105, 180, 0.1); /* ショッキングピンク薄め */
      font-size: 2em;
      font-weight: bold;
      white-space: pre;
      pointer-events: none;
      background-repeat: repeat;
      background-size: 150px 150px;
      background-image: repeating-linear-gradient(
        45deg,
        rgba(255, 105, 180, 0.1) 0,
        rgba(255, 105, 180, 0.1) 50%,
        transparent 50%,
        transparent 100%
      );
      background-clip: text;
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      mix-blend-mode: overlay;
    }
  </style>
</head>
<body>
  <h1>2025.08.10.-My birthday🎂✨</h1>

  <p>
    今日はHIKARI・HIKARUの誕生日です！笑。ちなみに大谷翔平選手世代なので31歳になりました✨<br>
    これからもいろんなことに挑戦しようと思うので、みなさんよろしくお願いします👍
  </p>

  <div class="gallery">
    <div class="watermark-container">
     <img src="https://raw.githubusercontent.com/Hikari-Hikaru/HIKARI-introdaction/main/image0.jpeg" alt="誕生日の写真1" class="protected-photo">
    </div>
    <div class="watermark-container">
     <img src="https://raw.githubusercontent.com/Hikari-Hikaru/HIKARI-introdaction/main/image2.jpeg" alt="誕生日の写真2" class="protected-photo">
    </div>
  </div>

  <div id="blackout"></div>

  <script>
    const photos = document.querySelectorAll('.protected-photo');
    const blackout = document.getElementById('blackout');
    photos.forEach(photo => {
      let timer;
      photo.addEventListener('touchstart', () => {
        timer = setTimeout(() => {
          blackout.style.display = 'block';
        }, 500);
      });
      photo.addEventListener('touchend', () => {
        clearTimeout(timer);
      });
      photo.addEventListener('touchcancel', () => {
        clearTimeout(timer);
      });
    });
    blackout.addEventListener('click', () => {
      blackout.style.display = 'none';
    });
  </script>
</body>
</html>
