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

    #blackout {
      display: none;
      position: fixed;
      inset: 0;
      background: black;
      z-index: 9999;
    }

    .watermark-container {
      position: relative;
      display: block;
      max-width: 600px;
      margin: 0 auto 20px;
    }

    .protected-photo {
      width: 100%;
      user-select: none;
      -webkit-user-drag: none;
      pointer-events: auto;
      display: block;
    }

    .watermark-text {
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%) rotate(-30deg);
      color: rgba(255, 105, 180, 0.2); /* ショッキングピンクの透かし（薄い） */
      font-size: 3em;
      font-weight: bold;
      white-space: nowrap;
      pointer-events: none; /* 透かし部分はクリック無効 */
    }
  </style>
</head>
<body>
  <h1>2025.08.10.-My birthday🎂✨</h1>
  <p>今日は私の誕生日！</p>

  <div class="watermark-container">
    <img src="images/image0.jpeg" alt="誕生日の写真" class="protected-photo">
    <div class="watermark-text">@HIKARUHIKARI</div>
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
