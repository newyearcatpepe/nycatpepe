<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>NewYearCatPepe | To The Moon! 🚀</title>
    <link href="https://fonts.googleapis.com/css2?family=Bangers&family=Open+Sans:wght@400;700&display=swap" rel="stylesheet">
    <style>
        /* TEMEL STİLLER */
        body {
            margin: 0;
            padding: 0;
            font-family: 'Open Sans', sans-serif;
            background-color: #0b251a; /* Koyu yılbaşı yeşili */
            color: white;
            overflow-x: hidden;
            text-align: center;
        }

        h1, h2 { font-family: 'Bangers', cursive; letter-spacing: 2px; }

        /* KAR YAĞIŞI EFEKTİ */
        .snow-container {
            position: fixed;
            top: 0; left: 0; right: 0; bottom: 0;
            pointer-events: none;
            z-index: 1000;
        }
        .snowflake {
            position: absolute;
            background-color: white;
            border-radius: 50%;
            opacity: 0.8;
            animation: fall linear infinite;
        }
        @keyframes fall {
            0% { transform: translateY(-10vh); }
            100% { transform: translateY(110vh); }
        }

        /* HERO BÖLÜMÜ (ANA RESİM) */
        .hero {
            padding: 100px 20px;
            background: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)), url('https://images.unsplash.com/photo-1543589077-47d81606c1bf?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80');
            background-size: cover;
            background-position: center;
            border-bottom: 5px solid #c41e3a; /* Noel kırmızısı */
        }

        .coin-title { font-size: 5rem; color: #f1c40f; text-shadow: 3px 3px #c41e3a; margin-bottom: 10px; }

        .pump-link {
            display: inline-block;
            background-color: #2ecc71;
            color: white;
            padding: 20px 40px;
            font-size: 1.5rem;
            text-decoration: none;
            border-radius: 50px;
            font-weight: bold;
            box-shadow: 0 0 20px #2ecc71;
            transition: 0.3s;
            margin: 20px;
        }
        .pump-link:hover { transform: scale(1.1); background-color: #27ae60; }

        /* ROADMAP (YOL HARİTASI) */
        .section { padding: 80px 20px; }
        .roadmap-grid {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 20px;
            max-width: 1000px;
            margin: 0 auto;
        }
        .roadmap-item {
            background: rgba(255, 255, 255, 0.1);
            padding: 30px;
            border-radius: 15px;
            width: 250px;
            border: 2px solid #c41e3a;
        }

        /* MEME GALERİSİ */
        .meme-gallery {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 15px;
            padding: 20px;
        }
        .meme-item {
            background: #fff;
            height: 250px;
            border-radius: 10px;
            color: #333;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            font-size: 1.2rem;
            border: 4px solid #f1c40f;
        }

        /* NOEL AĞACI ANİMASYONU */
        .trees { font-size: 50px; margin: 20px; display: block; animation: swing 2s infinite ease-in-out; }
        @keyframes swing {
            0%, 100% { transform: rotate(-5deg); }
            50% { transform: rotate(5deg); }
        }
    </style>
</head>
<body>

    <div class="snow-container" id="snow"></div>

    <header class="hero">
        <span class="trees">🎄 🎅 🎄</span>
        <h1 class="coin-title">NewYearCatPepe</h1>
        <p style="font-size: 1.5rem;">2025'in En Hızlı Kedisi! Miyav-Pepe Geliyor!</p>
        <a href="https://pump.fun/coin/SENIN_COIN_ADRESIN" class="pump-link" target="_blank">🚀 BUY ON PUMP.FUN 🚀</a>
    </header>

    <section id="roadmap" class="section">
        <h2>🗺️ ROADMAP (Yol Haritası)</h2>
        <div class="roadmap-grid">
            <div class="roadmap-item">
                <h3>Aşama 1</h3>
                <p>Coin Lansmanı & Pump.fun Hype</p>
            </div>
            <div class="roadmap-item">
                <h3>Aşama 2</h3>
                <p>Meme Yarışmaları & Twitter Akını</p>
            </div>
            <div class="roadmap-item">
                <h3>Aşama 3</h3>
                <p>Raydium Listeleme & Yılbaşı Partisi</p>
            </div>
        </div>
    </section>

    <section id="memes" class="section" style="background: rgba(0,0,0,0.2);">
        <h2>🔥 MEMES 🔥</h2>
        <div class="meme-gallery">
            <div class="meme-item" style="background-image: url('https://via.placeholder.com/300x300?text=Kedi+Pepe+1'); background-size: cover;"></div>
            <div class="meme-item" style="background-image: url('https://via.placeholder.com/300x300?text=Kedi+Pepe+2'); background-size: cover;"></div>
            <div class="meme-item" style="background-image: url('https://via.placeholder.com/300x300?text=Kedi+Pepe+3'); background-size: cover;"></div>
            <div class="meme-item" style="background-image: url('https://via.placeholder.com/300x300?text=Kedi+Pepe+4'); background-size: cover;"></div>
        </div>
    </section>

    <footer style="padding: 50px; background: #05140e;">
        <p>© 2025 NewYearCatPepe. Bu bir mizah coindir, yatırım tavsiyesi değildir! 🐱🐸</p>
    </footer>

    <script>
        // Kar yağışı oluşturma kodu
        const snowContainer = document.getElementById('snow');
        const flakeCount = 50;

        for (let i = 0; i < flakeCount; i++) {
            const flake = document.createElement('div');
            flake.className = 'snowflake';
            const size = Math.random() * 5 + 2 + 'px';
            flake.style.width = size;
            flake.style.height = size;
            flake.style.left = Math.random() * 100 + 'vw';
            flake.style.animationDuration = Math.random() * 3 + 2 + 's';
            flake.style.opacity = Math.random();
            snowContainer.appendChild(flake);
        }
    </script>

</body>
</html>
