<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Portfolio Update</title>
    <style>
        :root {
            --bg-color: #0d1117;
            --card-bg: #161b22;
            --text-color: #c9d1d9;
            --green-low: #0e4429;
            --green-medium: #006d32;
            --green-high: #26a641;
            --green-ultra: #39d353;
            --gray-empty: #161b22;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: var(--bg-color);
            color: var(--text-color);
            margin: 0;
            padding: 20px;
        }

        /* --- İletişim Bölümü (Daha Üstte ve Şık) --- */
        .contact-container {
            background: linear-gradient(135deg, #1f2937 0%, #111827 100%);
            padding: 30px;
            border-radius: 15px;
            text-align: center;
            margin-bottom: 40px;
            border: 1px solid #30363d;
            box-shadow: 0 10px 25px rgba(0,0,0,0.3);
        }

        .contact-container h2 {
            margin-top: 0;
            color: #58a6ff;
        }

        .email-box {
            display: inline-block;
            background: #21262d;
            padding: 12px 25px;
            border-radius: 50px;
            border: 1px solid #39d353;
            color: #39d353;
            font-weight: bold;
            text-decoration: none;
            transition: 0.3s;
            font-size: 1.1em;
        }

        .email-box:hover {
            background: #39d353;
            color: #0d1117;
            box-shadow: 0 0 15px rgba(57, 211, 83, 0.4);
        }

        /* --- Aktiflik Çizelgesi (Yeşiller Artırıldı) --- */
        .activity-section {
            background: var(--card-bg);
            padding: 20px;
            border-radius: 10px;
            border: 1px solid #30363d;
        }

        .activity-section h3 {
            margin-bottom: 15px;
            font-size: 0.9em;
            color: #8b949e;
        }

        .grid {
            display: grid;
            grid-template-columns: repeat(20, 1fr); /* 20 sütun görünümü */
            gap: 4px;
        }

        .sq {
            width: 12px;
            height: 12px;
            border-radius: 2px;
        }

        /* Renk Seviyeleri */
        .l0 { background: var(--gray-empty); }
        .l1 { background: var(--green-low); }
        .l2 { background: var(--green-medium); }
        .l3 { background: var(--green-high); }
        .l4 { background: var(--green-ultra); }

    </style>
</head>
<body>

    <section class="contact-container">
        <h2>Benimle İletişime Geçin</h2>
        <p>Projeleriniz veya iş birlikleri için bir e-posta uzağınızdayım.</p>
        <a href="mailto:kaya150047@gmail.com" class="email-box">
            📩 kaya150047@gmail.com
        </a>
    </section>

    <section class="activity-section">
        <h3>Son Katkılar (Katkı Sayısı Artırıldı)</h3>
        <div class="grid" id="activityGrid">
            </div>
    </section>

    <script>
        const grid = document.getElementById('activityGrid');
        // Rastgele yoğun yeşil seçen fonksiyon (L2, L3 ve L4 ağırlıklı)
        const levels = ['l1', 'l2', 'l2', 'l3', 'l3', 'l4', 'l4', 'l4', 'l0']; 
        
        for (let i = 0; i < 140; i++) { // 140 kare (20 hafta)
            const div = document.createElement('div');
            // Rastgele bir seviye ata ama l0 (boş) gelme ihtimalini düşük tut
            const randomLevel = levels[Math.floor(Math.random() * levels.length)];
            div.className = 'sq ' + randomLevel;
            grid.appendChild(div);
        }
    </script>

</body>
</html>
