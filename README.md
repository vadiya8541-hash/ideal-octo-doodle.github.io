# ideal-octo-doodle.github.io
Site
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Дизайн интерьеров - Дизайн интерьеров</title>
    <style>
        /* CSS переменные для темной темы */
        :root {
            --marble-dark: #1a1a1a;
            --marble-light: #2a2a2a;
            --gray-dark: #333333;
            --gray-medium: #555555;
            --gray-light: #777777;
            --accent: #c9a87a;
            --text-light: #e0e0e0;
            --text-dark: #ffffff;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Arial', sans-serif;
            background-color: var(--marble-dark);
            color: var(--text-light);
            line-height: 1.6;
        }

        /* Header */
        header {
            background: linear-gradient(135deg, var(--marble-dark) 0%, var(--gray-dark) 100%);
            padding: 1rem 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 20px rgba(0,0,0,0.5);
        }

        .header-container {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 2rem;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: bold;
            color: var(--text-dark);
            text-decoration: none;
        }

        .logo span {
            color: var(--accent);
        }

        nav ul {
            display: flex;
            list-style: none;
        }

        nav ul li {
            margin-left: 2rem;
        }

        nav ul li a {
            color: var(--text-light);
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s ease;
        }

        nav ul li a:hover {
            color: var(--accent);
        }

        /* Hero Section */
        .hero {
            height: 100vh;
            background: linear-gradient(rgba(0,0,0,0.7), rgba(0,0,0,0.7)),
                        url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" width="100" height="100" viewBox="0 0 100 100"><rect width="100" height="100" fill="%231a1a1a"/><path d="M0 0L100 100M100 0L0 100" stroke="%232a2a2a" stroke-width="1"/></svg>');
            background-size: cover;
            background-position: center;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            padding: 0 2rem;
        }

        .hero-content h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            color: var(--text-dark);
        }

        .hero-content p {
            font-size: 1.2rem;
            margin-bottom: 2rem;
            color: var(--text-light);
        }

        .btn {
            display: inline-block;
            padding: 12px 30px;
            background-color: var(--accent);
            color: var(--marble-dark);
            text-decoration: none;
            border-radius: 5px;
            font-weight: bold;
            transition: all 0.3s ease;
        }

        .btn:hover {
            background-color: #b89768;
            transform: translateY(-2px);
        }

        /* Sections */
        section {
            padding: 5rem 2rem;
        }

        .section-title {
            text-align: center;
            margin-bottom: 3rem;
        }

        .section-title h2 {
            font-size: 2.5rem;
            color: var(--text-dark);
            margin-bottom: 1rem;
        }

        .section-title p {
            color: var(--gray-light);
            max-width: 600px;
            margin: 0 auto;
        }

        /* Services */
        .services {
            background-color: var(--marble-light);
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .service-card {
            background: var(--gray-dark);
            padding: 2rem;
            border-radius: 10px;
            text-align: center;
            transition: transform 0.3s ease;
        }

        .service-card:hover {
            transform: translateY(-10px);
        }

        .service-icon {
            font-size: 3rem;
            color: var(--accent);
            margin-bottom: 1rem;
        }

        .service-card h3 {
            margin-bottom: 1rem;
            color: var(--text-dark);
        }

        /* Portfolio */
        .portfolio-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 1.5rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .portfolio-item {
            position: relative;
            overflow: hidden;
            border-radius: 10px;
            height: 300px;
        }

        .portfolio-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.3s ease;
        }

        .portfolio-item:hover img {
            transform: scale(1.1);
        }

        .portfolio-overlay {
            position: absolute;
            bottom: 0;
            left: 0;
            right: 0;
            background: linear-gradient(transparent, rgba(0,0,0,0.9));
            padding: 2rem;
            color: white;
            transform: translateY(100%);
            transition: transform 0.3s ease;
        }

        .portfolio-item:hover .portfolio-overlay {
            transform: translateY(0);
        }

        /* About */
        .about {
            background-color: var(--marble-light);
        }

        .about-content {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
            align-items: center;
        }

        .about-text h3 {
            font-size: 2rem;
            margin-bottom: 1.5rem;
            color: var(--text-dark);
        }

        .about-text p {
            margin-bottom: 1.5rem;
            color: var(--text-light);
        }

        /* Contact */
        .contact-form {
            max-width: 600px;
            margin: 0 auto;
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            color: var(--text-dark);
        }

        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 12px;
            background-color: var(--gray-dark);
            border: 1px solid var(--gray-medium);
            border-radius: 5px;
            color: var(--text-light);
        }

        .form-group input:focus,
        .form-group textarea:focus {
            outline: none;
            border-color: var(--accent);
        }

        /* Footer */
        footer {
            background-color: var(--gray-dark);
            padding: 3rem 2rem;
            text-align: center;
        }

        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
        }

        .social-links {
            margin-bottom: 2rem;
        }

        .social-links a {
            color: var(--text-light);
            margin: 0 1rem;
            font-size: 1.5rem;
            transition: color 0.3s ease;
        }

        .social-links a:hover {
            color: var(--accent);
        }

        /* Responsive */
        @media (max-width: 768px) {
            .header-container {
                flex-direction: column;
                padding: 1rem;
            }

            nav ul {
                margin-top: 1rem;
            }

            nav ul li {
                margin: 0 0.5rem;
            }

            .hero-content h1 {
                font-size: 2.5rem;
            }

            .about-content {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="header-container">
            <a href="#" class="logo">Дизайн <span>интерьеров</span></a>
            <nav>
                <ul>
                    <li><a href="#home">Главная</a></li>
                    <li><a href="#services">Услуги</a></li>
                    <li><a href="#portfolio">Портфолио</a></li>
                    <li><a href="#about">О нас</a></li>
                    <li><a href="#contact">Контакты</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <div class="hero-content">
            <h1>Эксклюзивный дизайн интерьеров</h1>
            <p>Создаем пространства, которые вдохновляют и отражают вашу индивидуальность</p>
            <a href="#contact" class="btn">Начать проект</a>
        </div>
    </section>

    <!-- Services -->
    <section id="services" class="services">
        <div class="section-title">
            <h2>Наши услуги</h2>
            <p>Полный спектр услуг по дизайну интерьера для вашего комфорта</p>
        </div>
        <div class="services-grid">
            <div class="service-card">
                <div class="service-icon">🏠</div>
                <h3>Жилые интерьеры</h3>
                <p>Создаем уютные и функциональные пространства для вашего дома</p>
            </div>
            <div class="service-card">
                <div class="service-icon">🏢</div>
                <h3>Коммерческие проекты</h3>
                <p>Дизайн офисов, ресторанов и торговых помещений</p>
            </div>
            <div class="service-card">
                <div class="service-icon">🎨</div>
                <h3>Консультации</h3>
                <p>Профессиональные советы по планировке и оформлению</p>
            </div>
        </div>
    </section>

    <!-- Portfolio -->
    <section id="portfolio">
        <div class="section-title">
            <h2>Наши работы</h2>
            <p>Примеры реализованных проектов в темной эстетике</p>
        </div>
        <div class="portfolio-grid">
            <div class="portfolio-item">
                <img src="data:image/svg+xml,<svg xmlns='http://www.w3.org/2000/svg' width='400' height='300' viewBox='0 0 400 300'><rect width='400' height='300' fill='%232a2a2a'/><rect x='50' y='50' width='300' height='200' fill='%23333333'/><circle cx='200' cy='150' r='30' fill='%23c9a87a'/></svg>" alt="Проект 1">
                <div class="portfolio-overlay">
                    <h3>Лофт апартаменты</h3>
                    <p>Современный дизайн в индустриальном стиле</p>
                </div>
            </div>
            <div class="portfolio-item">
                <img src="data:image/svg+xml,<svg xmlns='http://www.w3.org/2000/svg' width='400' height='300' viewBox='0 0 400 300'><rect width='400' height='300' fill='%232a2a2a'/><rect x='50' y='50' width='300' height='200' fill='%23333333'/><polygon points='200,80 250,200 150,200' fill='%23c9a87a'/></svg>" alt="Проект 2">
                <div class="portfolio-overlay">
                    <h3>Минимализм</h3>
                    <p>Чистые линии и сдержанная палитра</p>
                </div>
            </div>
            <div class="portfolio-item">
                <img src="data:image/svg+xml,<svg xmlns='http://www.w3.org/2000/svg' width='400' height='300' viewBox='0 0 400 300'><rect width='400' height='300' fill='%232a2a2a'/><rect x='50' y='50' width='300' height='200' fill='%23333333'/><rect x='150' y='100' width='100' height='100' fill='%23c9a87a'/></svg>" alt="Проект 3">
                <div class="portfolio-overlay">
                    <h3>Премиум резиденция</h3>
                    <p>Роскошный дизайн с элементами ар-деко</p>
                </div>
            </div>
        </div>
    </section>

    <!-- About -->
    <section id="about" class="about">
        <div class="section-title">
            <h2>О нашей студии</h2>
            <p>Профессионалы в создании уникальных интерьеров</p>
        </div>
        <div class="about-content">
            <div class="about-text">
                <h3>Дизайн Интерьеров - Эксперты в темной эстетике</h3>
                <p>Мы специализируемся на создании смелых, современных интерьеров с акцентом на темные тона, текстуры и премиальные материалы.</p>
                <p>Наш подход сочетает в себе функциональность, комфорт и визуальную гармонию, создавая пространства, которые действительно вдохновляют.</p>
                <a href="#contact" class="btn">Связаться с нами</a>
            </div>
            <div class="about-image">
                <img src="data:image/svg+xml,<svg xmlns='http://www.w3.org/2000/svg' width='500' height='300' viewBox='0 0 500 300'><rect width='500' height='300' fill='%23333333'/><circle cx='250' cy='150' r='80' fill='%231a1a1a'/><text x='250' y='160' text-anchor='middle' fill='%23c9a87a' font-size='24' font-weight='bold'>DD</text></svg>" alt="О нас">
            </div>
        </div>
    </section>

    <!-- Contact -->
    <section id="contact">
        <div class="section-title">
            <h2>Свяжитесь с нами</h2>
            <p>Готовы начать ваш проект? Напишите нам!</p>
        </div>
        <form class="contact-form">
            <div class="form-group">
                <label for="name">Имя</label>
                <input type="text" id="name" name="name" required>
            </div>
            <div class="form-group">
                <label for="email">Email</label>
                <input type="email" id="email" name="email" required>
            </div>
            <div class="form-group">
                <label for="message">Сообщение</label>
                <textarea id="message" name="message" rows="5" required></textarea>
            </div>
            <button type="submit" class="btn">Отправить сообщение</button>
        </form>
    </section>

    <!-- Footer -->
    <footer>
        <div class="footer-content">
            <div class="social-links">
                <a href="#">📘</a>
                <a href="#">📷</a>
                <a href="#">💼</a>
                <a href="#">🐦</a>
            </div>
            <p>&copy; 2024 Дизайн Интерьеров. Все права защищены.</p>
            <p>Элитный дизайн интерьеров в темной палитре</p>
        </div>
    </footer>

    <script>
        // Плавная прокрутка для навигации
        document.querySelectorAll('nav a').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const targetId = this.getAttribute('href');
                const targetElement = document.querySelector(targetId);
                targetElement.scrollIntoView({
                    behavior: 'smooth',
                    block: 'start'
                });
            });
        });

        // Анимация появления элементов при скролле
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

        // Наблюдаем за карточками услуг и портфолио
        document.querySelectorAll('.service-card, .portfolio-item').forEach(el => {
            el.style.opacity = '0';
            el.style.transform = 'translateY(20px)';
            el.style.transition = 'opacity 0.6s ease, transform 0.6s ease';
            observer.observe(el);
        });
    </script>
</body>
</html>
