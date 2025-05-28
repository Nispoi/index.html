# index.html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Сердце</title>
  <style>
    body {
      background-color: #111;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
    }

    .heart {
      width: 100px;
      height: 90px;
      position: relative;
      animation: pulse 2s infinite;
    }

    .heart::before,
    .heart::after {
      content: "";
      position: absolute;
      width: 100px;
      height: 90px;
      background: linear-gradient(45deg, pink, violet);
      border-radius: 50%;
      animation: colorShift 4s infinite alternate;
    }

    .heart::before {
      top: -50px;
      left: 0;
    }

    .heart::after {
      left: 50px;
      top: 0;
    }

    .heart-shape {
      width: 100px;
      height: 100px;
      transform: rotate(-45deg);
      background: linear-gradient(45deg, pink, violet);
      animation: colorShift 4s infinite alternate;
    }

    @keyframes pulse {
      0%, 100% {
        transform: scale(1) rotate(-45deg);
      }
      50% {
        transform: scale(1.1) rotate(-45deg);
      }
    }

    @keyframes colorShift {
      0% {
        background: linear-gradient(45deg, #ffb6c1, #dda0dd);
      }
      100% {
        background: linear-gradient(45deg, #da70d6, #ff69b4);
      }
    }
  </style>
</head>
<body>
  <div class="heart">
    <div class="heart-shape"></div>
  </div>
</body>
</html>
