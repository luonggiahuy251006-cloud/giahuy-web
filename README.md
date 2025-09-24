<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="UTF-8">
  <title>Nguyệt Lam dễ thương</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      overflow: hidden;
      background: #fff;
    }
    .marquee {
      position: absolute;
      top: 40%;
      width: 100%;
      font-size: 40px;
      font-weight: bold;
      color: #ff1493;
      white-space: nowrap;
      animation: scroll-left 12s linear infinite;
      text-align: center;
    }
    @keyframes scroll-left {
      0%   { transform: translateX(100%); }
      100% { transform: translateX(-100%); }
    }
    .heart {
      position: absolute;
      width: 20px;
      height: 20px;
      background: red;
      transform: rotate(-45deg);
      animation: fall 5s linear infinite;
    }
    .heart::before,
    .heart::after {
      content: "";
      position: absolute;
      width: 20px;
      height: 20px;
      background: red;
      border-radius: 50%;
    }
    .heart::before {
      top: -10px;
      left: 0;
    }
    .heart::after {
      left: 10px;
      top: 0;
    }
    @keyframes fall {
      0% {
        transform: translateY(-10px) rotate(-45deg);
        opacity: 1;
      }
      100% {
        transform: translateY(110vh) rotate(-45deg);
        opacity: 0;
      }
    }
  </style>
</head>
<body>
  <div class="marquee">💖 Nguyệt Lam dễ thương !! 💖</div>

  <script>
    function createHeart() {
      const heart = document.createElement("div");
      heart.className = "heart";
      heart.style.left = Math.random() * window.innerWidth + "px";
      heart.style.animationDuration = (3 + Math.random() * 3) + "s"; 
      document.body.appendChild(heart);

      setTimeout(() => {
        heart.remove();
      }, 6000);
    }

    setInterval(createHeart, 300);
  </script>
</body>
</html>
[index.html](https://github.com/user-attachments/files/22514509/index.html)
