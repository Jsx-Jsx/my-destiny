# my-destiny
<!DOCTYPE html>
<html lang="zh-CN">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>520 · 给孟先生</title>
  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      min-height: 100vh;
      overflow: hidden;
      font-family: "STKaiti", "KaiTi", "Microsoft YaHei", sans-serif;
      color: #fff;
      background: radial-gradient(circle at top, #ffd1dc 0%, #ff8fab 35%, #5b2245 100%);
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .bg-glow {
      position: fixed;
      inset: 0;
      background:
        radial-gradient(circle at 20% 20%, rgba(255,255,255,0.35), transparent 25%),
        radial-gradient(circle at 80% 10%, rgba(255,209,220,0.35), transparent 30%),
        radial-gradient(circle at 50% 90%, rgba(255,255,255,0.2), transparent 35%);
      animation: breathe 6s ease-in-out infinite alternate;
    }

    @keyframes breathe {
      from { opacity: .65; transform: scale(1); }
      to { opacity: 1; transform: scale(1.04); }
    }

    .card {
      position: relative;
      z-index: 2;
      width: min(88vw, 520px);
      padding: 42px 28px;
      border-radius: 32px;
      background: rgba(255, 255, 255, 0.18);
      backdrop-filter: blur(18px);
      box-shadow: 0 20px 60px rgba(70, 20, 60, 0.35);
      border: 1px solid rgba(255,255,255,.35);
      text-align: center;
      animation: rise 1.2s ease both;
    }

    @keyframes rise {
      from { opacity: 0; transform: translateY(24px); }
      to { opacity: 1; transform: translateY(0); }
    }

    .date {
      font-size: 18px;
      letter-spacing: 4px;
      opacity: .9;
      margin-bottom: 22px;
    }

    h1 {
      font-size: clamp(34px, 8vw, 54px);
      font-weight: 600;
      margin-bottom: 24px;
      text-shadow: 0 4px 18px rgba(90, 10, 60, .35);
    }

    .message {
      font-size: clamp(22px, 5vw, 32px);
      line-height: 1.8;
      letter-spacing: 1px;
      text-shadow: 0 3px 14px rgba(80, 10, 60, .25);
    }

    .heart-line {
      margin: 30px auto 0;
      width: 120px;
      height: 2px;
      background: linear-gradient(90deg, transparent, #fff, transparent);
      position: relative;
    }

    .heart-line::after {
      content: "❤";
      position: absolute;
      left: 50%;
      top: 50%;
      transform: translate(-50%, -52%);
      font-size: 22px;
      color: #fff;
      text-shadow: 0 0 18px rgba(255,255,255,.9);
    }

    .heart {
      position: fixed;
      bottom: -30px;
      color: rgba(255,255,255,.8);
      font-size: 20px;
      animation: floatUp linear infinite;
      z-index: 1;
    }

    @keyframes floatUp {
      0% { transform: translateY(0) scale(.8) rotate(0deg); opacity: 0; }
      15% { opacity: .9; }
      100% { transform: translateY(-110vh) scale(1.5) rotate(20deg); opacity: 0; }
    }

    .footer {
      margin-top: 28px;
      font-size: 15px;
      opacity: .82;
      letter-spacing: 2px;
    }
  </style>
</head>
<body>
  <div class="bg-glow"></div>

  <div class="card">
    <div class="date">2026 · 05 · 20</div>
    <h1>孟先生</h1>
    <div class="message">
      今天比昨天更喜欢你<br />
      希望可以一直站在你身边
    </div>
    <div class="heart-line"></div>
    <div class="footer">愿每一个普通日子，都因为你变得温柔</div>
  </div>

  <script>
    const hearts = ["❤", "♡", "✦", "❀"];
    for (let i = 0; i < 36; i++) {
      const el = document.createElement("div");
      el.className = "heart";
      el.textContent = hearts[Math.floor(Math.random() * hearts.length)];
      el.style.left = Math.random() * 100 + "vw";
      el.style.animationDuration = 6 + Math.random() * 8 + "s";
      el.style.animationDelay = Math.random() * 6 + "s";
      el.style.fontSize = 14 + Math.random() * 24 + "px";
      document.body.appendChild(el);
    }
  </script>
</body>
</html>
