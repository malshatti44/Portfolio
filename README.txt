<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Mohammad AlShatti</title>

  <style>
    *{
      box-sizing: border-box;
    }

    body{
      margin: 0;
      min-height: 100vh;
      background: #000;
      display: flex;
      align-items: center;
      justify-content: center;
      font-family: -apple-system, BlinkMacSystemFont, "SF Pro Display",
                   "Segoe UI", Inter, Arial, sans-serif;
      color: #fff;
      -webkit-font-smoothing: antialiased;
      text-rendering: optimizeLegibility;
    }

    /* Hero Box */
    .hero-box{
      position: relative;
      width: min(90%, 900px);
      padding: 44px 36px;
      border-radius: 18px;
      background: rgba(255,255,255,0.04);
      border: 1px solid rgba(255,255,255,0.12);
      text-align: center;
      overflow: hidden;
    }

    /* Light interaction */
    .hero-box::before{
      content: "";
      position: absolute;
      inset: -1px;
      background: radial-gradient(
        420px 220px at var(--x, 50%) var(--y, 50%),
        rgba(255,255,255,0.18),
        transparent 60%
      );
      opacity: 0;
      transition: opacity 0.25s ease;
      pointer-events: none;
    }

    .hero-box:hover::before{
      opacity: 1;
    }

    h1{
      margin: 0;
      font-size: clamp(44px, 8vw, 72px);
      font-weight: 600;
      letter-spacing: -0.02em;
    }

    p{
      margin-top: 16px;
      font-size: clamp(15px, 3.5vw, 18px);
      line-height: 1.7;
      color: rgba(255,255,255,0.7);
    }

    @media (max-width: 480px){
      .hero-box{
        padding: 36px 24px;
      }
    }
  </style>
</head>

<body>

  <div class="hero-box" id="hero">
    <h1>Mohammad AlShatti</h1>
    <p>
      Educational Technology, Artificial Intelligence & Digital Design Specialist.<br>
      Designing smart educational systems with clarity and purpose.
    </p>
  </div>

  <script>
    const hero = document.getElementById("hero");

    hero.addEventListener("mousemove", (e) => {
      const rect = hero.getBoundingClientRect();
      const x = e.clientX - rect.left;
      const y = e.clientY - rect.top;
      hero.style.setProperty("--x", x + "px");
      hero.style.setProperty("--y", y + "px");
    });
  </script>

</body>
</html>
