
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Feliz Día Mamá</title>
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', cursive;
      background: radial-gradient(circle at center, #2b2d42, #1a1c2c);
      overflow: hidden;
      height: 100vh;
      color: white;
      display: flex;
      justify-content: center;
      align-items: center;
    }

    .flowers {
      position: absolute;
      width: 100%;
      height: 100%;
      overflow: hidden;
      z-index: 0;
    }

    .flowers span {
      position: absolute;
      font-size: 1.5em;
      animation: fallFlowers linear infinite;
      opacity: 0.8;
    }

    @keyframes fallFlowers {
      0% {
        transform: translateY(-100px) rotate(0deg);
        opacity: 1;
      }
      100% {
        transform: translateY(100vh) rotate(360deg);
        opacity: 0;
      }
    }

    .card {
      position: relative;
      z-index: 1;
      background: rgba(255, 255, 255, 0.1);
      border: 2px solid rgba(255,255,255,0.3);
      border-radius: 20px;
      padding: 30px;
      max-width: 400px;
      text-align: center;
      backdrop-filter: blur(10px);
      animation: fadeIn 2s ease;
    }

    h1 {
      font-size: 2.5em;
      color: #fff398fe;
      margin-bottom: 10px;
      text-shadow: 0 0 10px #ff69b4;
    }

    p {
      font-size: 1.2em;
      color: #f0f0f0;
      margin-bottom: 20px;
    }

    button {
      padding: 12px 25px;
      font-size: 1em;
      background-color: #fff398fe;
      color: #1a1c2c;
      border: none;
      border-radius: 15px;
      cursor: pointer;
      transition: transform 0.3s ease;
      font-weight: bold;
    }

    button:hover {
      transform: scale(1.05);
    }

    .surprise {
      margin-top: 20px;
      font-size: 1.5em;
      color: #fffffff0;
      display: none;
      animation: pop 0.5s ease;
      text-shadow: 0 0 10px #fda9d7;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: scale(0.9); }
      to { opacity: 1; transform: scale(1); }
    }

    @keyframes pop {
      0% { transform: scale(0); opacity: 0; }
      100% { transform: scale(1); opacity: 1; }
    }

    @media (max-width: 500px) {
      .card {
        width: 90%;
        padding: 25px;
      }
    }
  </style>
</head>
<body>
  <div class="flowers" id="flowers"></div>

  <div class="card">
    <h1>🌸 ¡Feliz Día Mamá! 🌸</h1>
    <p>Tu amor florece en cada rincón de mi vida. Hoy celebramos tu ternura, tu fuerza y tu belleza infinita.</p>
    <button onclick="mostrarSorpresa()">🌷 Ver Sorpresa</button>
    <div class="surprise" id="sorpresa">💖 ¡Eres mi jardín favorito, mamá! 💖</div>
  </div>

  <script>
    // Generar lluvia de flores
    const flowersContainer = document.getElementById('flowers');
    const flowerEmojis = ['🌸', '🌷', '💐', '🌺', '🌼'];
    for (let i = 0; i < 50; i++) {
      const flower = document.createElement('span');
      flower.textContent = flowerEmojis[Math.floor(Math.random() * flowerEmojis.length)];
      flower.style.left = Math.random() * 100 + '%';
      flower.style.animationDuration = (Math.random() * 3 + 2) + 's';
      flower.style.animationDelay = Math.random() * 5 + 's';
      flowersContainer.appendChild(flower);
    }

    function mostrarSorpresa() {
      const sorpresa = document.getElementById('sorpresa');
      sorpresa.style.display = 'block';
    }
  </script>
</body>
</html>
