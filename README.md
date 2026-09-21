<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SHOP ACC FC ONLINE NGỌC HÀO - BẢO MẬT XÁC NHẬN CHUYỂN KHOẢN TỰ ĐỘNG</title>
    <!-- FontAwesome 6 Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- Google Fonts for Gaming Theme -->
    <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@500;700;900&family=Rajdhani:wght@600;700&family=Roboto:wght@400;500;700;900&display=swap" rel="stylesheet">
    
    <style>
        :root {
            --bg-main: #050811;
            --bg-card: rgba(18, 26, 45, 0.85);
            --bg-modal: #0d1322;
            --primary-neon: #00e676;
            --primary-glow: rgba(0, 230, 118, 0.4);
            --accent-gold: #ffd700;
            --accent-blue: #00b0ff;
            --accent-purple: #9d4edd;
            --accent-red: #ff2d55;
            --text-light: #f8fafc;
            --text-dim: #94a3b8;
            --border-color: rgba(51, 65, 85, 0.7);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Roboto', sans-serif;
            user-select: none;
        }

        body {
            background-color: var(--bg-main);
            color: var(--text-light);
            overflow-x: hidden;
            position: relative;
            min-height: 100vh;
        }

        /* Canvas Particle Background */
        #bgCanvas {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: 0;
            pointer-events: none;
        }

        .container {
            max-width: 1240px;
            margin: 0 auto;
            padding: 0 15px;
            position: relative;
            z-index: 1;
        }

        header {
            background: rgba(10, 15, 29, 0.9);
            position: sticky;
            top: 0;
            z-index: 100;
            border-bottom: 2px solid var(--primary-neon);
            box-shadow: 0 0 15px var(--primary-glow);
            backdrop-filter: blur(12px);
        }

        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 12px 0;
        }

        .glitch-logo {
            font-family: 'Orbitron', sans-serif;
            font-size: 22px;
            font-weight: 900;
            color: #fff;
            position: relative;
            text-decoration: none;
            letter-spacing: 1px;
            text-shadow: 0 0 10px var(--primary-neon);
            cursor: pointer;
        }

        .glitch-logo::before, .glitch-logo::after {
            content: 'NGỌC HÀO FC ONLINE';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            opacity: 0.8;
        }

        .glitch-logo::before {
            left: 2px;
            text-shadow: -2px 0 #ff0055;
            clip: rect(24px, 550px, 90px, 0);
            animation: glitch-anim 2.5s infinite linear alternate-reverse;
        }

        .glitch-logo::after {
            left: -2px;
            text-shadow: -2px 0 #00e5ff;
            clip: rect(85px, 550px, 140px, 0);
            animation: glitch-anim2 2.5s infinite linear alternate-reverse;
        }

        @keyframes glitch-anim {
            0% { clip: rect(12px, 9999px, 52px, 0); }
            20% { clip: rect(42px, 9999px, 12px, 0); }
            40% { clip: rect(25px, 9999px, 80px, 0); }
            60% { clip: rect(60px, 9999px, 30px, 0); }
            80% { clip: rect(10px, 9999px, 90px, 0); }
            100% { clip: rect(50px, 9999px, 20px, 0); }
        }

        @keyframes glitch-anim2 {
            0% { clip: rect(65px, 9999px, 100px, 0); }
            20% { clip: rect(10px, 9999px, 40px, 0); }
            40% { clip: rect(80px, 9999px, 20px, 0); }
            60% { clip: rect(30px, 9999px, 70px, 0); }
            80% { clip: rect(90px, 9999px, 10px, 0); }
            100% { clip: rect(15px, 9999px, 60px, 0); }
        }

        .nav-menu {
            display: flex;
            gap: 20px;
            list-style: none;
            align-items: center;
        }

        .nav-link {
            color: var(--text-light);
            text-decoration: none;
            font-family: 'Rajdhani', sans-serif;
            font-weight: 700;
            font-size: 16px;
            text-transform: uppercase;
            transition: 0.3s;
            display: flex;
            align-items: center;
            gap: 6px;
        }

        .nav-link:hover {
            color: var(--primary-neon);
            text-shadow: 0 0 8px var(--primary-neon);
        }

        .admin-nav-btn {
            background: rgba(255, 215, 0, 0.15);
            border: 1px solid var(--accent-gold);
            color: var(--accent-gold);
            padding: 6px 14px;
            border-radius: 8px;
            cursor: pointer;
            font-family: 'Rajdhani', sans-serif;
            font-weight: 700;
            font-size: 14px;
            transition: 0.3s;
            display: flex;
            align-items: center;
            gap: 6px;
        }

        .admin-nav-btn:hover {
            background: var(--accent-gold);
            color: #000;
            box-shadow: 0 0 12px rgba(255, 215, 0, 0.4);
        }

        .hero-banner {
            text-align: center;
            padding: 35px 0 20px;
        }

        .hero-title {
            font-family: 'Orbitron', sans-serif;
            font-size: 30px;
            font-weight: 900;
            background: linear-gradient(180deg, #ffffff 0%, #00e676 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            margin-bottom: 10px;
            text-transform: uppercase;
        }

        .ticker-bar {
            background: rgba(0, 230, 118, 0.1);
            border: 1px solid var(--primary-neon);
            border-radius: 50px;
            padding: 8px 20px;
            display: inline-flex;
            align-items: center;
            gap: 10px;
            font-size: 14px;
            color: var(--accent-gold);
            font-weight: 700;
        }

        .bp-rate-section {
            background: var(--bg-card);
            border: 1px solid var(--primary-neon);
            border-radius: 16px;
            padding: 22px;
            margin: 25px 0;
            box-shadow: 0 0 25px rgba(0, 230, 118, 0.15);
            backdrop-filter: blur(10px);
        }

        .sec-title {
            font-family: 'Orbitron', sans-serif;
            font-size: 20px;
            color: var(--text-light);
            margin-bottom: 15px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .sec-title i {
            color: var(--primary-neon);
        }

        .bp-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(190px, 1fr));
            gap: 15px;
        }

        .bp-card {
            background: rgba(10, 16, 30, 0.8);
            border: 1px solid var(--border-color);
            border-radius: 12px;
            padding: 15px 10px;
            text-align: center;
            position: relative;
            transition: all 0.3s ease;
            overflow: hidden;
        }

        .bp-card:hover {
            border-color: var(--primary-neon);
            transform: translateY(-5px);
            box-shadow: 0 8px 20px var(--primary-glow);
        }

        .bp-icon-animated {
            width: 55px;
            height: 55px;
            object-fit: contain;
            filter: drop-shadow(0 0 10px var(--primary-neon));
            animation: floatBP 3s infinite ease-in-out;
        }

        @keyframes floatBP {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-6px); }
        }

        .bp-amount {
            font-family: 'Orbitron', sans-serif;
            font-size: 17px;
            font-weight: 900;
            color: var(--accent-gold);
            margin: 8px 0 2px;
            display: block;
        }

        .bp-price {
            font-size: 16px;
            font-weight: 800;
            color: var(--primary-neon);
        }

        .filter-bar {
            display: flex;
            gap: 12px;
            flex-wrap: wrap;
            margin-bottom: 25px;
            background: var(--bg-card);
            padding: 12px 18px;
            border-radius: 12px;
            border: 1px solid var(--border-color);
            align-items: center;
        }

        .filter-btn {
            background: #0d1527;
            color: var(--text-dim);
            border: 1px solid var(--border-color);
            padding: 8px 18px;
            border-radius: 8px;
            cursor: pointer;
            font-family: 'Rajdhani', sans-serif;
            font-weight: 700;
            font-size: 15px;
            transition: 0.3s;
        }

        .filter-btn.active, .filter-btn:hover {
            background: var(--primary-neon);
            color: #000;
            border-color: var(--primary-neon);
            box-shadow: 0 0 12px var(--primary-glow);
        }

        .product-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 22px;
            margin-bottom: 50px;
        }

        .product-card {
            background: var(--bg-card);
            border: 1px solid var(--border-color);
            border-radius: 16px;
            overflow: hidden;
            transition: all 0.35s cubic-bezier(0.175, 0.885, 0.32, 1.275);
            display: flex;
            flex-direction: column;
            position: relative;
        }

        .product-card:hover {
            border-color: var(--primary-neon);
            transform: translateY(-8px);
            box-shadow: 0 12px 30px rgba(0, 230, 118, 0.25);
        }

        .card-thumb {
            height: 160px;
            background: radial-gradient(circle at center, #1e293b 0%, #0a0f1d 100%);
            position: relative;
            display: flex;
            align-items: center;
            justify-content: center;
            overflow: hidden;
            border-bottom: 1px solid var(--border-color);
        }

        .card-gif-preview {
            width: 100%;
            height: 100%;
            object-fit: cover;
            opacity: 0.85;
            transition: transform 0.5s ease;
        }

        .product-card:hover .card-gif-preview {
            transform: scale(1.08);
            opacity: 1;
        }

        .bp-badge-overlay {
            position: absolute;
            bottom: 10px;
            left: 50%;
            transform: translateX(-50%);
            background: rgba(0, 0, 0, 0.85);
            border: 1px solid var(--accent-gold);
            color: var(--accent-gold);
            padding: 4px 14px;
            border-radius: 20px;
            font-family: 'Orbitron', sans-serif;
            font-size: 13px;
            font-weight: 900;
            white-space: nowrap;
            box-shadow: 0 0 10px rgba(255, 215, 0, 0.4);
        }

        .card-body {
            padding: 16px;
            flex-grow: 1;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
        }

        .card-title {
            font-family: 'Rajdhani', sans-serif;
            font-size: 18px;
            font-weight: 700;
            color: #fff;
            margin-bottom: 12px;
        }

        .specs-list {
            list-style: none;
            margin-bottom: 16px;
            font-size: 13px;
        }

        .specs-list li {
            display: flex;
            justify-content: space-between;
            padding: 5px 0;
            border-bottom: 1px dashed rgba(255, 255, 255, 0.1);
            color: var(--text-dim);
        }

        .specs-list li strong {
            color: #fff;
        }

        .price-tag {
            font-family: 'Orbitron', sans-serif;
            font-size: 19px;
            font-weight: 900;
            color: var(--primary-neon);
            text-shadow: 0 0 8px var(--primary-glow);
        }

        .card-actions {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 10px;
            margin-top: 10px;
        }

        @keyframes btnShake {
            0%, 100% { transform: translate(0, 0) rotate(0deg); }
            15% { transform: translate(-3px, 2px) rotate(-1deg); }
            30% { transform: translate(3px, -2px) rotate(1deg); }
            45% { transform: translate(-2px, -1px) rotate(0deg); }
            60% { transform: translate(2px, 1px) rotate(1deg); }
            75% { transform: translate(-1px, 2px) rotate(-1deg); }
        }

        .btn-shake {
            animation: btnShake 2s infinite ease-in-out;
        }

        .btn-view {
            background: linear-gradient(135deg, #1e293b, #0f172a);
            color: var(--accent-blue);
            border: 1px solid var(--accent-blue);
            padding: 9px 0;
            border-radius: 8px;
            font-family: 'Rajdhani', sans-serif;
            font-weight: 700;
            font-size: 14px;
            cursor: pointer;
            transition: 0.3s;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 6px;
        }

        .btn-view:hover {
            background: var(--accent-blue);
            color: #000;
            box-shadow: 0 0 12px var(--accent-blue);
        }

        .btn-buy {
            background: linear-gradient(135deg, var(--primary-neon), #00b0ff);
            color: #000;
            border: none;
            padding: 9px 0;
            border-radius: 8px;
            font-family: 'Orbitron', sans-serif;
            font-weight: 900;
            font-size: 13px;
            cursor: pointer;
            transition: 0.3s;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 6px;
        }

        .btn-buy:hover {
            filter: brightness(1.25);
            box-shadow: 0 0 18px var(--primary-neon);
        }

        .modal-wrapper {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(3, 7, 18, 0.88);
            backdrop-filter: blur(8px);
            display: none;
            justify-content: center;
            align-items: center;
            z-index: 1000;
            padding: 15px;
        }

        .modal-box {
            background: var(--bg-modal);
            border: 2px solid var(--primary-neon);
            border-radius: 20px;
            width: 100%;
            max-width: 780px;
            max-height: 90vh;
            overflow-y: auto;
            position: relative;
            box-shadow: 0 0 35px var(--primary-glow);
            animation: modalPop 0.3s cubic-bezier(0.175, 0.885, 0.32, 1.275);
        }

        @keyframes modalPop {
            from { transform: scale(0.85); opacity: 0; }
            to { transform: scale(1); opacity: 1; }
        }

        .modal-close-btn {
            position: absolute;
            top: 15px;
            right: 18px;
            background: rgba(255, 255, 255, 0.1);
            border: none;
            color: #fff;
            width: 36px;
            height: 36px;
            border-radius: 50%;
            font-size: 18px;
            cursor: pointer;
            transition: 0.3s;
            z-index: 10;
        }

        .modal-close-btn:hover {
            background: var(--accent-red);
            transform: rotate(90deg);
        }

        .modal-header-info {
            padding: 20px 25px 10px;
            border-bottom: 1px solid var(--border-color);
        }

        .modal-acc-code {
            font-family: 'Orbitron', sans-serif;
            font-size: 22px;
            color: var(--accent-gold);
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .modal-tabs {
            display: flex;
            gap: 8px;
            padding: 15px 25px 0;
            border-bottom: 1px solid var(--border-color);
            background: rgba(0, 0, 0, 0.2);
            overflow-x: auto;
        }

        .tab-btn {
            background: transparent;
            color: var(--text-dim);
            border: none;
            border-bottom: 3px solid transparent;
            padding: 10px 18px;
            font-family: 'Rajdhani', sans-serif;
            font-weight: 700;
            font-size: 16px;
            cursor: pointer;
            transition: 0.3s;
            white-space: nowrap;
        }

        .tab-btn.active {
            color: var(--primary-neon);
            border-bottom-color: var(--primary-neon);
        }

        .tab-content {
            padding: 20px 25px;
            display: none;
        }

        .tab-content.active {
            display: block;
        }

        .gif-showcase-box {
            width: 100%;
            height: 320px;
            background: #000;
            border-radius: 12px;
            overflow: hidden;
            position: relative;
            border: 1px solid var(--accent-blue);
            box-shadow: inset 0 0 20px rgba(0, 176, 255, 0.3);
        }

        .gif-showcase-img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .hologram-effect {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, rgba(255,255,255,0.1) 0%, rgba(255,255,255,0) 50%, rgba(0,230,118,0.1) 100%);
            pointer-events: none;
        }

        .squad-player-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(130px, 1fr));
            gap: 10px;
            margin-top: 15px;
        }

        .player-badge-card {
            background: rgba(15, 23, 42, 0.9);
            border: 1px solid var(--border-color);
            border-radius: 8px;
            padding: 8px;
            text-align: center;
        }

        .player-badge-card img {
            width: 45px;
            height: 45px;
            border-radius: 50%;
            margin-bottom: 5px;
        }

        .p-name {
            font-size: 12px;
            font-weight: 700;
            color: #fff;
            display: block;
        }

        .p-stat {
            font-size: 11px;
            color: var(--accent-gold);
            font-weight: 900;
        }

        .qr-card-box {
            text-align: center;
            background: #060a12;
            padding: 20px;
            border-radius: 14px;
            border: 1px solid var(--primary-neon);
        }

        .qr-img {
            width: 220px;
            height: 220px;
            border-radius: 12px;
            border: 3px solid #fff;
            margin: 15px 0;
            box-shadow: 0 0 20px rgba(255, 255, 255, 0.2);
        }

        .bank-info-table {
            width: 100%;
            margin-top: 15px;
            text-align: left;
            font-size: 14px;
            border-collapse: collapse;
        }

        .bank-info-table td {
            padding: 8px 12px;
            border-bottom: 1px dashed var(--border-color);
        }

        .bank-info-table td:first-child {
            color: var(--text-dim);
            width: 40%;
        }

        .bank-info-table td:last-child {
            color: #fff;
            font-weight: 700;
        }

        .copy-btn {
            background: var(--accent-blue);
            color: #000;
            border: none;
            padding: 3px 8px;
            border-radius: 4px;
            cursor: pointer;
            font-size: 11px;
            margin-left: 8px;
            font-weight: 900;
        }

        .verify-box {
            background: rgba(255, 215, 0, 0.08);
            border: 1px dashed var(--accent-gold);
            padding: 15px;
            border-radius: 10px;
            margin-top: 15px;
            text-align: left;
        }

        .verify-input {
            width: 100%;
            background: #030710;
            border: 1px solid var(--border-color);
            padding: 10px 14px;
            border-radius: 6px;
            color: #fff;
            font-size: 14px;
            margin-top: 8px;
            font-family: 'Rajdhani', sans-serif;
            font-weight: 700;
        }

        .verify-input:focus {
            border-color: var(--primary-neon);
            outline: none;
        }

        .toast {
            position: fixed;
            bottom: 25px;
            right: 25px;
            background: var(--primary-neon);
            color: #000;
            padding: 12px 22px;
            border-radius: 8px;
            font-weight: 900;
            font-family: 'Rajdhani', sans-serif;
            font-size: 16px;
            box-shadow: 0 5px 20px rgba(0,230,118,0.5);
            display: none;
            z-index: 3000;
        }

        /* Admin Dashboard Styles */
        .admin-table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 15px;
            font-size: 13px;
        }

        .admin-table th, .admin-table td {
            padding: 10px 12px;
            border: 1px solid var(--border-color);
            text-align: left;
        }

        .admin-table th {
            background: #111c33;
            color: var(--accent-gold);
            font-family: 'Orbitron', sans-serif;
            font-size: 12px;
        }

        .admin-approve-btn {
            background: var(--primary-neon);
            color: #000;
            border: none;
            padding: 5px 12px;
            border-radius: 4px;
            cursor: pointer;
            font-weight: 900;
            font-size: 12px;
        }

        .admin-approve-btn:hover {
            filter: brightness(1.2);
        }

        .user-create-acc-bar {
            background: linear-gradient(135deg, rgba(0, 230, 118, 0.15), rgba(0, 176, 255, 0.15));
            border: 2px dashed var(--primary-neon);
            border-radius: 16px;
            padding: 20px;
            margin: 25px 0;
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            gap: 15px;
        }

        footer {
            background: #030710;
            border-top: 1px solid var(--border-color);
            padding: 35px 0;
            text-align: center;
            color: var(--text-dim);
            font-size: 14px;
            margin-top: 40px;
        }

        @media (max-width: 768px) {
            .hero-title { font-size: 22px; }
            .card-actions { grid-template-columns: 1fr; }
            .modal-tabs { padding: 10px 15px 0; }
            .gif-showcase-box { height: 210px; }
        }
    </style>
</head>
<body>

    <!-- Interactive Background Canvas -->
    <canvas id="bgCanvas"></canvas>

    <!-- Navigation Header -->
    <header>
        <div class="container navbar">
            <a href="#" class="glitch-logo" id="shopLogo">NGỌC HÀO FC ONLINE</a>
            <ul class="nav-menu">
                <li><a href="#bang-gia" class="nav-link"><i class="fa-solid fa-coins"></i> Bảng Giá</a></li>
                <li><a href="#danh-sach" class="nav-link"><i class="fa-solid fa-gamepad"></i> Kho Acc</a></li>
                <li><a href="https://zalo.me/0961599740" target="_blank" class="nav-link" style="color: var(--accent-blue);"><i class="fa-solid fa-comments"></i> Zalo Admin</a></li>
                <li>
                    <button class="admin-nav-btn" onclick="openUserCreateModal()" style="border-color: var(--primary-neon); color: var(--primary-neon); background: rgba(0,230,118,0.1);">
                        <i class="fa-solid fa-plus-circle"></i> Đăng Ký Bán Acc
                    </button>
                </li>
            </ul>
        </div>
    </header>

    <!-- Hero Banner -->
    <section class="hero-banner">
        <div class="container">
            <h1 class="hero-title">SHOP ACC FC ONLINE NGỌC HÀO</h1>
            <div class="ticker-bar">
                <i class="fa-solid fa-shield-cat"></i>
                <span>BẢO MẬT TUYỆT ĐỐI: CHỈ XÁC NHẬN CHUYỂN KHOẢN THÀNH CÔNG MỚI HIỆN MẬT KHẨU</span>
            </div>
        </div>
    </section>

    <main class="container">
        <!-- Bảng Giá Quy Đổi BP -->
        <section class="bp-rate-section" id="bang-gia">
            <h2 class="sec-title"><i class="fa-solid fa-fire"></i> BẢNG GIÁ QUY ĐỔI BP TỰ DO BUILD TEAM</h2>
            <div class="bp-grid">
                <div class="bp-card">
                    <img src="https://cdn-icons-png.flaticon.com/512/217/217853.png" alt="BP 5B" class="bp-icon-animated">
                    <span class="bp-amount">5.000 TỶ BP</span>
                    <span class="bp-price">150.000đ</span>
                </div>
                <div class="bp-card">
                    <img src="https://cdn-icons-png.flaticon.com/512/217/217853.png" alt="BP 8B" class="bp-icon-animated">
                    <span class="bp-amount">8.000 TỶ BP</span>
                    <span class="bp-price">400.000đ</span>
                </div>
                <div class="bp-card" style="border-color: var(--accent-gold);">
                    <span style="position: absolute; top:0; right:0; background: var(--accent-red); color:#fff; font-size:9px; font-weight:900; padding: 2px 8px; border-radius:0 0 0 8px;">SIÊU HOT</span>
                    <img src="https://cdn-icons-png.flaticon.com/512/217/217853.png" alt="BP 10B" class="bp-icon-animated">
                    <span class="bp-amount" style="color: var(--primary-neon);">10.000 TỶ BP</span>
                    <span class="bp-price">600.000đ</span>
                </div>
                <div class="bp-card">
                    <img src="https://cdn-icons-png.flaticon.com/512/217/217853.png" alt="BP 15B" class="bp-icon-animated">
                    <span class="bp-amount">15.000 TỶ BP</span>
                    <span class="bp-price">900.000đ</span>
                </div>
                <div class="bp-card">
                    <img src="https://cdn-icons-png.flaticon.com/512/217/217853.png" alt="BP 20B" class="bp-icon-animated">
                    <span class="bp-amount">20.000 TỶ BP</span>
                    <span class="bp-price">1.200.000đ</span>
                </div>
            </div>
        </section>

        <!-- Danh Sách Acc -->
        <section id="danh-sach">
            <h2 class="sec-title"><i class="fa-solid fa-store"></i> DANH SÁCH TÀI KHOẢN MỚI CẬP NHẬT</h2>

            <!-- Thanh Đăng Ký Acc Cho Người Xem -->
            <div class="user-create-acc-bar">
                <div>
                    <h3 style="font-family: 'Orbitron', sans-serif; color: var(--accent-gold); font-size: 16px;">
                        <i class="fa-solid fa-wand-magic-sparkles"></i> BẠN CÓ ACC FC ONLINE / BP MUỐN KÝ GỬI HOẶC BÁN?
                    </h3>
                    <p style="font-size: 13px; color: var(--text-dim); margin-top: 4px;">
                        Tạo acc ngay lên hệ thống để người xem khác có thể giao dịch qua cơ chế duyệt chuyển khoản bảo mật của Shop Ngọc Hào!
                    </p>
                </div>
                <button class="btn-buy btn-shake" onclick="openUserCreateModal()" style="padding: 10px 20px;">
                    <i class="fa-solid fa-circle-plus"></i> TẠO ACC CHO NGƯỜI XEM NGAY
                </button>
            </div>

            <!-- Bộ Lọc -->
            <div class="filter-bar">
                <span style="font-weight: 700; color: var(--text-dim);">Lọc Mức Giá:</span>
                <button class="filter-btn active" onclick="applyFilter('all', this)">Tất Cả</button>
                <button class="filter-btn" onclick="applyFilter('under500', this)">Dưới 500k</button>
                <button class="filter-btn" onclick="applyFilter('500to1000', this)">500k - 1 Triệu</button>
                <button class="filter-btn" onclick="applyFilter('over1000', this)">Trên 1 Triệu</button>
            </div>

            <!-- Products Grid -->
            <div class="product-grid" id="productGrid">
                <!-- Rendered dynamically -->
            </div>
        </section>
    </main>

    <!-- MODAL 1: XEM CHI TIẾT SQUAD -->
    <div class="modal-wrapper" id="accDetailModal">
        <div class="modal-box">
            <button class="modal-close-btn" onclick="closeModal('accDetailModal')"><i class="fa-solid fa-xmark"></i></button>
            
            <div class="modal-header-info">
                <div class="modal-acc-code" id="modalAccCode"><i class="fa-solid fa-shield-halved"></i> ACC FC ONLINE - MS806</div>
                <p style="color: var(--text-dim); font-size: 13px; margin-top: 4px;">Trắng thông tin 100% • Hỗ trợ đổi SĐT / Email chính chủ lập tức</p>
            </div>

            <div class="modal-tabs">
                <button class="tab-btn active" onclick="switchTab('tab-gif', this)"><i class="fa-solid fa-film"></i> Ảnh Động Squad (GIF)</button>
                <button class="tab-btn" onclick="switchTab('tab-info', this)"><i class="fa-solid fa-circle-info"></i> Thông Tin Đội Hình</button>
                <button class="tab-btn" onclick="switchTab('tab-items', this)"><i class="fa-solid fa-box-open"></i> Kho Vật Phẩm VIP</button>
            </div>

            <div class="tab-content active" id="tab-gif">
                <div class="gif-showcase-box">
                    <img id="detailGifImg" src="" alt="Animated Squad Preview" class="gif-showcase-img">
                    <div class="hologram-effect"></div>
                </div>
                <p style="font-size: 12px; color: var(--accent-gold); margin-top: 10px; text-align: center;">
                    <i class="fa-solid fa-wand-magic-sparkles"></i> Xem trước cầu thủ & giá trị BP trước khi thanh toán
                </p>
                <div class="squad-player-grid" id="modalPlayerList"></div>
            </div>

            <div class="tab-content" id="tab-info">
                <table class="bank-info-table">
                    <tr>
                        <td>Giá trị tài khoản (BP):</td>
                        <td id="detailBpVal" style="color: var(--accent-gold);">5.000 Tỷ BP</td>
                    </tr>
                    <tr>
                        <td>Giá bán khuyến mãi:</td>
                        <td id="detailPriceVal" style="color: var(--primary-neon); font-size: 18px; font-weight: 900;">150.000đ</td>
                    </tr>
                    <tr>
                        <td>Cấp độ VIP HLV:</td>
                        <td>Đẳng Cấp Huyền Thoại V</td>
                    </tr>
                    <tr>
                        <td>Tình trạng Thông Tin:</td>
                        <td style="color: var(--primary-neon);"><i class="fa-solid fa-check-double"></i> Trắng 100%</td>
                    </tr>
                </table>
            </div>

            <div class="tab-content" id="tab-items">
                <ul class="specs-list" style="font-size: 14px;">
                    <li><span>Phiếu Giảm Giá Thuế SVIP 50%:</span> <strong>x15 Tấm</strong></li>
                    <li><span>Thẻ Đổi Tên HLV:</span> <strong>x03 Thẻ</strong></li>
                    <li><span>Hộp Quà Kim Cương FC:</span> <strong>x25 Hộp</strong></li>
                </ul>
            </div>

            <div style="padding: 0 25px 20px;">
                <button class="btn-buy" id="btnModalBuyAction" style="width: 100%; margin-top: 10px; padding: 12px 0;">
                    <i class="fa-solid fa-cart-shopping"></i> TIẾN HÀNH THANH TOÁN BẢO MẬT
                </button>
            </div>
        </div>
    </div>

    <!-- MODAL 2: THANH TOÁN VIETQR & GỬI YÊU CẦU XÁC THỰC CHO ADMIN -->
    <div class="modal-wrapper" id="paymentModal">
        <div class="modal-box" style="max-width: 520px;">
            <button class="modal-close-btn" onclick="closeModal('paymentModal')"><i class="fa-solid fa-xmark"></i></button>
            <div class="qr-card-box">
                <h3 style="font-family: 'Orbitron', sans-serif; color: var(--accent-gold); font-size: 18px;" id="payAccTitle">
                    THANH TOÁN ACC FC ONLINE
                </h3>
                <p style="color: var(--text-dim); font-size: 13px; margin-top: 4px;">
                    Quét mã VietQR bằng App Ngân hàng với đúng nội dung bên dưới
                </p>

                <img src="" alt="VietQR Code" class="qr-img" id="vietQrImg">

                <table class="bank-info-table">
                    <tr>
                        <td>Ngân hàng:</td>
                        <td>Vietcombank (VCB)</td>
                    </tr>
                    <tr>
                        <td>Số tài khoản:</td>
                        <td>
                            <span id="bankNum">0961599740</span>
                            <button class="copy-btn" onclick="copyText('0961599740')">SAO CHÉP</button>
                        </td>
                    </tr>
                    <tr>
                        <td>Chủ tài khoản:</td>
                        <td>NGOC HAO</td>
                    </tr>
                    <tr>
                        <td>Số tiền:</td>
                        <td id="payPriceVal" style="color: var(--primary-neon);">600.000 VNĐ</td>
                    </tr>
                    <tr>
                        <td>Nội dung CK:</td>
                        <td>
                            <span id="memoVal" style="color: var(--accent-gold);">MS10B CHUYENKHOAN</span>
                            <button class="copy-btn" onclick="copyText(document.getElementById('memoVal').innerText)">SAO CHÉP</button>
                        </td>
                    </tr>
                </table>

                <!-- BẢO MẬT GỬI YÊU CẦU DUYỆT CHO ADMIN -->
                <div class="verify-box">
                    <label style="color: var(--accent-gold); font-size: 13px; font-weight: 700; display: flex; align-items: center; gap: 6px;">
                        <i class="fa-solid fa-shield-halved"></i> XÁC THỰC NHANH QUA ZALO ADMIN:
                    </label>
                    <p style="font-size: 11px; color: var(--text-dim); margin-top: 4px;">
                        Sau khi chuyển khoản thành công, bạn có thể gửi thẳng biên lai qua Zalo để Admin Ngọc Hào duyệt tự động & mở khóa mật khẩu tức thì!
                    </p>
                    <a href="https://zalo.me/0961599740" target="_blank" style="display: flex; align-items: center; justify-content: center; gap: 8px; background: #0068ff; color: #fff; padding: 10px; border-radius: 6px; text-decoration: none; font-weight: 900; margin-top: 8px; font-family: 'Rajdhani', sans-serif;">
                        <i class="fa-solid fa-comment-dots"></i> NHẮN ZALO ADMIN (0961.599.740) ĐỂ DUYỆT NGAY
                    </a>
                    <input type="text" id="txRefInput" class="verify-input" placeholder="Hoặc nhập mã giao dịch (FT...) rồi bấm gửi hệ thống..." style="margin-top: 10px;">
                </div>

                <button class="btn-buy" style="width: 100%; margin-top: 15px; padding: 12px 0;" onclick="submitPaymentVerification()">
                    <i class="fa-solid fa-paper-plane"></i> GỬI YÊU CẦU XÁC THỰC HỆ THỐNG
                </button>
            </div>
        </div>
    </div>

    <!-- MODAL 3: CHỜ ADMIN DUYỆT -->
    <div class="modal-wrapper" id="waitingModal">
        <div class="modal-box" style="max-width: 480px; text-align: center; padding: 30px;">
            <div style="font-size: 50px; color: var(--accent-gold); margin-bottom: 15px; animation: floatBP 2s infinite ease-in-out;">
                <i class="fa-solid fa-hourglass-half"></i>
            </div>
            <h3 style="font-family: 'Orbitron', sans-serif; color: var(--accent-gold); font-size: 20px; margin-bottom: 10px;">
                ĐÃ GỬI YÊU CẦU CHO ADMIN!
            </h3>
            <p style="font-size: 13px; color: var(--text-dim); line-height: 1.6;" id="waitingSubText">
                Hệ thống đã chuyển yêu cầu xác thực chuyển khoản của bạn đến bảng quản trị của Admin Ngọc Hào. Vui lòng đợi trong giây lát, Admin sẽ duyệt ngay khi nhận được tiền vào tài khoản VCB!
            </p>
            <button class="btn-view" style="width: 100%; margin-top: 20px; justify-content: center;" onclick="closeModal('waitingModal')">
                ĐÓNG CỬA SỔ & THEO DÕI
            </button>
        </div>
    </div>

    <!-- MODAL 4: BÀN GIAO TÀI KHOẢN BẢO MẬT -->
    <div class="modal-wrapper" id="deliveryModal">
        <div class="modal-box" style="max-width: 520px; border-color: var(--accent-gold); box-shadow: 0 0 35px rgba(255, 215, 0, 0.4);">
            <button class="modal-close-btn" onclick="closeModal('deliveryModal')"><i class="fa-solid fa-xmark"></i></button>
            
            <div style="padding: 25px; text-align: center;">
                <div style="font-size: 48px; color: var(--primary-neon); margin-bottom: 10px;">
                    <i class="fa-solid fa-circle-check"></i>
                </div>
                <h3 style="font-family: 'Orbitron', sans-serif; color: var(--accent-gold); font-size: 20px; margin-bottom: 5px;">
                    🎉 ADMIN ĐÃ XÁC THỰC THÀNH CÔNG!
                </h3>
                <p style="font-size: 13px; color: var(--primary-neon); font-weight: 700;" id="deliveryAccCode">Tài khoản đã được mở khóa bảo mật</p>

                <div style="background: rgba(0, 0, 0, 0.6); border: 1px solid var(--border-color); border-radius: 12px; padding: 18px; margin-top: 15px; text-align: left;">
                    <p style="font-size: 12px; color: var(--accent-gold); margin-bottom: 12px; text-align: center; border-bottom: 1px dashed var(--border-color); padding-bottom: 8px;">
                        <i class="fa-solid fa-key"></i> THÔNG TIN ĐĂNG NHẬP GARENA (ĐÃ MỞ KHÓA)
                    </p>

                    <div style="margin-bottom: 12px; display: flex; justify-content: space-between; align-items: center; background: #090d16; padding: 10px 14px; border-radius: 8px; border: 1px solid var(--border-color);">
                        <div>
                            <span style="font-size: 11px; color: var(--text-dim); display: block;">Tài khoản Garena:</span>
                            <strong style="font-size: 16px; color: #fff; font-family: 'Rajdhani', sans-serif;" id="delivUser">rwhaogaming1</strong>
                        </div>
                        <button class="copy-btn" style="padding: 6px 12px; font-size: 12px;" onclick="copyText(document.getElementById('delivUser').innerText)">
                            <i class="fa-solid fa-copy"></i> SAO CHÉP
                        </button>
                    </div>

                    <div style="margin-bottom: 12px; display: flex; justify-content: space-between; align-items: center; background: #090d16; padding: 10px 14px; border-radius: 8px; border: 1px solid var(--border-color);">
                        <div>
                            <span style="font-size: 11px; color: var(--text-dim); display: block;">Mật khẩu (Đã mở khóa):</span>
                            <strong style="font-size: 16px; color: var(--primary-neon); font-family: 'Rajdhani', sans-serif;" id="delivPass">Hao13032008@@@</strong>
                        </div>
                        <button class="copy-btn" style="padding: 6px 12px; font-size: 12px;" onclick="copyText(document.getElementById('delivPass').innerText)">
                            <i class="fa-solid fa-copy"></i> SAO CHÉP
                        </button>
                    </div>

                    <div style="display: flex; justify-content: space-between; align-items: center; background: #090d16; padding: 10px 14px; border-radius: 8px; border: 1px solid var(--border-color);">
                        <div>
                            <span style="font-size: 11px; color: var(--text-dim); display: block;">Mật khẩu Cấp 2:</span>
                            <strong style="font-size: 16px; color: var(--accent-gold); font-family: 'Rajdhani', sans-serif;" id="delivMk2">1804</strong>
                        </div>
                        <button class="copy-btn" style="padding: 6px 12px; font-size: 12px;" onclick="copyText(document.getElementById('delivMk2').innerText)">
                            <i class="fa-solid fa-copy"></i> SAO CHÉP
                        </button>
                    </div>
                </div>

                <div style="margin-top: 15px; background: rgba(0, 230, 118, 0.1); border: 1px solid var(--primary-neon); padding: 10px; border-radius: 8px; font-size: 12px; color: var(--text-light); text-align: left;">
                    <i class="fa-solid fa-shield-cat" style="color: var(--primary-neon);"></i> <strong>Lưu ý:</strong> Hãy đổi ngay số điện thoại và email tại <code>account.garena.com</code> để bảo vệ tài khoản vĩnh viễn!
                </div>

                <button class="btn-buy" style="width: 100%; margin-top: 20px; padding: 12px 0;" onclick="closeModal('deliveryModal'); showToast('Đã lưu thông tin bảo mật thành công!');">
                    <i class="fa-solid fa-circle-check"></i> HOÀN TẤT & ĐÓNG CỬA SỔ
                </button>
            </div>
        </div>
    </div>

    <!-- MODAL 5: ĐĂNG NHẬP ADMIN -->
    <div class="modal-wrapper" id="adminLoginModal">
        <div class="modal-box" style="max-width: 400px; padding: 25px;">
            <button class="modal-close-btn" onclick="closeModal('adminLoginModal')"><i class="fa-solid fa-xmark"></i></button>
            <h3 style="font-family: 'Orbitron', sans-serif; color: var(--accent-gold); font-size: 18px; margin-bottom: 15px;">
                <i class="fa-solid fa-user-shield"></i> ĐĂNG NHẬP QUẢN TRỊ ADMIN
            </h3>
            <div style="margin-bottom: 12px;">
                <label style="font-size: 12px; color: var(--text-dim);">Mật khẩu Quản trị:</label>
                <input type="password" id="adminPassInput" class="verify-input" placeholder="Nhập mật khẩu admin...">
            </div>
            <button class="btn-buy" style="width: 100%; padding: 10px 0; margin-top: 5px;" onclick="verifyAdminLogin()">
                TRUY CẬP BẢNG ĐIỀU KHIỂN
            </button>
        </div>
    </div>

    <!-- MODAL 7: FORM TẠO ACC CHO NGƯỜI XEM -->
    <div class="modal-wrapper" id="userCreateAccModal">
        <div class="modal-box" style="max-width: 520px; padding: 25px;">
            <button class="modal-close-btn" onclick="closeModal('userCreateAccModal')"><i class="fa-solid fa-xmark"></i></button>
            
            <h3 style="font-family: 'Orbitron', sans-serif; color: var(--accent-gold); font-size: 18px; margin-bottom: 5px;">
                <i class="fa-solid fa-user-pen"></i> TẠO ACC & KÝ GỬI CHO NGƯỜI XEM
            </h3>
            <p style="font-size: 12px; color: var(--text-dim); margin-bottom: 15px;">
                Nhập thông tin tài khoản của bạn. Sau khi tạo thành công, acc sẽ xuất hiện trực tiếp ngoài trang chủ để người xem khác tiến hành thanh toán!
            </p>

            <div style="display: flex; flex-direction: column; gap: 12px;">
                <div>
                    <label style="font-size: 12px; color: var(--text-dim);">Mã số Acc / Tiêu đề ngắn (Ví dụ: MS999 - Acc Full Team Real):</label>
                    <input type="text" id="ucCode" class="verify-input" placeholder="Nhập mã số (VD: MS999)...">
                </div>

                <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 10px;">
                    <div>
                        <label style="font-size: 12px; color: var(--text-dim);">Tài khoản Garena:</label>
                        <input type="text" id="ucAccName" class="verify-input" placeholder="Tên đăng nhập...">
                    </div>
                    <div>
                        <label style="font-size: 12px; color: var(--text-dim);">Mật khẩu Garena:</label>
                        <input type="text" id="ucPass" class="verify-input" placeholder="Mật khẩu...">
                    </div>
                </div>

                <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 10px;">
                    <div>
                        <label style="font-size: 12px; color: var(--text-dim);">Giá trị BP (Ví dụ: 10000 Tỷ):</label>
                        <input type="number" id="ucBp" class="verify-input" placeholder="Nhập số BP..." value="5000">
                    </div>
                    <div>
                        <label style="font-size: 12px; color: var(--text-dim);">Giá bán (VNĐ):</label>
                        <input type="number" id="ucPrice" class="verify-input" placeholder="Nhập giá VNĐ..." value="200000">
                    </div>
                </div>

                <div>
                    <label style="font-size: 12px; color: var(--text-dim);">Mật khẩu cấp 2:</label>
                    <input type="text" id="ucMk2" class="verify-input" placeholder="Mã pin cấp 2..." value="1234">
                </div>
            </div>

            <button class="btn-buy" style="width: 100%; margin-top: 20px; padding: 12px 0;" onclick="submitUserCreatedAcc()">
                <i class="fa-solid fa-cloud-arrow-up"></i> ĐĂNG BÁN ACC LÊN SHOP NGAY
            </button>
        </div>
    </div>

    <!-- MODAL 6: BẢNG QUẢN TRỊ ADMIN -->
    <div class="modal-wrapper" id="adminDashboardModal">
        <div class="modal-box" style="max-width: 850px; padding: 25px;">
            <button class="modal-close-btn" onclick="closeModal('adminDashboardModal')"><i class="fa-solid fa-xmark"></i></button>
            <div style="display: flex; justify-content: space-between; align-items: center; border-bottom: 1px solid var(--border-color); padding-bottom: 12px; margin-bottom: 15px;">
                <h3 style="font-family: 'Orbitron', sans-serif; color: var(--accent-gold); font-size: 18px;">
                    <i class="fa-solid fa-gauge-high"></i> BẢNG ĐIỀU KHIỂN ADMIN - DUYỆT GIAO DỊCH CK
                </h3>
                <span style="font-size: 12px; color: var(--primary-neon); background: rgba(0,230,118,0.1); padding: 4px 10px; border-radius: 4px;">Trạng thái: Đang hoạt động 24/7</span>
            </div>

            <p style="font-size: 13px; color: var(--text-dim); margin-bottom: 15px;">
                Danh sách các yêu cầu chuyển khoản khách hàng đang chờ duyệt. Khi bạn bấm <strong>"Duyệt CK"</strong>, hệ thống bên phía khách hàng tương ứng sẽ lập tức mở khóa hiện thông tin tài khoản Garena!
            </p>

            <div style="overflow-x: auto;">
                <table class="admin-table">
                    <thead>
                        <tr>
                            <th>Mã Đơn / Acc</th>
                            <th>Mã Giao Dịch (FT)</th>
                            <th>Số Tiền</th>
                            <th>Thời Gian</th>
                            <th>Hành Động Duyệt</th>
                        </tr>
                    </thead>
                    <tbody id="adminOrderTableBody">
                        <!-- Rendered dynamically -->
                    </tbody>
                </table>
            </div>
        </div>
    </div>

    <div class="toast" id="toastMsg">Đã sao chép vào bộ nhớ tạm!</div>

    <!-- Footer -->
    <footer id="ho-tro">
        <div class="container">
            <h3 style="font-family: 'Orbitron', sans-serif; color: var(--primary-neon); margin-bottom: 8px;">SHOP ACC FC ONLINE NGỌC HÀO</h3>
            <p>Hệ thống bảo mật duyệt chuyển khoản tự động và xác thực qua Zalo 24/7</p>
            <p style="margin-top: 12px;">
                <a href="https://zalo.me/0961599740" target="_blank" style="background: #0068ff; color: #fff; padding: 8px 16px; border-radius: 8px; text-decoration: none; font-weight: 900; display: inline-flex; align-items: center; gap: 6px; box-shadow: 0 0 15px rgba(0, 104, 255, 0.4);">
                    <i class="fa-solid fa-comments"></i> Chat Zalo Trực Tiếp: 0961.599.740 (Ngọc Hào)
                </a>
            </p>
            <p style="margin-top: 15px; font-size: 12px; color: var(--text-dim);">© 2026 Shop Acc FC Online Ngọc Hào. All rights reserved.</p>
        </div>
    </footer>

    <script>
        const accountsData = [
            {
                code: "MS10B_RWHAOGAMING1",
                accName: "rwhaogaming1",
                pass: "Hao13032008@@@",
                mk2: "1804",
                bp: 10000,
                bpDisplay: "10.000 TỶ BP",
                price: 600000,
                tag: "⚡ HOT GARENA",
                tagColor: "linear-gradient(45deg, #ff0055, #ffd700)",
                gif: "https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExbnEybXo5dWQzaWhubWkzdTZ1MXk4a3kwaGx3bzlpNzBsZXZxbDV1NSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/l0HlA1H749A5N2G7C/giphy.gif",
                players: [
                    { name: "Pele ICON TM", stat: "+3 138", img: "https://cdn-icons-png.flaticon.com/512/166/166120.png" },
                    { name: "Zidane ICON", stat: "+5 135", img: "https://cdn-icons-png.flaticon.com/512/166/166120.png" },
                    { name: "Maldini ICON", stat: "+5 134", img: "https://cdn-icons-png.flaticon.com/512/166/166120.png" }
                ]
            },
            {
                code: "MS806",
                accName: "acc_5b_trang",
                pass: "MatKhau123@",
                mk2: "1234",
                bp: 5000,
                bpDisplay: "5.000 TỶ BP",
                price: 150000,
                tag: "SIÊU RẺ",
                tagColor: "linear-gradient(45deg, #ff9500, #ff2d55)",
                gif: "https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExM3k2Y2tzNXh3eXdyNWkxbmlmNXF4am12eWVzOHYycjlseWs4aWF1YSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/4T41C12M3g2t1R8PzD/giphy.gif",
                players: [
                    { name: "C. Ronaldo ICON", stat: "+5 132", img: "https://cdn-icons-png.flaticon.com/512/166/166120.png" },
                    { name: "L. Messi 23TS", stat: "+5 130", img: "https://cdn-icons-png.flaticon.com/512/166/166120.png" },
                    { name: "Gullit ICON", stat: "+3 131", img: "https://cdn-icons-png.flaticon.com/512/166/166120.png" }
                ]
            },
            {
                code: "MS807",
                accName: "acc_8b_trang",
                pass: "MatKhau888@",
                mk2: "8888",
                bp: 8000,
                bpDisplay: "8.000 TỶ BP",
                price: 400000,
                tag: "HOT SALE",
                tagColor: "linear-gradient(45deg, #00b0ff, #00e676)",
                gif: "https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExbDVscWFmMDlpdG55bjQ3cW1rdHBxbWszZmR5bm5sOHl3azljbzFxbCZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/3o7TKSjRrfIPjeiVyM/giphy.gif",
                players: [
                    { name: "Ronaldo De Lima LN", stat: "+6 134", img: "https://cdn-icons-png.flaticon.com/512/166/166120.png" },
                    { name: "KDB 24TS", stat: "+5 133", img: "https://cdn-icons-png.flaticon.com/512/166/166120.png" },
                    { name: "Van Dijk BWC", stat: "+6 132", img: "https://cdn-icons-png.flaticon.com/512/166/166120.png" }
                ]
            },
            {
                code: "MS808",
                accName: "acc_15b_trang",
                pass: "MatKhau15b@",
                mk2: "1515",
                bp: 15000,
                bpDisplay: "15.000 TỶ BP",
                price: 900000,
                tag: "VIP PRO",
                tagColor: "linear-gradient(45deg, #9d4edd, #00b0ff)",
                gif: "https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExM3k2Y2tzNXh3eXdyNWkxbmlmNXF4am12eWVzOHYycjlseWs4aWF1YSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/4T41C12M3g2t1R8PzD/giphy.gif",
                players: [
                    { name: "Son Heung Min24TS", stat: "+6 136", img: "https://cdn-icons-png.flaticon.com/512/166/166120.png" },
                    { name: "Mbappe 24TS", stat: "+5 137", img: "https://cdn-icons-png.flaticon.com/512/166/166120.png" },
                    { name: "Haaland 24TS", stat: "+5 136", img: "https://cdn-icons-png.flaticon.com/512/166/166120.png" }
                ]
            },
            {
                code: "MS809",
                accName: "acc_20b_trang",
                pass: "MatKhau20b@",
                mk2: "2020",
                bp: 20000,
                bpDisplay: "20.000 TỶ BP",
                price: 1200000,
                tag: "SUPER VIP",
                tagColor: "linear-gradient(45deg, #00e676, #ffd700)",
                gif: "https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExbDVscWFmMDlpdG55bjQ3cW1rdHBxbWszZmR5bm5sOHl3azljbzFxbCZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/3o7TKSjRrfIPjeiVyM/giphy.gif",
                players: [
                    { name: "C. Ronaldo ICON TM", stat: "+5 140", img: "https://cdn-icons-png.flaticon.com/512/166/166120.png" },
                    { name: "Gullit ICON TM", stat: "+5 139", img: "https://cdn-icons-png.flaticon.com/512/166/166120.png" },
                    { name: "Shevchenko ICON TM", stat: "+5 138", img: "https://cdn-icons-png.flaticon.com/512/166/166120.png" }
                ]
            }
        ];

        let pendingOrders = [];
        let currentSelectedAcc = null;
        let activePayAccount = null;

        // Xử lý sự kiện nhấn 5 lần vào tên shop để mở Đăng nhập Admin
        let logoClickCount = 0;
        let logoClickTimer = null;

        document.getElementById('shopLogo').addEventListener('click', function(e) {
            e.preventDefault();
            logoClickCount++;
            clearTimeout(logoClickTimer);

            if (logoClickCount === 5) {
                logoClickCount = 0;
                openAdminLoginModal();
            } else {
                logoClickTimer = setTimeout(() => {
                    logoClickCount = 0;
                }, 2000);
            }
        });

        function renderProducts(data) {
            const grid = document.getElementById('productGrid');
            grid.innerHTML = '';

            data.forEach(acc => {
                const card = document.createElement('div');
                card.className = 'product-card';
                card.setAttribute('data-price', acc.price);

                card.innerHTML = `
                    <div class="card-thumb">
                        <img src="${acc.gif}" alt="${acc.code}" class="card-gif-preview" onerror="this.src='https://media.giphy.com/media/4T41C12M3g2t1R8PzD/giphy.gif'">
                        <span class="bp-badge-overlay">${acc.bpDisplay}</span>
                        <span style="position: absolute; top:10px; right:10px; background:${acc.tagColor}; color:#000; font-size:10px; font-weight:900; padding:2px 8px; border-radius:4px;">${acc.tag}</span>
                    </div>
                    <div class="card-body">
                        <h3 class="card-title">ACC FC ONLINE - ${acc.code}</h3>
                        <ul class="specs-list">
                            <li><span>Bảo Mật:</span> <strong>Duyệt CK Trực Tiếp 24/7</strong></li>
                            <li><span>Giá BP:</span> <strong>${acc.bpDisplay}</strong></li>
                            <li><span>Hệ Thống:</span> <strong>Mở Khoá An Toàn</strong></li>
                        </ul>
                        <div style="display:flex; justify-content:space-between; align-items:center; margin-bottom:12px;">
                            <span style="font-size:12px; color:var(--text-dim);">Giá bán:</span>
                            <span class="price-tag">${acc.price.toLocaleString('vi-VN')}đ</span>
                        </div>
                        <div class="card-actions">
                            <button class="btn-view" onclick="openDetailModal('${acc.code}')">
                                <i class="fa-solid fa-eye"></i> XEM ACC
                            </button>
                            <button class="btn-buy btn-shake" onclick="openPaymentModal('${acc.code}', ${acc.price})">
                                MUA NGAY
                            </button>
                        </div>
                    </div>
                `;
                grid.appendChild(card);
            });
        }

        function applyFilter(type, btn) {
            document.querySelectorAll('.filter-btn').forEach(b => b.classList.remove('active'));
            btn.classList.add('active');

            if (type === 'all') {
                renderProducts(accountsData);
            } else if (type === 'under500') {
                renderProducts(accountsData.filter(a => a.price < 500000));
            } else if (type === '500to1000') {
                renderProducts(accountsData.filter(a => a.price >= 500000 && a.price <= 1000000));
            } else if (type === 'over1000') {
                renderProducts(accountsData.filter(a => a.price > 1000000));
            }
        }

        function openDetailModal(code) {
            const acc = accountsData.find(a => a.code === code);
            if (!acc) return;
            currentSelectedAcc = acc;

            document.getElementById('modalAccCode').innerHTML = `<i class="fa-solid fa-shield-halved"></i> ACC FC ONLINE - ${acc.code}`;
            document.getElementById('detailGifImg').src = acc.gif;
            document.getElementById('detailBpVal').innerText = acc.bpDisplay;
            document.getElementById('detailPriceVal').innerText = acc.price.toLocaleString('vi-VN') + 'đ';

            const playerBox = document.getElementById('modalPlayerList');
            playerBox.innerHTML = acc.players.map(p => `
                <div class="player-badge-card">
                    <img src="${p.img}" alt="${p.name}">
                    <span class="p-name">${p.name}</span>
                    <span class="p-stat">${p.stat}</span>
                </div>
            `).join('');

            document.getElementById('btnModalBuyAction').onclick = function() {
                closeModal('accDetailModal');
                openPaymentModal(acc.code, acc.price);
            };

            document.getElementById('accDetailModal').style.display = 'flex';
        }

        function openPaymentModal(code, price) {
            const acc = accountsData.find(a => a.code === code) || { code, price, accName: "rwhaogaming1", pass: "Hao13032008@@@", mk2: "1804" };
            activePayAccount = acc;

            document.getElementById('payAccTitle').innerText = `THANH TOÁN BẢO MẬT - ${acc.code}`;
            document.getElementById('payPriceVal').innerText = price.toLocaleString('vi-VN') + ' VNĐ';
            document.getElementById('txRefInput').value = '';
            
            const memo = `${acc.code} CHUYENKHOAN`;
            document.getElementById('memoVal').innerText = memo;

            const bankId = "VCB";
            const accountNo = "0961599740";
            const accountName = "NGOC HAO";
            const qrUrl = `https://img.vietqr.io/image/${bankId}-${accountNo}-compact2.png?amount=${price}&addInfo=${encodeURIComponent(memo)}&accountName=${encodeURIComponent(accountName)}`;

            document.getElementById('vietQrImg').src = qrUrl;
            document.getElementById('paymentModal').style.display = 'flex';
        }

        function submitPaymentVerification() {
            const txInput = document.getElementById('txRefInput').value.trim();
            if(!txInput) {
                showToast('Vui lòng nhập mã giao dịch ngân hàng (FT...) để gửi admin xác thực!');
                return;
            }

            const orderId = 'ORD-' + Math.floor(1000 + Math.random() * 9000);
            const newOrder = {
                id: orderId,
                accCode: activePayAccount.code,
                txRef: txInput,
                price: activePayAccount.price.toLocaleString('vi-VN') + 'đ',
                time: new Date().toLocaleTimeString(),
                accData: activePayAccount
            };

            pendingOrders.push(newOrder);

            closeModal('paymentModal');
            document.getElementById('waitingModal').style.display = 'flex';
            showToast('Đã gửi mã giao dịch cho Admin Ngọc Hào thành công!');
        }

        function openAdminLoginModal() {
            document.getElementById('adminPassInput').value = '';
            document.getElementById('adminLoginModal').style.display = 'flex';
        }

        function openUserCreateModal() {
            document.getElementById('userCreateAccModal').style.display = 'flex';
        }

        function submitUserCreatedAcc() {
            const code = document.getElementById('ucCode').value.trim();
            const accName = document.getElementById('ucAccName').value.trim();
            const pass = document.getElementById('ucPass').value.trim();
            const bp = parseInt(document.getElementById('ucBp').value) || 5000;
            const price = parseInt(document.getElementById('ucPrice').value) || 150000;
            const mk2 = document.getElementById('ucMk2').value.trim() || '1234';

            if(!code || !accName || !pass) {
                showToast('Vui lòng điền đầy đủ Mã số, Tài khoản và Mật khẩu Garena!');
                return;
            }

            const newAcc = {
                code: code,
                accName: accName,
                pass: pass,
                mk2: mk2,
                bp: bp,
                bpDisplay: bp.toLocaleString('vi-VN') + ' TỶ BP',
                price: price,
                tag: '👤 NGƯỜI XEM TẠO',
                tagColor: 'linear-gradient(45deg, #00b0ff, #9d4edd)',
                gif: 'https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExM3k2Y2tzNXh3eXdyNWkxbmlmNXF4am12eWVzOHYycjlseWs4aWF1YSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/4T41C12M3g2t1R8PzD/giphy.gif',
                players: [
                    { name: "Cầu thủ tùy chỉnh", stat: "+5 130", img: "https://cdn-icons-png.flaticon.com/512/166/166120.png" },
                    { name: "Đội hình người xem", stat: "+5 128", img: "https://cdn-icons-png.flaticon.com/512/166/166120.png" }
                ]
            };

            accountsData.unshift(newAcc);
            renderProducts(accountsData);

            closeModal('userCreateAccModal');
            showToast('Tạo và đăng bán acc thành công! Acc của bạn đã xuất hiện ngoài shop.');
            document.getElementById('danh-sach').scrollIntoView({ behavior: 'smooth' });
        }

        function verifyAdminLogin() {
            const pass = document.getElementById('adminPassInput').value;
            if(pass === 'hao13032008@@@@') {
                closeModal('adminLoginModal');
                renderAdminOrders();
                document.getElementById('adminDashboardModal').style.display = 'flex';
                showToast('Đăng nhập Quản trị thành công!');
            } else {
                showToast('Mật khẩu admin không chính xác!');
            }
        }

        function renderAdminOrders() {
            const tbody = document.getElementById('adminOrderTableBody');
            tbody.innerHTML = '';

            if(pendingOrders.length === 0) {
                tbody.innerHTML = `<tr><td colspan="5" style="text-align:center; color:var(--text-dim); padding:20px;">Chưa có yêu cầu chuyển khoản nào đang chờ duyệt.</td></tr>`;
                return;
            }

            pendingOrders.forEach((order, index) => {
                const tr = document.createElement('tr');
                tr.innerHTML = `
                    <td><strong>${order.accCode}</strong></td>
                    <td style="color: var(--accent-gold);">${order.txRef}</td>
                    <td style="color: var(--primary-neon);">${order.price}</td>
                    <td>${order.time}</td>
                    <td>
                        <button class="admin-approve-btn" onclick="adminApproveOrder(${index})">
                            <i class="fa-solid fa-check"></i> Duyệt CK & Mở Khóa
                        </button>
                    </td>
                `;
                tbody.appendChild(tr);
            });
        }

        function adminApproveOrder(index) {
            const order = pendingOrders[index];
            pendingOrders.splice(index, 1);
            renderAdminOrders();

            closeModal('adminDashboardModal');
            closeModal('waitingModal');

            if(order && order.accData) {
                document.getElementById('deliveryAccCode').innerText = `MÃ GD: ${order.txRef} - ${order.accData.code}`;
                document.getElementById('delivUser').innerText = order.accData.accName || 'rwhaogaming1';
                document.getElementById('delivPass').innerText = order.accData.pass || 'Hao13032008@@@';
                document.getElementById('delivMk2').innerText = order.accData.mk2 || '1804';
                document.getElementById('deliveryModal').style.display = 'flex';
                showToast(`Đã duyệt đơn hàng ${order.accCode}! Khách đã nhận mật khẩu.`);
            }
        }

        function closeModal(modalId) {
            document.getElementById(modalId).style.display = 'none';
        }

        function switchTab(tabId, btn) {
            document.querySelectorAll('.tab-btn').forEach(b => b.classList.remove('active'));
            document.querySelectorAll('.tab-content').forEach(c => c.classList.remove('active'));

            btn.classList.add('active');
            document.getElementById(tabId).classList.add('active');
        }

        function copyText(text) {
            const input = document.createElement('textarea');
            input.value = text;
            document.body.appendChild(input);
            input.select();
            document.execCommand('copy');
            document.body.removeChild(input);
            showToast(`Đã sao chép: ${text}`);
        }

        function showToast(msg) {
            const toast = document.getElementById('toastMsg');
            toast.innerText = msg;
            toast.style.display = 'block';
            setTimeout(() => { toast.style.display = 'none'; }, 2500);
        }

        window.onload = function() {
            renderProducts(accountsData);

            const canvas = document.getElementById('bgCanvas');
            const ctx = canvas.getContext('2d');

            function resizeCanvas() {
                canvas.width = window.innerWidth;
                canvas.height = window.innerHeight;
            }
            resizeCanvas();
            window.addEventListener('resize', resizeCanvas);

            const particles = [];
            const particleCount = 45;

            for (let i = 0; i < particleCount; i++) {
                particles.push({
                    x: Math.random() * canvas.width,
                    y: Math.random() * canvas.height,
                    radius: Math.random() * 2 + 1,
                    color: Math.random() > 0.5 ? '#00e676' : '#00b0ff',
                    speedX: (Math.random() - 0.5) * 0.8,
                    speedY: (Math.random() - 0.5) * 0.8
                });
            }

            function animateParticles() {
                ctx.clearRect(0, 0, canvas.width, canvas.height);

                particles.forEach((p, index) => {
                    p.x += p.speedX;
                    p.y += p.speedY;

                    if (p.x < 0 || p.x > canvas.width) p.speedX *= -1;
                    if (p.y < 0 || p.y > canvas.height) p.speedY *= -1;

                    ctx.beginPath();
                    ctx.arc(p.x, p.y, p.radius, 0, Math.PI * 2);
                    ctx.fillStyle = p.color;
                    ctx.shadowBlur = 10;
                    ctx.shadowColor = p.color;
                    ctx.fill();

                    for (let j = index + 1; j < particles.length; j++) {
                        const p2 = particles[j];
                        const dist = Math.hypot(p.x - p2.x, p.y - p2.y);
                        if (dist < 120) {
                            ctx.beginPath();
                            ctx.moveTo(p.x, p.y);
                            ctx.lineTo(p2.x, p2.y);
                            ctx.strokeStyle = `rgba(0, 230, 118, ${1 - dist / 120})`;
                            ctx.lineWidth = 0.5;
                            ctx.stroke();
                        }
                    }
                });

                requestAnimationFrame(animateParticles);
            }
            animateParticles();
        };
    </script>
</body>
</html>
