<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8">
  <title>2025年8月10日 - My birthday! </title>
  <link rel="stylesheet" href="../style.css"> <!-- 共通CSSの読み込み -->
   <style>
    #blackout {
      display: none;
      position: fixed;
      inset: 0;
      background: black;
      z-index: 9999;
    }

    .protected-photo {
      width: 300px;
      user-select: none;
      -webkit-user-drag: none;
      pointer-events: auto;
      margin-bottom: 16px;
    }
  </style>
</head>
<body>
  <header>
    <h1>HIKARI・HIKARU 日々のブログ</h1>
  </header>
  <main>
    <h2>2025年8月10日 - ハッピーバースデー🎂✨</h2>
    <p>
      今日は私のお誕生日です！<br>
      「大谷翔平選手」や「ジャスティン・ビーバーさん」と同年代なんです。実は私...(フフフッ) <br><br>
      特に特別なことは無いのですが、毎年思うのが「誕生日」ってちょっとワクワクしますよね(笑)。
      <br><br>
    　実は初めての自分の写真載せてみました(笑)<br><br>
      <br><br>
      そんなこんなで、今後ともよろしくお願いいたします！
       </p>

    <!-- 私、実は初めての自分の写真載せてみました(笑) -->
   <img src="https://hikari-hikaru.github.io/dairy5/image2.jpeg" alt="今日の主人公" width="300">
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
