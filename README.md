<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=no">
  <title>Anindya ✦ 3D Profile</title>
  <!-- Font & Icon -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Quicksand:wght@400;600;700&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
  <style>
    /* Reset & Base */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }
    body {
      font-family: 'Quicksand', sans-serif;
      min-height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      background: linear-gradient(145deg, #fce9f0 0%, #fef6e6 100%);
      padding: 16px;
      margin: 0;
    }
    /* Kartu 3D utama – efek glass + shadow lembut */
    .card-3d {
      max-width: 720px;
      width: 100%;
      background: rgba(255, 245, 240, 0.55);
      backdrop-filter: blur(6px);
      -webkit-backdrop-filter: blur(6px);
      border-radius: 56px 56px 48px 48px;
      padding: 28px 24px 32px;
      box-shadow: 
        0 30px 40px -18px rgba(230, 150, 150, 0.25),
        0 12px 28px -6px rgba(255, 200, 150, 0.2),
        inset 0 0 0 1px rgba(255, 255, 255, 0.6);
      transition: transform 0.25s ease, box-shadow 0.3s ease;
      transform: perspective(1200px) rotateX(2deg) rotateY(-1deg);
      border: 1px solid rgba(255, 220, 200, 0.4);
    }
    .card-3d:hover {
      transform: perspective(1200px) rotateX(1deg) rotateY(1deg) scale(1.01);
      box-shadow: 0 40px 50px -22px rgba(200, 120, 120, 0.3);
    }

    /* ===== ANIMASI KUCING (abu-abu putih) ===== */
    .cat-section {
      display: flex;
      justify-content: center;
      margin-bottom: 12px;
      position: relative;
    }
    .cat-avatar {
      background: rgba(255, 245, 240, 0.3);
      border-radius: 120px;
      padding: 8px 16px 4px 16px;
      backdrop-filter: blur(2px);
      box-shadow: inset 0 0 12px rgba(255, 200, 180, 0.3);
      display: inline-flex;
      align-items: center;
      gap: 6px;
    }
    .cat-icon {
      font-size: 58px;
      line-height: 1;
      display: inline-block;
      animation: floatCat 2.8s infinite alternate ease-in-out;
      filter: drop-shadow(0 8px 12px rgba(120, 80, 80, 0.15));
      color: #8c7a7a;
      transform-origin: center;
    }
    /* kucing abu-abu putih via emoji + gradasi soft */
    .cat-icon i {
      background: linear-gradient(145deg, #d9d0d0, #f0ecec);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      text-shadow: 0 2px 6px rgba(160, 130, 130, 0.2);
      font-size: 64px;
    }
    /* tambahan detail: ekor/gerakan */
    @keyframes floatCat {
      0% { transform: translateY(0px) rotate(-6deg) scale(1); }
      100% { transform: translateY(-10px) rotate(6deg) scale(1.04); }
    }
    .cat-whisker {
      font-size: 20px;
      opacity: 0.5;
      margin: 0 2px;
      color: #b8a0a0;
    }

    /* ===== JUDUL & NAMA ===== */
    .name-title {
      text-align: center;
      margin: 6px 0 2px;
    }
    .name-title h1 {
      font-weight: 700;
      font-size: 2.8rem;
      letter-spacing: 1px;
      background: linear-gradient(135deg, #f7b0b0, #f7d0a0);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
      text-shadow: 0 4px 18px rgba(255, 180, 150, 0.2);
      display: inline-block;
      padding: 0 12px;
      border-radius: 60px;
      backdrop-filter: blur(2px);
    }
    .sub-name {
      font-weight: 600;
      color: #b48a7a;
      background: rgba(255, 235, 220, 0.5);
      backdrop-filter: blur(4px);
      display: inline-block;
      padding: 4px 24px;
      border-radius: 60px;
      font-size: 1rem;
      letter-spacing: 2px;
      border: 1px solid rgba(255, 200, 170, 0.3);
      margin-top: -6px;
    }

    /* ===== INFO GRID (soft pink + kuning) ===== */
    .info-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 12px 14px;
      margin: 22px 0 18px;
    }
    .info-item {
      background: rgba(255, 240, 230, 0.5);
      backdrop-filter: blur(4px);
      border-radius: 34px;
      padding: 10px 12px 10px 18px;
      display: flex;
      align-items: center;
      gap: 8px;
      border: 1px solid rgba(255, 215, 190, 0.5);
      box-shadow: 0 4px 12px rgba(255, 180, 150, 0.08);
      transition: all 0.2s;
    }
    .info-item:hover {
      background: rgba(255, 235, 215, 0.7);
      transform: scale(1.01);
      border-color: #fbc4ab;
    }
    .info-item i {
      font-size: 1.4rem;
      width: 28px;
      color: #e8a78b;
      text-shadow: 0 2px 6px rgba(230, 140, 120, 0.2);
    }
    .info-item .label {
      font-weight: 600;
      color: #986e5e;
      font-size: 0.78rem;
      letter-spacing: 0.5px;
      opacity: 0.7;
      margin-right: 4px;
    }
    .info-item .value {
      font-weight: 600;
      color: #3d2c26;
      font-size: 0.95rem;
      background: rgba(255, 215, 190, 0.2);
      padding: 0 10px 0 6px;
      border-radius: 30px;
      white-space: nowrap;
    }
    .info-item .value strong {
      font-weight: 700;
      color: #b26b5a;
    }

    /* ===== CITA-CITA & HOBI ===== */
    .dream-hobby {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 14px 18px;
      margin: 18px 0 12px;
      background: rgba(255, 235, 210, 0.25);
      backdrop-filter: blur(4px);
      padding: 14px 18px;
      border-radius: 60px;
      border: 1px solid rgba(255, 200, 170, 0.25);
    }
    .dream-hobby span {
      display: flex;
      align-items: center;
      gap: 8px;
      font-weight: 600;
      color: #4d3730;
      font-size: 1rem;
      background: rgba(255, 225, 200, 0.4);
      padding: 4px 18px 4px 14px;
      border-radius: 60px;
      backdrop-filter: blur(2px);
    }
    .dream-hobby i {
      color: #d9947a;
      font-size: 1.2rem;
    }

    /* ===== GAME SECTION ===== */
    .game-section {
      margin: 18px 0 10px;
      background: rgba(255, 235, 215, 0.25);
      backdrop-filter: blur(4px);
      border-radius: 48px;
      padding: 14px 14px 14px 22px;
      display: flex;
      flex-wrap: wrap;
      align-items: center;
      justify-content: space-between;
      border: 1px solid rgba(255, 200, 170, 0.3);
      transition: all 0.25s;
    }
    .game-section:hover {
      background: rgba(255, 230, 205, 0.45);
      border-color: #f5b89e;
    }
    .game-label {
      display: flex;
      align-items: center;
      gap: 10px;
      font-weight: 600;
      color: #7a5a4a;
    }
    .game-label i {
      font-size: 1.8rem;
      color: #e8a78b;
    }
    .game-link {
      background: linear-gradient(135deg, #fdd3c0, #fee0c0);
      padding: 8px 22px 8px 18px;
      border-radius: 60px;
      font-weight: 700;
      font-size: 0.95rem;
      color: #5c3d31;
      text-decoration: none;
      display: inline-flex;
      align-items: center;
      gap: 10px;
      border: 1px solid rgba(255, 180, 150, 0.4);
      box-shadow: 0 4px 12px rgba(230, 150, 120, 0.1);
      transition: 0.2s;
      backdrop-filter: blur(4px);
    }
    .game-link i {
      font-size: 1.2rem;
      color: #b26b5a;
    }
    .game-link:hover {
      background: linear-gradient(135deg, #fcc8b0, #ffdbb8);
      transform: scale(1.02);
      box-shadow: 0 6px 16px rgba(210, 140, 110, 0.25);
      color: #3d2c1e;
    }

    /* ===== LINK PROYEK (tambahan) ===== */
    .project-tag {
      display: flex;
      justify-content: center;
      margin: 12px 0 2px;
    }
    .project-tag a {
      font-size: 0.85rem;
      background: rgba(255, 220, 200, 0.5);
      backdrop-filter: blur(4px);
      padding: 6px 24px;
      border-radius: 60px;
      color: #6d4d3d;
      font-weight: 600;
      text-decoration: none;
      border: 1px solid rgba(255, 190, 160, 0.3);
      display: inline-flex;
      align-items: center;
      gap: 6px;
      letter-spacing: 0.3px;
      transition: 0.2s;
    }
    .project-tag a:hover {
      background: rgba(255, 210, 185, 0.7);
      transform: scale(1.02);
    }

    /* ===== FOOTER KUCING ===== */
    .cat-footer {
      text-align: center;
      margin-top: 14px;
      font-size: 0.75rem;
      color: #b0887a;
      letter-spacing: 1px;
      display: flex;
      justify-content: center;
      gap: 10px;
      flex-wrap: wrap;
      opacity: 0.7;
    }

    /* Responsive */
    @media (max-width: 500px) {
      .card-3d { padding: 20px 14px; border-radius: 40px; }
      .name-title h1 { font-size: 2.2rem; }
      .info-grid { grid-template-columns: 1fr; gap: 8px; }
      .info-item { padding: 8px 12px; }
      .game-section { flex-direction: column; align-items: flex-start; gap: 12px; }
      .dream-hobby span { font-size: 0.9rem; padding: 2px 14px; }
      .cat-icon i { font-size: 48px; }
    }
  </style>
</head>
<body>
  <div class="card-3d">

    <!-- ANIMASI KUCING ABU-ABU PUTIH -->
    <div class="cat-section">
      <div class="cat-avatar">
        <span class="cat-whisker"><i class="fas fa-arrow-left"></i></span>
        <span class="cat-icon">
          <i class="fas fa-cat"></i> 
        </span>
        <span class="cat-whisker"><i class="fas fa-arrow-right"></i></span>
        <span style="font-size: 20px; margin-left: 4px; color: #b8a0a0;">🐾</span>
      </div>
    </div>

    <!-- NAMA & SUB -->
    <div class="name-title">
      <h1>✦ Anindya ✦</h1>
      <div class="sub-name">🐈 𝘴𝘢𝘺𝘢 𝘴𝘶𝘬𝘢 𝘬𝘶𝘤𝘪𝘯𝘨</div>
    </div>

    <!-- INFO GRID: lahir, umur, bulan, dll -->
    <div class="info-grid">
      <div class="info-item">
        <i class="fas fa-map-pin"></i>
        <span class="label">Lahir</span>
        <span class="value"><strong>Jakarta</strong></span>
      </div>
      <div class="info-item">
        <i class="fas fa-cake-candles"></i>
        <span class="label">Umur</span>
        <span class="value">16 tahun</span>
      </div>
      <div class="info-item">
        <i class="fas fa-calendar-alt"></i>
        <span class="label">Bulan</span>
        <span class="value">Desember</span>
      </div>
      <div class="info-item">
        <i class="fas fa-heart"></i>
        <span class="label">Hewan fav</span>
        <span class="value">🐱 Kucing</span>
      </div>
    </div>

    <!-- CITA-CITA & HOBI (plus main kucing) -->
    <div class="dream-hobby">
      <span><i class="fas fa-stethoscope"></i> Cita-cita: Dokter</span>
      <span><i class="fas fa-paw"></i> Hobi: main kucing</span>
      <span><i class="fas fa-cat"></i> fav: Kucing abu-putih</span>
    </div>

    <!-- GAME + LINK (proyek game) -->
    <div class="game-section">
      <div class="game-label">
        <i class="fas fa-gamepad"></i>
        <span>Proyek Game</span>
      </div>
      <a href="https://anindyaimutsukakucing.github.io/game-sky-warior/" target="_blank" class="game-link">
        <i class="fas fa-rocket"></i> Sky Warior
        <i class="fas fa-arrow-right" style="font-size: 0.9rem;"></i>
      </a>
    </div>

    <!-- link tambahan (projek game) -->
    <div class="project-tag">
      <a href="https://anindyaimutsukakucing.github.io/game-sky-warior/" target="_blank">
        <i class="fas fa-code"></i> github.io/game-sky-warior
      </a>
    </div>

    <!-- footer imut -->
    <div class="cat-footer">
      <span><i class="fas fa-paw" style="color:#d9947a;"></i> anindya · 16 · desember</span>
      <span>🐈⬛ kucing abu-putih</span>
      <span><i class="fas fa-cat"></i> ˚ ༘ ೀ</span>
    </div>

  </div>
  <!-- tambahan efek 3d elemen (opsional) -->
</body>
</html>
