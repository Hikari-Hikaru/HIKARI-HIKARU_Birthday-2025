<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8">
  <title>2025年8月10日 - My birthday!</title>
  <link rel="stylesheet" href="../style.css">

  <style>
    #blackout {
      display: none;
      position: fixed;
      inset: 0;
      background: black;
      z-index: 9999;
    }

    .protected-photo {
      width: 100%;
      user-select: none;
      -webkit-user-drag: none;
      pointer-events: auto;
      display: block;
    }

    .watermark-container {
      position: relative;
      display: inline-block;
      width: 300px;
      margin-bottom: 16px;
    }

    .watermark {
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      color: white;
      font-size: 24px;
      opacity: 0.2;
      background: rgba(0, 0, 0, 0.5);
      padding: 10px 20px;
      border-radius: 10px;
      text-shadow: 2px 2px 4px black;
      pointer-events: none;
      white-space: nowrap;
    }
  </style>
</head>
<body oncontextmenu="return false;" onselectstart="return false;" ondragstart="return false;">
  <header>
    <h1>HIKARI・HIKARU 日々のブログ</h1>
  </header>

  <main>
    <h2>2025年8月10日 - ハッピーバースデー🎂✨</h2>
    <p>
      今日は私のお誕生日です！<br>
      「大谷翔平選手」や「ジャスティン・ビーバーさん」と同年代なんです。実は私... <br>
      特に特別なことは無いのですが、毎年思うのが「誕生日」ってちょっとワクワクしますよね(笑)。<br><br>
      そんなこんなで、今後ともよろしくお願いいたします！
    </p>

    <div class="watermark-container">
      <img src="https://hikari-hikaru.github.io/dairy5/image2.jpeg" alt="今日の主人公" class="protected-photo">
      <div class="watermark">© HIKARI-HIKARU 2025</div>
    </div>
  </main>

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
      photo.addEventListener('touchend', () => clearTimeout(timer));
      photo.addEventListener('touchcancel', () => clearTimeout(timer));
    });

    blackout.addEventListener('click', () => {
      blackout.style.display = 'none';
    });
  </script>
</body>
</html>
