# I-love-you-
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>I Love You</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      background-color: #ffdee9;
      background-image: linear-gradient(0deg, #ffdee9 0%, #b5fffc 100%);
      overflow: hidden;
      font-family: 'Arial', sans-serif;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      flex-direction: column;
    }

    h1 {
      font-size: 3em;
      color: #ff0066;
      z-index: 10;
      text-shadow: 2px 2px 4px #00000033;
    }

    .heart {
      position: absolute;
      top: -10px;
      font-size: 20px;
      animation: fall 5s linear infinite;
      color: red;
      user-select: none;
    }

    @keyframes fall {
      to {
        transform: translateY(100vh) rotate(360deg);
        opacity: 0;
      }
    }
  </style>
</head>
<body>
  <h1>I Love You ❤️</h1>

  <script>
    function createHeart() {
      const heart = document.createElement('div');
      heart.classList.add('heart');
      heart.textContent = '❤️';
      heart.style.left = Math.random() * 100 + 'vw';
      heart.style.fontSize = Math.random() * 20 + 20 + 'px';
      document.body.appendChild(heart);

      setTimeout(() => {
        heart.remove();
      }, 5000);
    }

    setInterval(createHeart, 300);
  </script>
</body>
</html>
