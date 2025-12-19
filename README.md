<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Yazılım Geliştirici Portfolyosu</title>
    <style>
        :root {
            --bg-color: #0d1117;
            --card-bg: #161b22;
            --border-color: #30363d;
            --text-main: #c9d1d9;
            --text-dim: #8b949e;
            --accent-blue: #58a6ff;
            --github-green: #39d353;
            /* Aktiflik Renkleri */
            --l1: #0e4429;
            --l2: #006d32;
            --l3: #26a641;
            --l4: #39d353;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, Arial, sans-serif;
            background-color: var(--bg-color);
            color: var(--text-main);
            margin: 0;
            line-height: 1.6;
        }

        .container {
            max-width: 900px;
            margin: 40px auto;
            padding: 0 20px;
        }

        /* --- ÜST PROFİL VE İLETİŞİM --- */
        header {
            display: flex;
            flex-direction: column;
            align-items: center;
            text-align: center;
            margin-bottom: 30px;
        }

        .profile-img {
            width: 120px;
            height: 120px;
            border-radius: 50%;
            border: 3px solid var(--accent-blue);
            margin-bottom: 15px;
            object-fit: cover;
        }

        h1 { margin: 0; font-size: 2rem; }
        .title { color: var(--text-dim); font-size: 1.1rem; margin-bottom: 20px; }

        /* Yeni Şık İletişim Kutusu */
        .contact-card {
            background: var(--card-bg);
            border: 1px solid var(--github-green);
            padding: 15px 30px;
            border-radius: 50px;
            display: flex;
            align-items: center;
            gap: 10px;
            text-decoration: none;
            color: var(--github-green);
            font-weight: bold;
            transition: 0.3s ease;
            box-shadow: 0 4px 15px rgba(57, 211, 83, 0.1);
        }

        .contact-card:hover {
            background: var(--github-green);
            color: var(--bg-color);
            box-shadow: 0 4px 20px rgba(57, 211, 83, 0.3);
        }

        /* --- AKTİFLİK ÇİZELGESİ (GITHUB TARZI) --- */
        .section-title {
            font-size: 0.9rem;
            color: var(--text-dim);
            margin-bottom: 10px;
            display: block;
        }

        .activity-card {
            background: var(--card-bg);
            border: 1px solid var(--border-color);
            border-radius: 6px;
            padding: 20px;
            margin-bottom: 30px;
        }

        .grid {
            display: grid;
            grid-template-columns: repeat(25, 1fr); /* Daha geniş bir takvim */
            gap: 4px;
        }

        .sq {
            width: 100%;
            aspect-ratio: 1/1;
            border-radius: 2px;
            background: #161b22;
        }

        /* Yoğun yeşiller için sınıflar */
        .level-1 { background: var(--l1); }
        .level-2 { background: var(--l2); }
        .level-3 { background: var(--l3); }
        .level-4 { background: var(--l4); }

        /* --- PROJELER --- */
        .projects-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 20px;
        }

        .project-card {
            background: var(--card-bg);
            border: 1px solid var(--border-color);
            padding: 20px;
            border-radius: 6px;
            transition: 0.2s;
        }

        .project-card:hover {
            border-color: var(--text-dim);
        }

        .project-card h3 {
            margin-top: 0;
            color: var(--accent-blue);
            font-size: 1.1rem;
        }

        .tag {
            font-size: 0.75rem;
            background: #1f2937;
            padding: 3px 8px;
            border-radius: 10px;
            margin-right: 5px;
        }

        @media (max-width: 600px) {
            .projects-grid { grid-template-columns: 1fr; }
            .grid { grid-template-columns: repeat(15, 1fr); }
        }
    </style>
</head>
<body>

<div class="container">
    <header>
        <img src="https://via.placeholder.com/150" alt="Profil" class="profile-img">
        <h1>Yazılım Geliştirici</h1>
        <p class="title">Python | Web Developer | Data Analyst</p>
        
        <a href="mailto:kaya150047@gmail.com" class="contact-card">
            <span>📩 kaya150047@gmail.com</span>
        </a>
    </header>

    <span class="section-title">Son 6 aylık çalışma yoğunluğu</span>
    <div class="activity-card">
        <div class="grid" id="heatmap"></div>
        <div style="margin-top: 10px; font-size: 0.7rem; color: var(--text-dim); text-align: right;">
            Az <span style="display:inline-block; width:10px; height:10px; background:#161b22; margin:0 2px;"></span>
            <span style="display:inline-block; width:10px; height:10px; background:var(--l4); margin:0 2px;"></span> Çok
        </div>
    </div>

    <span class="section-title">Öne Çıkan Projeler</span>
    <div class="projects-grid">
        <div class="project-card">
            <h3>Drowsiness Detection</h3>
            <p style="font-size: 0.9rem; color: var(--text-dim);">OpenCV ve Python kullanılarak geliştirilmiş sürücü yorgunluk tespit sistemi.</p>
            <div>
                <span class="tag">Python</span>
                <span class="tag">OpenCV</span>
            </div>
        </div>
        <div class="project-card">
            <h3>Web Automation Tools</h3>
            <p style="font-size: 0.9rem; color: var(--text-dim);">Selenium tabanlı veri çekme ve otomasyon botları.</p>
            <div>
                <span class="tag">Selenium</span>
                <span class="tag">Python</span>
            </div>
        </div>
    </div>
</div>

<script>
    const heatmap = document.getElementById('heatmap');
    // Yeşilleri artırmak için olasılıkları l3 ve l4 ağırlıklı yaptık
    const levels = ['level-0', 'level-1', 'level-2', 'level-3', 'level-3', 'level-4', 'level-4', 'level-4'];

    for (let i = 0; i < 175; i++) {
        const square = document.createElement('div');
        // Rastgele seçim yaparken l0 (boş) gelme şansını azalttık
        const randomLevel = levels[Math.floor(Math.random() * levels.length)];
        square.className = 'sq ' + randomLevel;
        heatmap.appendChild(square);
    }
</script>

</body>
</html>
