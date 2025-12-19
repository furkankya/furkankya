<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Yazılım Geliştirici Profili</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        :root {
            --bg-color: #0d1117;
            --card-bg: #161b22;
            --border-color: #30363d;
            --text-main: #c9d1d9;
            --text-dim: #8b949e;
            --accent-green: #39d353;
            --accent-blue: #58a6ff;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, Arial, sans-serif;
            background-color: var(--bg-color);
            color: var(--text-main);
            margin: 0;
            display: flex;
            justify-content: center;
            padding: 40px 20px;
        }

        .profile-container {
            max-width: 850px;
            width: 100%;
        }

        /* --- ÜST İLETİŞİM VE BAŞLIK --- */
        .header-section {
            text-align: center;
            border-bottom: 1px solid var(--border-color);
            padding-bottom: 30px;
            margin-bottom: 30px;
        }

        .typewriter h1 {
            overflow: hidden;
            border-right: .15em solid var(--accent-green);
            white-space: nowrap;
            margin: 0 auto;
            letter-spacing: .15em;
            animation: typing 3.5s steps(40, end), blink-caret .75s step-end infinite;
            font-size: 1.8rem;
            color: var(--accent-blue);
        }

        /* İletişim Butonları (Üstte) */
        .contact-badges {
            margin-top: 20px;
            display: flex;
            justify-content: center;
            gap: 15px;
            flex-wrap: wrap;
        }

        .badge {
            display: flex;
            align-items: center;
            padding: 8px 16px;
            background: var(--card-bg);
            border: 1px solid var(--border-color);
            border-radius: 50px;
            text-decoration: none;
            color: var(--text-main);
            font-size: 0.9rem;
            transition: 0.3s;
        }

        .badge:hover {
            border-color: var(--accent-green);
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(57, 211, 83, 0.1);
        }

        .badge i { margin-right: 8px; color: var(--accent-green); }

        /* --- STATS KARTLARI (GITHUB STİLİ) --- */
        .stats-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 15px;
            margin-bottom: 30px;
        }

        .stat-card {
            background: var(--card-bg);
            border: 1px solid var(--border-color);
            border-radius: 10px;
            padding: 15px;
        }

        /* --- AKTİFLİK ÇİZELGESİ (YEŞİLLER ARTIRILDI) --- */
        .activity-box {
            background: var(--card-bg);
            border: 1px solid var(--border-color);
            border-radius: 10px;
            padding: 20px;
            margin-top: 20px;
        }

        .activity-grid {
            display: grid;
            grid-template-columns: repeat(28, 1fr);
            gap: 4px;
        }

        .sq {
            width: 100%;
            aspect-ratio: 1/1;
            border-radius: 2px;
        }

        /* Yeşil Yoğunluğu Sınıfları */
        .v0 { background: #161b22; }
        .v1 { background: #0e4429; }
        .v2 { background: #006d32; }
        .v3 { background: #26a641; }
        .v4 { background: #39d353; }

        /* Beceri İkonları */
        .skills {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-top: 20px;
        }

        .skill-icon {
            padding: 5px 12px;
            background: #1f2937;
            border-radius: 5px;
            font-size: 0.85rem;
            border: 1px solid var(--border-color);
        }

        /* Animasyonlar */
        @keyframes typing { from { width: 0 } to { width: 100% } }
        @keyframes blink-caret { from, to { border-color: transparent } 50% { border-color: var(--accent-green); } }

        @media (max-width: 600px) {
            .stats-grid { grid-template-columns: 1fr; }
            .activity-grid { grid-template-columns: repeat(14, 1fr); }
        }
    </style>
</head>
<body>

<div class="profile-container">
    
    <div class="header-section">
        <div class="typewriter">
            <h1>Merhaba, Ben Bir Geliştiriciyim! 👋</h1>
        </div>
        <p style="color: var(--text-dim); margin-top: 10px;">Python Geliştirici | Veri Analisti | Web Otomasyon Uzmanı</p>
        
        <div class="contact-badges">
            <a href="mailto:kaya150047@gmail.com" class="badge">
                <i class="fas fa-envelope"></i> kaya150047@gmail.com
            </a>
            <a href="#" class="badge">
                <i class="fab fa-github"></i> GitHub
            </a>
            <a href="#" class="badge">
                <i class="fab fa-linkedin"></i> LinkedIn
            </a>
        </div>
    </div>

    <h3 style="font-size: 1.1rem; margin-bottom: 10px;">Kullandığım Teknolojiler</h3>
    <div class="skills">
        <span class="skill-icon"><i class="fab fa-python" style="color:#3776AB"></i> Python</span>
        <span class="skill-icon"><i class="fas fa-eye" style="color:#5C2D91"></i> OpenCV</span>
        <span class="skill-icon"><i class="fab fa-html5" style="color:#E34F26"></i> HTML5</span>
        <span class="skill-icon"><i class="fab fa-css3-alt" style="color:#1572B6"></i> CSS3</span>
        <span class="skill-icon"><i class="fab fa-js" style="color:#F7DF1E"></i> JavaScript</span>
        <span class="skill-icon"><i class="fas fa-robot" style="color:#43B02A"></i> Selenium</span>
    </div>

    <h3 style="font-size: 1.1rem; margin-top: 30px; margin-bottom: 10px;">GitHub İstatistikleri</h3>
    <div class="stats-grid">
        <div class="stat-card">
            <p style="margin:0; color:var(--accent-blue); font-weight:bold;">Top Languages</p>
            <div style="margin-top:10px; height:10px; background:#3776AB; border-radius:5px; width:85%;"></div>
            <p style="font-size:0.8rem; margin-top:5px; color:var(--text-dim);">Python %85, Diğer %15</p>
        </div>
        <div class="stat-card" style="display:flex; flex-direction:column; justify-content:center; align-items:center;">
            <span style="font-size:1.5rem; color:var(--accent-green); font-weight:bold;">500+</span>
            <span style="font-size:0.8rem; color:var(--text-dim);">Toplam Katkı (Yıllık)</span>
        </div>
    </div>

    <h3 style="font-size: 1.1rem; margin-top: 20px; margin-bottom: 5px;">Çalışma Yoğunluğu</h3>
    <div class="activity-box">
        <div class="activity-grid" id="contributions"></div>
        <p style="font-size:0.7rem; color:var(--text-dim); text-align:right; margin-top:10px;">
            Daha az <span class="sq" style="display:inline-block; width:10px; background:#161b22"></span> 
            <span class="sq" style="display:inline-block; width:10px; background:#39d353"></span> Daha çok
        </p>
    </div>

</div>

<script>
    const container = document.getElementById('contributions');
    // Yeşili artırmak için olasılıkları v3 ve v4 (en koyu yeşiller) ağırlıklı yaptık
    const levels = ['v1', 'v2', 'v3', 'v3', 'v3', 'v4', 'v4', 'v4', 'v4', 'v4', 'v0'];

    for (let i = 0; i < 224; i++) { // 28 sütun x 8 satır gibi düşün
        const day = document.createElement('div');
        const randomLevel = levels[Math.floor(Math.random() * levels.length)];
        day.className = 'sq ' + randomLevel;
        container.appendChild(day);
    }
</script>

</body>
</html>
