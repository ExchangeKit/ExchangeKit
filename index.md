<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ExchangeKit | Crypto Development Tools</title>
    <style>
        :root {
            --bg-gradient: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            --bg-light: #f8f9fa;
            --text-dark: #212529;
            --text-light: #ffffff;
            --accent-primary: #6f42c1;
            --accent-secondary: #00b4d8;
            --accent-success: #20c997;
            --card-bg: rgba(255, 255, 255, 0.95);
            --card-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            --transition: all 0.3s ease;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Inter', 'Segoe UI', sans-serif;
        }

        body {
            background: var(--bg-gradient);
            color: var(--text-dark);
            line-height: 1.6;
            min-height: 100vh;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 2rem;
        }

        /* Header & Hero */
        .hero {
            text-align: center;
            padding: 5rem 1rem;
            color: var(--text-light);
        }

        .hero-content {
            max-width: 800px;
            margin: 0 auto;
        }

        .hero h1 {
            font-size: 4rem;
            font-weight: 800;
            margin-bottom: 1.5rem;
            background: linear-gradient(135deg, #ff6b6b 0%, #ee5a24 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            text-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
        }

        .hero p {
            font-size: 1.4rem;
            margin-bottom: 2rem;
            opacity: 0.9;
        }

        .badges {
            display: flex;
            justify-content: center;
            gap: 1rem;
            flex-wrap: wrap;
            margin: 2rem 0;
        }

        .badge {
            background: rgba(255, 255, 255, 0.2);
            backdrop-filter: blur(10px);
            color: var(--text-light);
            padding: 0.8rem 1.5rem;
            border-radius: 50px;
            border: 1px solid rgba(255, 255, 255, 0.3);
            font-weight: 600;
            transition: var(--transition);
        }

        .badge:hover {
            transform: translateY(-2px);
            background: rgba(255, 255, 255, 0.3);
        }

        /* Navigation */
        .nav-links {
            display: flex;
            justify-content: center;
            gap: 2rem;
            margin: 3rem 0;
            flex-wrap: wrap;
        }

        .nav-links a {
            color: var(--text-light);
            text-decoration: none;
            font-weight: 600;
            font-size: 1.1rem;
            padding: 0.8rem 1.5rem;
            border: 2px solid rgba(255, 255, 255, 0.3);
            border-radius: 50px;
            transition: var(--transition);
        }

        .nav-links a:hover {
            background: rgba(255, 255, 255, 0.1);
            transform: translateY(-2px);
        }

        /* Content Sections */
        .section {
            background: var(--card-bg);
            border-radius: 20px;
            padding: 3rem;
            margin: 3rem 0;
            box-shadow: var(--card-shadow);
            backdrop-filter: blur(10px);
        }

        h2 {
            font-size: 2.5rem;
            text-align: center;
            margin-bottom: 2rem;
            color: var(--accent-primary);
            font-weight: 700;
        }

        h3 {
            font-size: 1.5rem;
            color: var(--accent-secondary);
            margin: 1.5rem 0 1rem;
        }

        /* Projects Grid */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 2rem;
            margin-top: 2rem;
        }

        .project-card {
            background: var(--card-bg);
            border-radius: 15px;
            padding: 2rem;
            box-shadow: var(--card-shadow);
            transition: var(--transition);
            border: 1px solid rgba(255, 255, 255, 0.5);
        }

        .project-card:hover {
            transform: translateY(-5px) scale(1.02);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.15);
        }

        .project-card h4 {
            font-size: 1.4rem;
            color: var(--accent-primary);
            margin-bottom: 1rem;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .project-status {
            font-size: 0.8rem;
            padding: 0.3rem 0.8rem;
            border-radius: 20px;
            font-weight: bold;
        }
        .status-stable { background: var(--accent-success); color: white; }
        .status-beta { background: #fd7e14; color: white; }
        .status-alpha { background: #dc3545; color: white; }

        .stack {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
            margin: 1rem 0;
        }

        .stack-item {
            background: linear-gradient(135deg, var(--accent-primary), var(--accent-secondary));
            color: white;
            padding: 0.3rem 0.8rem;
            border-radius: 15px;
            font-size: 0.8rem;
            font-weight: 600;
        }

        .btn {
            display: inline-block;
            padding: 0.8rem 1.5rem;
            background: linear-gradient(135deg, var(--accent-primary), var(--accent-secondary));
            color: white;
            text-decoration: none;
            border-radius: 50px;
            font-weight: 600;
            transition: var(--transition);
            margin-top: 1rem;
        }

        .btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(111, 66, 193, 0.4);
        }

        /* Tech Stack */
        .tech-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
        }

        .tech-category {
            text-align: center;
            padding: 1.5rem;
        }

        .tech-icons {
            font-size: 2.5rem;
            margin-bottom: 1rem;
        }

        /* Contact */
        .contact-links {
            display: flex;
            justify-content: center;
            gap: 1.5rem;
            margin-top: 2rem;
            flex-wrap: wrap;
        }

        .contact-btn {
            padding: 1rem 2rem;
            background: linear-gradient(135deg, #ff6b6b, #ee5a24);
            color: white;
            text-decoration: none;
            border-radius: 50px;
            font-weight: 600;
            transition: var(--transition);
        }

        .contact-btn:hover {
            transform: translateY(-3px) scale(1.05);
            box-shadow: 0 10px 25px rgba(255, 107, 107, 0.4);
        }

        /* Footer */
        footer {
            text-align: center;
            padding: 2rem;
            color: var(--text-light);
            margin-top: 4rem;
        }

        /* Animations */
        @keyframes float {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-10px); }
        }

        .project-card {
            animation: float 3s ease-in-out infinite;
        }

        .project-card:nth-child(2) { animation-delay: 0.5s; }
        .project-card:nth-child(3) { animation-delay: 1s; }

        /* Responsive */
        @media (max-width: 768px) {
            .hero h1 { font-size: 2.5rem; }
            .hero p { font-size: 1.1rem; }
            .projects-grid { grid-template-columns: 1fr; }
            .nav-links { gap: 1rem; }
            .nav-links a { padding: 0.6rem 1.2rem; }
            .contact-links { flex-direction: column; }
            .section { padding: 2rem; }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Hero Section -->
        <header class="hero">
            <div class="hero-content">
                <h1>ExchangeKit</h1>
                <p>Мощные инструменты для автоматизации криптотрейдинга</p>
                <p>Создано трейдером для трейдеров</p>
                
                <div class="badges">
                    <span class="badge">🚀 Высокая производительность</span>
                    <span class="badge">🔐 Безопасность</span>
                    <span class="badge">⚡ Мгновенное исполнение</span>
                </div>

                <div class="nav-links">
                    <a href="#about">Обо мне</a>
                    <a href="#projects">Проекты</a>
                    <a href="#stack">Технологии</a>
                    <a href="#contact">Контакты</a>
                </div>
            </div>
        </header>

        <!-- About Section -->
        <section id="about" class="section">
            <h2>✨ Обо мне</h2>
            <div class="about-content">
                <p>Привет! Я занимаюсь криптовалютами более 8 лет и создаю инструменты, которые делают трейдинг эффективнее.</p>
                <p>Мои проекты — это результат тысяч часов практики, тестирования и оптимизации. Я верю в open-source и делюсь своими лучшими наработками.</p>
                <div class="stack">
                    <span class="stack-item">🎯 Практический опыт</span>
                    <span class="stack-item">⚡ Высокая производительность</span>
                    <span class="stack-item">🔓 Open-Source</span>
                </div>
            </div>
        </section>

        <!-- Projects Section -->
        <section id="projects" class="section">
            <h2>🚀 Мои проекты</h2>
            <div class="projects-grid">
                <div class="project-card">
                    <h4>⚡ Universal API <span class="project-status status-stable">stable</span></h4>
                    <p>Единый интерфейс для работы с Binance, Bybit, OKX и другими биржами. Асинхронный и молниеносный.</p>
                    <div class="stack">
                        <span class="stack-item">Python</span>
                        <span class="stack-item">aiohttp</span>
                        <span class="stack-item">WebSocket</span>
                    </div>
                    <a href="https://github.com/ExchangeKit/universal-exchange-api" class="btn">Исследовать код</a>
                </div>

                <div class="project-card">
                    <h4>📊 Portfolio Tracker <span class="project-status status-beta">beta</span></h4>
                    <p>Мгновенный трекинг портфеля across multiple exchanges. Красивые графики и детальная аналитика.</p>
                    <div class="stack">
                        <span class="stack-item">React</span>
                        <span class="stack-item">TypeScript</span>
                        <span class="stack-item">Chart.js</span>
                    </div>
                    <a href="https://github.com/ExchangeKit/crypto-portfolio-tracker" class="btn">Исследовать код</a>
                </div>

                <div class="project-card">
                    <h4>🤖 Trading Bot <span class="project-status status-alpha">alpha</span></h4>
                    <p>Модульный trading bot с поддержкой арбитража, market-making и следования за трендом.</p>
                    <div class="stack">
                        <span class="stack-item">Python</span>
                        <span class="stack-item">NumPy</span>
                        <span class="stack-item">Pandas</span>
                    </div>
                    <a href="https://github.com/ExchangeKit/trading-bot" class="btn">Исследовать код</a>
                </div>
            </div>
        </section>

        <!-- Tech Stack Section -->
        <section id="stack" class="section">
            <h2>🛠 Технологический стек</h2>
            <div class="tech-grid">
                <div class="tech-category">
                    <div class="tech-icons">🐍</div>
                    <h3>Backend</h3>
                    <p>Python 3.10+, Asyncio, FastAPI, aiohttp, Web3.py</p>
                </div>
                <div class="tech-category">
                    <div class="tech-icons">⚡</div>
                    <h3>Performance</h3>
                    <p>Rust, C++, Multiprocessing, Redis, ZeroMQ</p>
                </div>
                <div class="tech-category">
                    <div class="tech-icons">🔗</div>
                    <h3>Blockchain</h3>
                    <p>Ethereum, Polygon, Web3, Smart Contracts, Hardhat</p>
                </div>
            </div>
        </section>

        <!-- Contact Section -->
        <section id="contact" class="section">
            <h2>📞 Давайте работать вместе</h2>
            <p style="text-align: center; margin-bottom: 2rem;">Всегда открыт для коллабораций, идей и интересных проектов</p>
            
            <div class="contact-links">
                <a href="https://github.com/ExchangeKit" class="contact-btn">⭐ GitHub</a>
                <a href="https://t.me/your_channel" class="contact-btn">📢 Telegram</a>
                <a href="mailto:your-email@example.com" class="contact-btn">✉️ Email</a>
            </div>
        </section>
    </div>

    <footer>
        <p>© 2024 ExchangeKit. Сделано с ❤️ и большим количеством кофе</p>
        <p>🚀 Преодолеваем границы возможного в крипто-автоматизации</p>
    </footer>
</body>
</html>
