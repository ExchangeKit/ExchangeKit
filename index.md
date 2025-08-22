<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ExchangeKit | Crypto Development Tools</title>
    <style>
        :root {
            --bg-primary: #0d1117;
            --bg-secondary: #161b22;
            --accent-primary: #0070f3;
            --accent-secondary: #00ffcc;
            --text-primary: #f0f6fc;
            --text-secondary: #c9d1d9;
            --card-bg: #21262d;
            --card-border: #30363d;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background-color: var(--bg-primary);
            color: var(--text-primary);
            line-height: 1.6;
            padding: 0;
            margin: 0;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 2rem;
        }

        /* Header & Hero */
        .hero {
            text-align: center;
            padding: 4rem 1rem;
            background: linear-gradient(135deg, var(--bg-secondary) 0%, var(--bg-primary) 100%);
            border-bottom: 1px solid var(--card-border);
        }

        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            background: linear-gradient(135deg, var(--accent-primary) 0%, var(--accent-secondary) 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .hero p {
            font-size: 1.5rem;
            color: var(--text-secondary);
            max-width: 800px;
            margin: 0 auto 2rem;
        }

        .badges {
            margin: 1rem 0;
        }

        .badge {
            display: inline-block;
            background-color: var(--card-bg);
            color: var(--text-secondary);
            padding: 0.3rem 0.7rem;
            margin: 0.3rem;
            border-radius: 20px;
            border: 1px solid var(--card-border);
            font-size: 0.9rem;
        }

        /* Navigation */
        .nav-links {
            display: flex;
            justify-content: center;
            gap: 2rem;
            margin: 2rem 0;
            flex-wrap: wrap;
        }

        .nav-links a {
            color: var(--accent-secondary);
            text-decoration: none;
            font-weight: 600;
            transition: color 0.3s ease;
        }

        .nav-links a:hover {
            color: var(--accent-primary);
        }

        /* Sections */
        section {
            margin: 4rem 0;
        }

        h2 {
            font-size: 2.2rem;
            margin-bottom: 2rem;
            color: var(--accent-primary);
            text-align: center;
        }

        h3 {
            font-size: 1.5rem;
            margin: 1.5rem 0 1rem;
            color: var(--accent-secondary);
        }

        /* About */
        .about {
            background-color: var(--bg-secondary);
            padding: 3rem;
            border-radius: 15px;
            border: 1px solid var(--card-border);
        }

        /* Projects Grid */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 2rem;
        }

        .project-card {
            background-color: var(--card-bg);
            border: 1px solid var(--card-border);
            border-radius: 10px;
            padding: 1.5rem;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .project-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0, 112, 243, 0.1);
        }

        .project-card h4 {
            font-size: 1.3rem;
            margin-bottom: 0.5rem;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .project-status {
            display: inline-block;
            font-size: 0.7rem;
            padding: 0.2rem 0.6rem;
            border-radius: 15px;
            margin-left: 0.5rem;
            font-weight: bold;
        }
        .status-stable { background: #2ea043; color: white; }
        .status-beta { background: #d29922; color: black; }
        .status-alpha { background: #da3633; color: white; }

        .stack {
            margin: 1rem 0;
        }

        .stack-item {
            display: inline-block;
            background-color: var(--bg-primary);
            color: var(--text-secondary);
            padding: 0.2rem 0.6rem;
            margin: 0.2rem;
            border-radius: 5px;
            font-size: 0.8rem;
            border: 1px solid var(--card-border);
        }

        /* Contact */
        .contact-links {
            display: flex;
            justify-content: center;
            gap: 2rem;
            margin-top: 2rem;
            flex-wrap: wrap;
        }

        .contact-btn {
            display: inline-block;
            padding: 0.8rem 1.5rem;
            background: linear-gradient(135deg, var(--accent-primary) 0%, var(--accent-secondary) 100%);
            color: white;
            text-decoration: none;
            border-radius: 30px;
            font-weight: bold;
            transition: transform 0.3s ease;
        }

        .contact-btn:hover {
            transform: scale(1.05);
        }

        /* Footer */
        footer {
            text-align: center;
            padding: 2rem;
            margin-top: 4rem;
            border-top: 1px solid var(--card-border);
            color: var(--text-secondary);
        }

        /* Responsive */
        @media (max-width: 768px) {
            .hero h1 { font-size: 2.5rem; }
            .hero p { font-size: 1.2rem; }
            .container { padding: 1rem; }
            .nav-links { gap: 1rem; }
            .projects-grid { grid-template-columns: 1fr; }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Hero Section -->
        <header class="hero">
            <h1>ExchangeKit</h1>
            <p>Набор высокопроизводительных инструментов и библиотек для взаимодействия с криптовалютными биржами</p>
            <p>Надежная автоматизация для трейдинга и анализа</p>
            
            <div class="badges">
                <span class="badge">Python</span>
                <span class="badge">Web3</span>
                <span class="badge">Asyncio</span>
                <span class="badge">REST API</span>
                <span class="badge">WebSocket</span>
                <span class="badge">Binance</span>
                <span class="badge">Bybit</span>
                <span class="badge">Arbitrage</span>
            </div>

            <div class="nav-links">
                <a href="#about">Обо мне</a>
                <a href="#projects">Проекты</a>
                <a href="#stack">Технологии</a>
                <a href="#contact">Контакты</a>
                <a href="https://github.com/ExchangeKit">GitHub</a>
            </div>
        </header>

        <!-- About Section -->
        <section id="about">
            <h2>Обо мне</h2>
            <div class="about">
                <p>Привет! Я — опытный разработчик и крипто-энтузиаст с более чем 8-летним опытом в индустрии. Я создаю <strong>надёжные и эффективные инструменты</strong> для автоматизации торговли, анализа рынка и работы с NFT.</p>
                <p>Мои проекты — это результат многолетней практики и желания поделиться решениями, которые реально работают и упрощают жизнь.</p>
                <p><strong>Моя философия:</strong> Чистый код, максимальная производительность и безопасность пользователя.</p>
            </div>
        </section>

        <!-- Projects Section -->
        <section id="projects">
            <h2>Ключевые проекты</h2>
            <div class="projects-grid">
                <div class="project-card">
                    <h4>universal-exchange-api <span class="project-status status-stable">stable</span></h4>
                    <p>Единый асинхронный клиент для API Binance, Bybit, OKX и других бирж. Основа для всех остальных инструментов.</p>
                    <div class="stack">
                        <span class="stack-item">Python</span>
                        <span class="stack-item">aiohttp</span>
                        <span class="stack-item">REST</span>
                        <span class="stack-item">WebSocket</span>
                    </div>
                    <a href="https://github.com/ExchangeKit/universal-exchange-api" class="contact-btn">Смотреть на GitHub</a>
                </div>

                <div class="project-card">
                    <h4>crypto-portfolio-tracker <span class="project-status status-beta">beta</span></h4>
                    <p>Консольный трекер портфеля, который агрегирует активы с нескольких бирж и кошельков в единую сводку.</p>
                    <div class="stack">
                        <span class="stack-item">Python</span>
                        <span class="stack-item">Requests</span>
                        <span class="stack-item">Tabulate</span>
                    </div>
                    <a href="https://github.com/ExchangeKit/crypto-portfolio-tracker" class="contact-btn">Смотреть на GitHub</a>
                </div>

                <div class="project-card">
                    <h4>nft-mint-automation <span class="project-status status-beta">beta</span></h4>
                    <p>Утилита для автоматизации участия в минтах на EVM-сетях (Ethereum, Polygon, Arbitrum).</p>
                    <div class="stack">
                        <span class="stack-item">Web3.py</span>
                        <span class="stack-item">Ethereum</span>
                        <span class="stack-item">Selenium</span>
                    </div>
                    <a href="https://github.com/ExchangeKit/nft-mint-automation" class="contact-btn">Смотреть на GitHub</a>
                </div>
            </div>
        </section>

        <!-- Tech Stack Section -->
        <section id="stack">
            <h2>Технологический стек</h2>
            <div class="projects-grid">
                <div class="project-card">
                    <h3>Бэкенд & Автоматизация</h3>
                    <div class="stack">
                        <span class="stack-item">Python 3.10+</span>
                        <span class="stack-item">Asyncio</span>
                        <span class="stack-item">aiohttp</span>
                        <span class="stack-item">CCXT</span>
                        <span class="stack-item">Web3.py</span>
                    </div>
                </div>

                <div class="project-card">
                    <h3>Инфраструктура</h3>
                    <div class="stack">
                        <span class="stack-item">Docker</span>
                        <span class="stack-item">Linux</span>
                        <span class="stack-item">Bash</span>
                        <span class="stack-item">Git</span>
                    </div>
                </div>

                <div class="project-card">
                    <h3>Биржи & Сети</h3>
                    <div class="stack">
                        <span class="stack-item">Binance API</span>
                        <span class="stack-item">Bybit API</span>
                        <span class="stack-item">OKX API</span>
                        <span class="stack-item">Ethereum</span>
                        <span class="stack-item">Polygon</span>
                    </div>
                </div>
            </div>
        </section>

        <!-- Contact Section -->
        <section id="contact">
            <h2>Связаться со мной</h2>
            <p style="text-align: center;">Есть вопросы, предложения или нашли баг? Я всегда открыт к общению!</p>
            
            <div class="contact-links">
                <a href="https://github.com/ExchangeKit" class="contact-btn">GitHub</a>
                <a href="https://t.me/your_channel" class="contact-btn">Telegram</a>
                <a href="mailto:your-email@example.com" class="contact-btn">Email</a>
            </div>
        </section>
    </div>

    <footer>
        <p>© 2024 ExchangeKit. Сделано с ❤️ для сообщества.</p>
    </footer>
</body>
</html>
