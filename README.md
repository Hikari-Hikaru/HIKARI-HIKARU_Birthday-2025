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
      color: #000; /* 本文は黒文字 */
      font-size: 1.1em;
      line-height: 1.6;
    }

    .gallery {
      display: flex;
      gap: 10px; /* 画像間の余白 */
      justify-content: center;
      flex-wrap: wrap; /* スマホで縦並び */
    }

    .watermark-container {
      position: relative;
      width: 45%; /* 2枚横並び */
      max-width: 400px;
      cursor: pointer;
    }

    .protected-photo {
      width: 100%;
      display: block;
      user-select: none;
      -webkit-user-drag: none;
      pointer-events: auto;
      border-radius: 8px;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
      transition: transform 0.2s ease;
    }

    .protected-photo:hover {
      transform: scale(1.03);
    }

    /* モーダル（全画面拡大） */
    #modal {
      display: none;
      position: fixed;
      inset: 0;
      background: rgba(0, 0, 0, 0.8);
      z-index: 9999;
      justify-content: center;
      align-items: center;
    }

    #modal img {
      max-width: 90%;
      max-height: 90%;
      border-radius: 10px;
      box-shadow: 0 0 20px rgba(255, 255, 255, 0.3);
    }

    #modal:active {
      display: none;
    }
  </style>
</head>
<body>
  <h1>2025.08.10.-My birthday🎂✨</h1>

  <p>今日はHIKARI・HIKARUの誕生日です！笑。ちなみに大谷翔平選手世代なので31歳になりました✨<br>
  これからもいろんなことに挑戦しようと思うので、みなさんよろしくお願いします👍</p>

  <div class="gallery">
    <div class="watermark-container">
      <img src="https://raw.githubusercontent.com/Hikari-Hikaru/HIKARI-HIKARU_Birthday-2025/main/image0.jpeg" alt="誕生日の写真1" class="protected-photo">
    </div>
    <div class="watermark-container">
      <img src="https://raw.githubusercontent.com/Hikari-Hikaru/HIKARI-HIKARU_Birthday-2025/main/image2.jpeg" alt="誕生日の写真2" class="protected-photo">
    </div>
  </div>

  <!-- モーダル -->
  <div id="modal">
    <img src="" alt="拡大画像">
  </div>

  <script>
    const modal = document.getElementById('modal');
    const modalImg = modal.querySelector('img');
    const photos = document.querySelectorAll('.protected-photo');

    photos.forEach(photo => {
      photo.addEventListener('click', () => {
        modalImg.src = photo.src;
        modal.style.display = 'flex';
      });
    });

    modal.addEventListener('click', () => {
      modal.style.display = 'none';
      modalImg.src = '';
    });
  </script>
</body>
</html>
