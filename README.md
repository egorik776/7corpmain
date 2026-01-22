
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>7Corp | Создание игр на Unity под заказ</title>
    <link rel="icon" href="data:image/svg+xml,<svg xmlns=%22http://www.w3.org/2000/svg%22 viewBox=%220 0 100 100%22><text y=%22.9em%22 font-size=%2290%22>7</text></svg>">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap">
    
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: 'Inter', sans-serif;
            line-height: 1.6;
            color: #f0f0f0;
            background-color: #000;
            overflow-x: hidden;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        section {
            padding: 100px 0;
        }

        h1, h2, h3, h4 {
            font-weight: 700;
            line-height: 1.2;
            margin-bottom: 20px;
        }

        h1 {
            font-size: 3.5rem;
            background: linear-gradient(90deg, #00dbde, #fc00ff);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            text-shadow: 0 0 30px rgba(0, 219, 222, 0.3);
        }

        h2 {
            font-size: 2.8rem;
            color: #fff;
            position: relative;
            display: inline-block;
        }

        h2::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 0;
            width: 80px;
            height: 4px;
            background: linear-gradient(90deg, #00dbde, #fc00ff);
            border-radius: 2px;
        }

        h3 {
            font-size: 1.8rem;
            color: #fff;
            margin-bottom: 15px;
        }

        p {
            font-size: 1.1rem;
            margin-bottom: 20px;
            color: #ccc;
        }

        .btn {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            padding: 16px 35px;
            background: linear-gradient(90deg, #00dbde, #fc00ff);
            color: white;
            text-decoration: none;
            border-radius: 50px;
            font-weight: 600;
            font-size: 1.1rem;
            text-transform: uppercase;
            letter-spacing: 1px;
            transition: all 0.3s ease;
            border: none;
            cursor: pointer;
            box-shadow: 0 5px 20px rgba(0, 219, 222, 0.3);
            position: relative;
            overflow: hidden;
            z-index: 1;
            gap: 10px;
        }

        .btn::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, #fc00ff, #00dbde);
            z-index: -1;
            opacity: 0;
            transition: opacity 0.3s ease;
        }

        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 25px rgba(0, 219, 222, 0.5);
        }

        .btn:hover::before {
            opacity: 1;
        }

        .btn-secondary {
            background: transparent;
            border: 2px solid #00dbde;
            box-shadow: none;
        }

        .btn-secondary:hover {
            background: rgba(0, 219, 222, 0.1);
        }

        .btn-contact {
            background: #0088cc;
        }

        .btn-contact:hover {
            background: #006699;
            transform: translateY(-3px);
        }

        .btn-avito {
            background: #5acb00;
        }

        .btn-avito:hover {
            background: #4ab000;
            transform: translateY(-3px);
        }

        .logo {
            font-family: 'Inter', sans-serif;
            font-size: 2.5rem;
            font-weight: 900;
            color: #fff;
            text-decoration: none;
            position: relative;
            display: flex;
            align-items: center;
            transition: transform 0.3s ease;
        }

        .logo:hover {
            transform: scale(1.05);
        }

        .logo-7 {
            background: white;
            color: black;
            width: 60px;
            height: 60px;
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 12px;
            font-size: 3rem;
            margin-right: 15px;
            font-weight: 900;
            box-shadow: 0 0 25px rgba(255, 255, 255, 0.3);
            animation: logoGlow 3s infinite alternate;
            position: relative;
        }

        .logo-7::after {
            content: '';
            position: absolute;
            top: -5px;
            left: -5px;
            right: -5px;
            bottom: -5px;
            border-radius: 17px;
            background: linear-gradient(45deg, #00dbde, #fc00ff, #00dbde);
            z-index: -1;
            opacity: 0.5;
            animation: rotate 10s linear infinite;
        }

        @keyframes logoGlow {
            0% {
                box-shadow: 0 0 25px rgba(255, 255, 255, 0.3);
            }
            100% {
                box-shadow: 0 0 35px rgba(255, 255, 255, 0.7), 0 0 50px rgba(0, 219, 222, 0.5);
            }
        }

        @keyframes rotate {
            0% {
                transform: rotate(0deg);
            }
            100% {
                transform: rotate(360deg);
            }
        }

        .logo-text {
            font-size: 1.8rem;
            background: linear-gradient(90deg, #fff, #00dbde);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            font-weight: 800;
        }

        header {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            z-index: 1000;
            padding: 20px 0;
            transition: all 0.3s ease;
            background-color: rgba(0, 0, 0, 0.95);
            backdrop-filter: blur(15px);
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        }

        header.scrolled {
            padding: 15px 0;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.8);
        }

        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        nav ul {
            display: flex;
            list-style: none;
        }

        nav ul li {
            margin-left: 35px;
        }

        nav ul li a {
            color: #fff;
            text-decoration: none;
            font-weight: 600;
            font-size: 1.1rem;
            transition: all 0.3s ease;
            position: relative;
            padding: 5px 0;
        }

        nav ul li a::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 0;
            height: 2px;
            background: linear-gradient(90deg, #00dbde, #fc00ff);
            transition: width 0.3s ease;
        }

        nav ul li a:hover {
            color: #00dbde;
        }

        nav ul li a:hover::after {
            width: 100%;
        }

        .mobile-menu-btn {
            display: none;
            background: none;
            border: none;
            color: white;
            font-size: 1.8rem;
            cursor: pointer;
            padding: 5px;
        }

        .hero {
            height: 100vh;
            display: flex;
            align-items: center;
            position: relative;
            overflow: hidden;
            background: radial-gradient(ellipse at center, #111 0%, #000 70%);
            padding-top: 80px;
        }

        .hero-bg {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
            opacity: 0.2;
            background: 
                radial-gradient(circle at 20% 50%, rgba(0, 219, 222, 0.15) 0%, transparent 50%),
                radial-gradient(circle at 80% 20%, rgba(252, 0, 255, 0.15) 0%, transparent 50%);
        }

        .hero-content {
            max-width: 850px;
            z-index: 2;
        }

        .hero h1 {
            margin-bottom: 25px;
            animation: fadeInUp 1s ease;
        }

        .hero p {
            font-size: 1.3rem;
            margin-bottom: 40px;
            color: #ddd;
            max-width: 700px;
            animation: fadeInUp 1s ease 0.3s both;
        }

        .hero-buttons {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            animation: fadeInUp 1s ease 0.6s both;
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .contact-buttons {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-top: 30px;
        }

        .contact-btn {
            display: inline-flex;
            align-items: center;
            padding: 14px 28px;
            background: rgba(255, 255, 255, 0.1);
            color: white;
            text-decoration: none;
            border-radius: 12px;
            font-weight: 600;
            font-size: 1rem;
            transition: all 0.3s ease;
            border: 1px solid rgba(255, 255, 255, 0.2);
            gap: 10px;
            backdrop-filter: blur(10px);
        }

        .contact-btn:hover {
            background: rgba(255, 255, 255, 0.2);
            transform: translateY(-3px);
            border-color: #00dbde;
        }

        .contact-btn i {
            font-size: 1.2rem;
        }

        .services {
            background-color: #0a0a0a;
            position: relative;
        }

        .services::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(45deg, transparent 60%, rgba(0, 17, 17, 0.1) 100%);
            pointer-events: none;
        }

        .section-intro {
            text-align: center;
            max-width: 800px;
            margin: 0 auto 70px;
        }

        .section-intro p {
            font-size: 1.2rem;
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 40px;
            margin-top: 60px;
        }

        .service-card {
            background: linear-gradient(145deg, #111, #0a0a0a);
            border-radius: 20px;
            padding: 45px 30px;
            text-align: center;
            transition: all 0.4s ease;
            border: 1px solid #222;
            position: relative;
            overflow: hidden;
            z-index: 1;
        }

        .service-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, rgba(0, 219, 222, 0.1), rgba(252, 0, 255, 0.1));
            z-index: -1;
            opacity: 0;
            transition: opacity 0.4s ease;
        }

        .service-card:hover {
            transform: translateY(-15px);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.6);
            border-color: #00dbde;
        }

        .service-card:hover::before {
            opacity: 1;
        }

        .service-icon {
            font-size: 4rem;
            margin-bottom: 30px;
            color: #00dbde;
            transition: transform 0.4s ease;
        }

        .service-card:hover .service-icon {
            transform: scale(1.1);
        }

        .process {
            background-color: #000;
            position: relative;
        }

        .process-steps {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 40px;
            margin-top: 70px;
            position: relative;
        }

        .process-step {
            flex: 1;
            min-width: 280px;
            max-width: 320px;
            text-align: center;
            position: relative;
            padding: 30px;
            border-radius: 15px;
            background: rgba(20, 20, 20, 0.5);
            transition: transform 0.3s ease;
        }

        .process-step:hover {
            transform: translateY(-10px);
            background: rgba(30, 30, 30, 0.7);
        }

        .step-number {
            width: 80px;
            height: 80px;
            background: linear-gradient(135deg, #00dbde, #fc00ff);
            color: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2rem;
            font-weight: 700;
            margin: 0 auto 30px;
            position: relative;
            z-index: 2;
            box-shadow: 0 0 25px rgba(0, 219, 222, 0.5);
        }

        .technologies {
            background-color: #0a0a0a;
        }

        .tech-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
            gap: 35px;
            margin-top: 70px;
        }

        .tech-item {
            border-radius: 20px;
            overflow: hidden;
            position: relative;
            height: 320px;
            transition: all 0.4s ease;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
            background: linear-gradient(145deg, #111, #0a0a0a);
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            padding: 40px;
            border: 1px solid #222;
        }

        .tech-item:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.7);
            border-color: #00dbde;
        }

        .tech-emoji {
            font-size: 5rem;
            margin-bottom: 25px;
            filter: drop-shadow(0 0 10px rgba(0, 219, 222, 0.3));
            transition: transform 0.4s ease;
        }

        .tech-item:hover .tech-emoji {
            transform: scale(1.2) rotate(5deg);
        }

        .tech-overlay {
            text-align: center;
        }

        .contact {
            background-color: #000;
            text-align: center;
            position: relative;
        }

        .contact-badges {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 25px;
            margin-top: 50px;
            margin-bottom: 60px;
        }

        .contact-badge {
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 30px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 20px;
            min-width: 280px;
            transition: all 0.3s ease;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        .contact-badge:hover {
            transform: translateY(-10px);
            background: rgba(255, 255, 255, 0.1);
            border-color: #00dbde;
            box-shadow: 0 15px 30px rgba(0, 219, 222, 0.2);
        }

        .badge-icon {
            font-size: 3.5rem;
            margin-bottom: 20px;
        }

        .badge-icon.telegram {
            color: #0088cc;
        }

        .badge-icon.avito {
            color: #5acb00;
        }

        .badge-content h4 {
            font-size: 1.5rem;
            margin-bottom: 10px;
            color: #fff;
        }

        .badge-content p {
            color: #aaa;
            margin-bottom: 15px;
        }

        .contact-form {
            max-width: 750px;
            margin: 60px auto 0;
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 30px;
        }

        .form-group {
            text-align: left;
        }

        .form-group.full-width {
            grid-column: 1 / -1;
        }

        .form-group label {
            display: block;
            margin-bottom: 10px;
            color: #fff;
            font-weight: 600;
            font-size: 1rem;
        }

        .form-group input,
        .form-group textarea,
        .form-group select {
            width: 100%;
            padding: 16px 20px;
            background: rgba(255, 255, 255, 0.07);
            border: 1px solid #333;
            border-radius: 12px;
            color: #fff;
            font-size: 1rem;
            transition: all 0.3s ease;
            font-family: 'Inter', sans-serif;
        }

        /* ФИКС ДЛЯ ВЫПАДАЮЩЕГО СПИСКА */
        .form-group select option {
            background-color: #0a0a0a;
            color: #fff;
            padding: 10px;
        }

        .form-group select option:checked {
            background-color: #00dbde;
            color: #000;
        }

        .form-group select option:hover {
            background-color: #333;
        }

        .form-group input:focus,
        .form-group textarea:focus,
        .form-group select:focus {
            outline: none;
            border-color: #00dbde;
            background: rgba(255, 255, 255, 0.1);
            box-shadow: 0 0 15px rgba(0, 219, 222, 0.2);
        }

        footer {
            background-color: #050505;
            padding: 80px 0 40px;
            border-top: 1px solid #222;
        }

        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 50px;
            margin-bottom: 60px;
        }

        .footer-logo {
            margin-bottom: 25px;
        }

        .footer-about p {
            color: #999;
            max-width: 300px;
        }

        .footer-links h3,
        .footer-contact h3 {
            color: #fff;
            margin-bottom: 25px;
            font-size: 1.5rem;
        }

        .footer-links ul {
            list-style: none;
        }

        .footer-links ul li {
            margin-bottom: 15px;
        }

        .footer-links ul li a {
            color: #999;
            text-decoration: none;
            transition: color 0.3s ease;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .footer-links ul li a:hover {
            color: #00dbde;
        }

        .footer-contact p {
            color: #999;
            margin-bottom: 15px;
            display: flex;
            align-items: center;
        }

        .footer-contact i {
            margin-right: 12px;
            color: #00dbde;
            width: 20px;
            text-align: center;
        }

        .social-links {
            display: flex;
            gap: 15px;
            margin-top: 25px;
        }

        .social-links a {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background: rgba(255, 255, 255, 0.1);
            display: flex;
            align-items: center;
            justify-content: center;
            color: #fff;
            text-decoration: none;
            transition: all 0.3s ease;
            font-size: 1.2rem;
        }

        .social-links a:hover {
            background: #00dbde;
            transform: translateY(-5px);
        }

        .copyright {
            text-align: center;
            padding-top: 40px;
            border-top: 1px solid #333;
            color: #777;
            font-size: 0.9rem;
        }

        @media (max-width: 992px) {
            h1 {
                font-size: 2.8rem;
            }
            
            h2 {
                font-size: 2.3rem;
            }
            
            section {
                padding: 80px 0;
            }
            
            .contact-form {
                grid-template-columns: 1fr;
            }
        }

        @media (max-width: 768px) {
            .mobile-menu-btn {
                display: block;
            }
            
            nav ul {
                position: fixed;
                top: 70px;
                left: -100%;
                width: 100%;
                height: calc(100vh - 70px);
                background: rgba(0, 0, 0, 0.98);
                flex-direction: column;
                align-items: center;
                justify-content: flex-start;
                padding-top: 50px;
                transition: left 0.3s ease;
                z-index: 999;
            }
            
            nav ul.active {
                left: 0;
            }
            
            nav ul li {
                margin: 20px 0;
            }
            
            h1 {
                font-size: 2.4rem;
            }
            
            h2 {
                font-size: 2rem;
            }
            
            .hero-buttons {
                flex-direction: column;
                align-items: flex-start;
            }
            
            .contact-badges {
                flex-direction: column;
                align-items: center;
            }
            
            .contact-badge {
                width: 100%;
                max-width: 350px;
            }
            
            .tech-grid {
                grid-template-columns: 1fr;
            }
        }

        @media (max-width: 480px) {
            h1 {
                font-size: 2rem;
            }
            
            h2 {
                font-size: 1.8rem;
            }
            
            .logo {
                font-size: 2rem;
            }
            
            .logo-7 {
                width: 50px;
                height: 50px;
                font-size: 2.5rem;
            }
            
            .btn {
                padding: 14px 25px;
                font-size: 1rem;
            }
            
            .service-card, .tech-item {
                padding: 30px 20px;
            }
            
            .tech-emoji {
                font-size: 4rem;
            }
        }
    </style>
</head>
<body>
    <header id="header">
        <div class="container header-container">
            <a href="#" class="logo">
                <div class="logo-7">7</div>
                <span class="logo-text">CORP</span>
            </a>
            
            <button class="mobile-menu-btn" id="mobileMenuBtn">
                <i class="fas fa-bars"></i>
            </button>
            
            <nav>
                <ul id="navMenu">
                    <li><a href="#home">🏠 Главная</a></li>
                    <li><a href="#services">🎮 Услуги</a></li>
                    <li><a href="#process">📋 Процесс</a></li>
                    <li><a href="#technologies">⚙️ Технологии</a></li>
                    <li><a href="#contact">📞 Контакты</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <section class="hero" id="home">
        <div class="hero-bg"></div>
        <div class="container">
            <div class="hero-content">
                <h1>🎮 Создаём игры на Unity под заказ</h1>
                <p>7Corp - студия разработки игр на Unity. Мы создаём качественные игры для мобильных устройств и ПК с использованием Unity3D.</p>
                
                <div class="hero-buttons">
                    <a href="#contact" class="btn">
                        <i class="fas fa-paper-plane"></i> 🚀 Обсудить проект
                    </a>
                    <a href="#services" class="btn btn-secondary">
                        <i class="fas fa-cogs"></i> 🔧 Наши услуги
                    </a>
                </div>
                
                <div class="contact-buttons">
                    <a href="https://t.me/sevencorp77" target="_blank" class="contact-btn">
                        <i class="fab fa-telegram"></i> 💬 Telegram: @sevencorp77
                    </a>
                    <a href="https://www.avito.ru/yaroslavl/predlozheniya_uslug/razrabotka_igr_na_unity_7744285832" target="_blank" class="contact-btn">
                        <i class="fas fa-store"></i> 🛒 Наш Авито
                    </a>
                </div>
            </div>
        </div>
    </section>

    <section class="services" id="services">
        <div class="container">
            <div class="section-intro">
                <h2>🎯 Наши услуги</h2>
                <p>Специализируемся на разработке игр на Unity для различных платформ</p>
            </div>
            
            <div class="services-grid">
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-gamepad"></i>
                    </div>
                    <h3>🎮 Мобильные игры на Unity</h3>
                    <p>Создание 2D/3D игр для iOS и Android на Unity3D</p>
                </div>
                
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-desktop"></i>
                    </div>
                    <h3>💻 Игры для ПК на Unity</h3>
                    <p>Разработка игр для Windows, macOS, Linux с использованием Unity</p>
                </div>
                
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-vr-cardboard"></i>
                    </div>
                    <h3>👓 VR проекты на Unity</h3>
                    <p>Создание VR приложений и игр с использованием Unity XR</p>
                </div>
                
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-tools"></i>
                    </div>
                    <h3>🔧 Доработка Unity игр</h3>
                    <p>Оптимизация, добавление функций, исправление багов в существующих Unity проектах</p>
                </div>
            </div>
        </div>
    </section>

    <section class="process" id="process">
        <div class="container">
            <div class="section-intro">
                <h2>📋 Процесс работы</h2>
                <p>Чёткая организация этапов разработки гарантирует качественный результат в оговоренные сроки</p>
            </div>
            
            <div class="process-steps">
                <div class="process-step">
                    <div class="step-number">01</div>
                    <div class="step-content">
                        <h3>💡 Консультация</h3>
                        <p>Обсуждение идеи, анализ рынка, определение целей и требований к проекту</p>
                    </div>
                </div>
                
                <div class="process-step">
                    <div class="step-number">02</div>
                    <div class="step-content">
                        <h3>🎨 Дизайн и прототип</h3>
                        <p>Создание концепции, дизайн интерфейса, разработка прототипа и MVP на Unity</p>
                    </div>
                </div>
                
                <div class="process-step">
                    <div class="step-number">03</div>
                    <div class="step-content">
                        <h3>⚙️ Разработка на Unity</h3>
                        <p>Программирование на C#, создание контента, интеграция и тестирование в Unity</p>
                    </div>
                </div>
                
                <div class="process-step">
                    <div class="step-number">04</div>
                    <div class="step-content">
                        <h3>🚀 Запуск и поддержка</h3>
                        <p>Публикация в магазинах приложений, техническая поддержка и дальнейшее развитие</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section class="technologies" id="technologies">
        <div class="container">
            <div class="section-intro">
                <h2>⚙️ Технологии Unity</h2>
                <p>Используем современные технологии и инструменты Unity для создания качественных игр</p>
            </div>
            
            <div class="tech-grid">
                <div class="tech-item">
                    <div class="tech-emoji">🎮</div>
                    <div class="tech-overlay">
                        <h3>Unity Engine</h3>
                        <p>Unity3D 2022 LTS, C# программирование, UGUI/UI Toolkit</p>
                    </div>
                </div>
                
                <div class="tech-item">
                    <div class="tech-emoji">📱</div>
                    <div class="tech-overlay">
                        <h3>Мобильная разработка</h3>
                        <p>iOS/Android сборки, адаптация интерфейсов, оптимизация производительности</p>
                    </div>
                </div>
                
                <div class="tech-item">
                    <div class="tech-emoji">🎨</div>
                    <div class="tech-overlay">
                        <h3>Графика и анимация</h3>
                        <p>Shader Graph, VFX Graph, Timeline, Cinemachine, Animator</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section class="contact" id="contact">
        <div class="container">
            <div class="section-intro">
                <h2>📞 Свяжитесь с нами</h2>
                <p>Готовы обсудить ваш проект на Unity? Выберите удобный способ связи</p>
            </div>
            
            <div class="contact-badges">
                <div class="contact-badge">
                    <div class="badge-icon telegram">
                        <i class="fab fa-telegram"></i>
                    </div>
                    <div class="badge-content">
                        <h4>💬 Telegram</h4>
                        <p>Быстрое общение, отправка файлов, голосовые сообщения</p>
                        <a href="https://t.me/sevencorp77" target="_blank" class="btn btn-contact">
                            <i class="fab fa-telegram"></i> @sevencorp77
                        </a>
                    </div>
                </div>
                
                <div class="contact-badge">
                    <div class="badge-icon avito">
                        <i class="fas fa-store"></i>
                    </div>
                    <div class="badge-content">
                        <h4>🛒 Авито Услуги</h4>
                        <p>Официальное предложение с отзывами и гарантией</p>
                        <a href="https://www.avito.ru/yaroslavl/predlozheniya_uslug/razrabotka_igr_na_unity_7744285832" target="_blank" class="btn btn-avito">
                            <i class="fas fa-external-link-alt"></i> Перейти на Авито
                        </a>
                    </div>
                </div>
            </div>
            
            <div class="section-intro">
                <h3>📝 Или оставьте заявку</h3>
                <p>Мы свяжемся с вами в течение 24 часов</p>
            </div>
            
            <form class="contact-form" id="contactForm">
                <div class="form-group">
                    <label for="name">👤 Имя</label>
                    <input type="text" id="name" required>
                </div>
                
                <div class="form-group">
                    <label for="contact">📧 Telegram или Email</label>
                    <input type="text" id="contact" required>
                </div>
                
                <div class="form-group full-width">
                    <label for="projectType">🎯 Тип проекта</label>
                    <select id="projectType">
                        <option value="">Выберите тип проекта</option>
                        <option value="mobile">📱 Мобильная игра на Unity</option>
                        <option value="pc">💻 Игра для ПК на Unity</option>
                        <option value="vr">👓 VR игра на Unity</option>
                        <option value="update">🔧 Доработка Unity игры</option>
                        <option value="other">✨ Другое</option>
                    </select>
                </div>
                
                <div class="form-group full-width">
                    <label for="message">💡 Опишите ваш проект</label>
                    <textarea id="message" rows="5" required></textarea>
                </div>
                
                <div class="form-group full-width" style="text-align: center;">
                    <button type="submit" class="btn">
                        <i class="fas fa-paper-plane"></i> 🚀 Отправить заявку
                    </button>
                </div>
            </form>
        </div>
    </section>

    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-about">
                    <div class="footer-logo">
                        <a href="#" class="logo">
                            <div class="logo-7">7</div>
                            <span class="logo-text">CORP</span>
                        </a>
                    </div>
                    <p>🚀 Студия разработки игр на Unity. Специализируемся на создании игр для мобильных устройств и ПК.</p>
                    
                    <div class="social-links">
                        <a href="https://t.me/sevencorp77" target="_blank"><i class="fab fa-telegram"></i></a>
                        <a href="https://www.avito.ru/yaroslavl/predlozheniya_uslug/razrabotka_igr_na_unity_7744285832" target="_blank"><i class="fas fa-store"></i></a>
                        <a href="#"><i class="fab fa-vk"></i></a>
                        <a href="#"><i class="fab fa-youtube"></i></a>
                    </div>
                </div>
                
                <div class="footer-links">
                    <h3>🧭 Навигация</h3>
                    <ul>
                        <li><a href="#home"><i class="fas fa-chevron-right"></i> 🏠 Главная</a></li>
                        <li><a href="#services"><i class="fas fa-chevron-right"></i> 🎮 Услуги</a></li>
                        <li><a href="#process"><i class="fas fa-chevron-right"></i> 📋 Процесс</a></li>
                        <li><a href="#technologies"><i class="fas fa-chevron-right"></i> ⚙️ Технологии</a></li>
                        <li><a href="#contact"><i class="fas fa-chevron-right"></i> 📞 Контакты</a></li>
                    </ul>
                </div>
                
                <div class="footer-contact">
                    <h3>📱 Контакты</h3>
                    <p><i class="fab fa-telegram"></i> 💬 Telegram: @sevencorp77</p>
                    <p><i class="fas fa-store"></i> 🛒 Авито: разработка игр на Unity</p>
                    <p><i class="fas fa-envelope"></i> 📧 sevencorp565@gmail.com</p>
                    <p><i class="fas fa-map-marker-alt"></i> 📍 Россия, Ярославль</p>
                </div>
            </div>
            
            <div class="copyright">
                <p>&copy; 2024 7Corp. Все права защищены.</p>
            </div>
        </div>
    </footer>

    <script>
        const header = document.getElementById('header');
        window.addEventListener('scroll', () => {
            if (window.scrollY > 100) {
                header.classList.add('scrolled');
            } else {
                header.classList.remove('scrolled');
            }
        });

        const mobileMenuBtn = document.getElementById('mobileMenuBtn');
        const navMenu = document.getElementById('navMenu');

        mobileMenuBtn.addEventListener('click', () => {
            navMenu.classList.toggle('active');
            mobileMenuBtn.innerHTML = navMenu.classList.contains('active') 
                ? '<i class="fas fa-times"></i>' 
                : '<i class="fas fa-bars"></i>';
        });

        document.querySelectorAll('nav ul li a').forEach(link => {
            link.addEventListener('click', () => {
                navMenu.classList.remove('active');
                mobileMenuBtn.innerHTML = '<i class="fas fa-bars"></i>';
            });
        });

        const contactForm = document.getElementById('contactForm');
        
        contactForm.addEventListener('submit', (e) => {
            e.preventDefault();
            
            const formData = {
                name: document.getElementById('name').value,
                contact: document.getElementById('contact').value,
                projectType: document.getElementById('projectType').value,
                message: document.getElementById('message').value
            };
            
            alert(`Спасибо, ${formData.name}! Ваша заявка отправлена. Мы свяжемся с вами в ближайшее время.`);
            
            contactForm.reset();
            
            const telegramMessage = `Новая заявка от ${formData.name}%0AКонтакт: ${formData.contact}%0AТип проекта: ${formData.projectType}%0AСообщение: ${formData.message}`;
            window.open(`https://t.me/sevencorp77?text=${telegramMessage}`, '_blank');
        });

        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                if (targetId === '#') return;
                
                const targetElement = document.querySelector(targetId);
                if (targetElement) {
                    window.scrollTo({
                        top: targetElement.offsetTop - 80,
                        behavior: 'smooth'
                    });
                }
            });
        });

        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = '1';
                    entry.target.style.transform = 'translateY(0)';
                }
            });
        }, observerOptions);

        document.querySelectorAll('.service-card, .process-step, .tech-item, .contact-badge').forEach(el => {
            el.style.opacity = '0';
            el.style.transform = 'translateY(30px)';
            el.style.transition = 'opacity 0.6s ease, transform 0.6s ease';
            observer.observe(el);
        });

        const logo7 = document.querySelector('.logo-7');
        
        logo7.addEventListener('mouseenter', () => {
            logo7.style.animation = 'logoGlow 0.5s infinite alternate';
        });
        
        logo7.addEventListener('mouseleave', () => {
            logo7.style.animation = 'logoGlow 3s infinite alternate';
        });

        const techEmojis = document.querySelectorAll('.tech-emoji');
        
        techEmojis.forEach(emoji => {
            emoji.addEventListener('mouseenter', function() {
                this.style.transform = 'scale(1.3) rotate(10deg)';
            });
            
            emoji.addEventListener('mouseleave', function() {
                this.style.transform = 'scale(1) rotate(0deg)';
            });
        });

        console.log('🎮 7Corp - создаём игры на Unity! 🚀');
    </script>
</body>
</html>
