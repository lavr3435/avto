<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PremiumAuto - Автосалон премиум автомобилей</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;500;700&family=Montserrat:wght@400;500;700&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Roboto', sans-serif;
            color: #333;
            line-height: 1.6;
            background-color: #f8f9fa;
        }
        
        h1, h2, h3, h4 {
            font-family: 'Montserrat', sans-serif;
            font-weight: 700;
            color: #1a1a1a;
        }
        
        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 15px;
        }
        
        /* Header Styles */
        header {
            background: linear-gradient(to right, #1a1a1a, #2c3e50);
            color: white;
            padding: 15px 0;
            position: sticky;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.2);
        }
        
        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            display: flex;
            align-items: center;
        }
        
        .logo img {
            height: 50px;
            margin-right: 10px;
        }
        
        .logo h1 {
            color: white;
            font-size: 24px;
        }
        
        .logo span {
            color: #ff9900;
        }
        
        nav ul {
            display: flex;
            list-style: none;
        }
        
        nav ul li {
            margin-left: 25px;
        }
        
        nav ul li a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
        }
        
        nav ul li a:hover {
            color: #ff9900;
        }
        
        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.7)), url('https://images.unsplash.com/photo-1533473359331-0135ef1b58bf?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1770&q=80') no-repeat center center/cover;
            color: white;
            text-align: center;
            padding: 100px 0;
        }
        
        .hero h2 {
            font-size: 3rem;
            margin-bottom: 20px;
            color: white;
        }
        
        .hero p {
            font-size: 1.2rem;
            max-width: 700px;
            margin: 0 auto 30px;
        }
        
        .btn {
            display: inline-block;
            background: #ff9900;
            color: white;
            padding: 12px 30px;
            border: none;
            border-radius: 5px;
            font-size: 1rem;
            font-weight: 500;
            cursor: pointer;
            transition: background 0.3s, transform 0.3s;
            text-decoration: none;
        }
        
        .btn:hover {
            background: #e68a00;
            transform: translateY(-2px);
        }
        
        /* Featured Cars */
        .section-title {
            text-align: center;
            margin: 50px 0 30px;
            position: relative;
        }
        
        .section-title::after {
            content: '';
            display: block;
            width: 80px;
            height: 4px;
            background: #ff9900;
            margin: 15px auto;
            border-radius: 2px;
        }
        
        .cars-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin: 40px 0;
        }
        
        .car-card {
            background: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s;
        }
        
        .car-card:hover {
            transform: translateY(-10px);
        }
        
        .car-image {
            height: 200px;
            overflow: hidden;
        }
        
        .car-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s;
        }
        
        .car-card:hover .car-image img {
            transform: scale(1.1);
        }
        
        .car-info {
            padding: 20px;
        }
        
        .car-info h3 {
            margin-bottom: 10px;
            font-size: 1.4rem;
        }
        
        .car-details {
            display: flex;
            justify-content: space-between;
            margin: 15px 0;
            color: #666;
        }
        
        .car-price {
            font-size: 1.3rem;
            font-weight: 700;
            color: #2c3e50;
            margin: 10px 0;
        }
        
        /* Services */
        .services {
            background: #2c3e50;
            color: white;
            padding: 60px 0;
        }
        
        .services .section-title {
            color: white;
        }
        
        .services .section-title::after {
            background: #ff9900;
        }
        
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 25px;
        }
        
        .service-card {
            background: rgba(255, 255, 255, 0.1);
            padding: 25px;
            border-radius: 10px;
            text-align: center;
            transition: transform 0.3s;
        }
        
        .service-card:hover {
            transform: translateY(-5px);
        }
        
        .service-icon {
            font-size: 2.5rem;
            color: #ff9900;
            margin-bottom: 15px;
        }
        
        /* About */
        .about {
            padding: 60px 0;
        }
        
        .about-content {
            display: flex;
            align-items: center;
            gap: 40px;
        }
        
        .about-text {
            flex: 1;
        }
        
        .about-image {
            flex: 1;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        .about-image img {
            width: 100%;
            height: auto;
            display: block;
        }
        
        /* Testimonials */
        .testimonials {
            background: #f1f1f1;
            padding: 60px 0;
        }
        
        .testimonials-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 25px;
        }
        
        .testimonial-card {
            background: white;
            padding: 25px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
        }
        
        .testimonial-text {
            font-style: italic;
            margin-bottom: 15px;
        }
        
        .testimonial-author {
            display: flex;
            align-items: center;
        }
        
        .author-image {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            overflow: hidden;
            margin-right: 15px;
        }
        
        .author-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        
        /* Contact */
        .contact {
            padding: 60px 0;
        }
        
        .contact-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 40px;
        }
        
        .contact-info {
            display: flex;
            flex-direction: column;
            gap: 20px;
        }
        
        .contact-item {
            display: flex;
            align-items: center;
            gap: 15px;
        }
        
        .contact-icon {
            width: 40px;
            height: 40px;
            background: #ff9900;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 1.2rem;
        }
        
        .contact-form {
            background: white;
            padding: 25px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        .form-group {
            margin-bottom: 20px;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 5px;
            font-weight: 500;
        }
        
        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 12px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-family: 'Roboto', sans-serif;
        }
        
        .form-group textarea {
            height: 120px;
            resize: vertical;
        }
        
        /* Footer */
        footer {
            background: #1a1a1a;
            color: white;
            padding: 40px 0 20px;
        }
        
        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
            margin-bottom: 30px;
        }
        
        .footer-column h3 {
            color: white;
            margin-bottom: 20px;
            font-size: 1.2rem;
        }
        
        .footer-column ul {
            list-style: none;
        }
        
        .footer-column ul li {
            margin-bottom: 10px;
        }
        
        .footer-column ul li a {
            color: #ccc;
            text-decoration: none;
            transition: color 0.3s;
        }
        
        .footer-column ul li a:hover {
            color: #ff9900;
        }
        
        .social-links {
            display: flex;
            gap: 15px;
        }
        
        .social-links a {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            background: #333;
            border-radius: 50%;
            color: white;
            text-decoration: none;
            transition: background 0.3s;
        }
        
        .social-links a:hover {
            background: #ff9900;
        }
        
        .copyright {
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid #333;
            color: #ccc;
            font-size: 0.9rem;
        }
        
        /* Responsive */
        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
                text-align: center;
            }
            
            nav ul {
                margin-top: 15px;
                justify-content: center;
            }
            
            nav ul li {
                margin: 0 10px;
            }
            
            .hero h2 {
                font-size: 2rem;
            }
            
            .about-content {
                flex-direction: column;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container">
            <div class="header-content">
                <div class="logo">
                    <h1>Premium<span>Auto</span></h1>
                </div>
                <nav>
                    <ul>
                        <li><a href="#home">Главная</a></li>
                        <li><a href="#cars">Автомобили</a></li>
                        <li><a href="#services">Услуги</a></li>
                        <li><a href="#about">О нас</a></li>
                        <li><a href="#contact">Контакты</a></li>
                    </ul>
                </nav>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="container">
            <h2>Найдите свой идеальный автомобиль</h2>
            <p>Широкий выбор премиальных автомобилей от ведущих мировых производителей с гарантией качества и лучшими условиями покупки</p>
            <a href="#cars" class="btn">Посмотреть каталог</a>
        </div>
    </section>

    <!-- Featured Cars -->
    <section class="featured-cars" id="cars">
        <div class="container">
            <h2 class="section-title">Популярные модели</h2>
            <div class="cars-grid">
                <div class="car-card">
                    <div class="car-image">
                        <img src="https://images.unsplash.com/photo-1542362567-b07e54358753?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1770&q=80" alt="BMW X5">
                    </div>
                    <div class="car-info">
                        <h3>BMW X5</h3>
                        <div class="car-details">
                            <span><i class="fas fa-calendar-alt"></i> 2023 г.</span>
                            <span><i class="fas fa-gas-pump"></i> Бензин</span>
                            <span><i class="fas fa-tachometer-alt"></i> 15 000 км</span>
                        </div>
                        <div class="car-price">5 200 000 ₽</div>
                        <a href="#" class="btn">Подробнее</a>
                    </div>
                </div>
                
                <div class="car-card">
                    <div class="car-image">
                        <img src="https://images.unsplash.com/photo-1549399542-7e821f5fdb6e?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1770&q=80" alt="Audi Q7">
                    </div>
                    <div class="car-info">
                        <h3>Audi Q7</h3>
                        <div class="car-details">
                            <span><i class="fas fa-calendar-alt"></i> 2022 г.</span>
                            <span><i class="fas fa-gas-pump"></i> Дизель</span>
                            <span><i class="fas fa-tachometer-alt"></i> 25 000 км</span>
                        </div>
                        <div class="car-price">4 800 000 ₽</div>
                        <a href="#" class="btn">Подробнее</a>
                    </div>
                </div>
                
                <div class="car-card">
                    <div class="car-image">
                        <img src="https://images.unsplash.com/photo-1503376780353-7e6692767b70?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1770&q=80" alt="Porsche 911">
                    </div>
                    <div class="car-info">
                        <h3>Porsche 911</h3>
                        <div class="car-details">
                            <span><i class="fas fa-calendar-alt"></i> 2023 г.</span>
                            <span><i class="fas fa-gas-pump"></i> Бензин</span>
                            <span><i class="fas fa-tachometer-alt"></i> 8 000 км</span>
                        </div>
                        <div class="car-price">8 900 000 ₽</div>
                        <a href="#" class="btn">Подробнее</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Services -->
    <section class="services" id="services">
        <div class="container">
            <h2 class="section-title">Наши услуги</h2>
            <div class="services-grid">
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-car"></i>
                    </div>
                    <h3>Продажа автомобилей</h3>
                    <p>Широкий выбор новых и подержанных автомобилей премиум-класса</p>
                </div>
                
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-exchange-alt"></i>
                    </div>
                    <h3>Трейд-ин</h3>
                    <p>Выгодный обмен вашего текущего автомобиля на новый</p>
                </div>
                
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-wrench"></i>
                    </div>
                    <h3>Сервис и обслуживание</h3>
                    <p>Качественное обслуживание и ремонт автомобилей любого класса</p>
                </div>
                
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-file-signature"></i>
                    </div>
                    <h3>Автострахование</h3>
                    <p>Помощь в оформлении всех видов страхования на выгодных условиях</p>
                </div>
            </div>
        </div>
    </section>

    <!-- About -->
    <section class="about" id="about">
        <div class="container">
            <h2 class="section-title">О нашем салоне</h2>
            <div class="about-content">
                <div class="about-text">
                    <p>PremiumAuto - это автосалон премиум-класса, который предлагает своим клиентам лучшие автомобили от мировых производителей. Мы работаем на рынке с 2010 года и за это время заслужили репутацию надежного партнера.</p>
                    <p>Наш showroom расположен в центре города и предлагает comfortable зону ожидания, где вы можете насладиться чашечкой кофе пока наши специалисты подберут для вас идеальный автомобиль.</p>
                    <p>Мы предлагаем полный комплекс услуг: от помощи в выборе автомобиля и оформления кредита до страхования и сервисного обслуживания.</p>
                    <a href="#contact" class="btn">Связаться с нами</a>
                </div>
                <div class="about-image">
                    <img src="https://images.unsplash.com/photo-1560518883-ce09059eeffa?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1673&q=80" alt="Автосалон PremiumAuto">
                </div>
            </div>
        </div>
    </section>

    <!-- Testimonials -->
    <section class="testimonials">
        <div class="container">
            <h2 class="section-title">Отзывы клиентов</h2>
            <div class="testimonials-grid">
                <div class="testimonial-card">
                    <div class="testimonial-text">
                        "Приобрел BMW X5 в салоне PremiumAuto. Остался очень доволен профессиональным подходом менеджеров и условиями покупки. Машина полностью соответствует описанию."
                    </div>
                    <div class="testimonial-author">
                        <div class="author-image">
                            <img src="https://randomuser.me/api/portraits/men/32.jpg" alt="Дмитрий Иванов">
                        </div>
                        <div>
                            <h4>Дмитрий Иванов</h4>
                            <p>Клиент</p>
                        </div>
                    </div>
                </div>
                
                <div class="testimonial-card">
                    <div class="testimonial-text">
                        "Обслуживаю свой Mercedes в этом салоне уже несколько лет. Всегда качественный сервис, вежливый персонал и адекватные цены. Рекомендую!"
                    </div>
                    <div class="testimonial-author">
                        <div class="author-image">
                            <img src="https://randomuser.me/api/portraits/women/44.jpg" alt="Елена Смирнова">
                        </div>
                        <div>
                            <h4>Елена Смирнова</h4>
                            <p>Клиент</p>
                        </div>
                    </div>
                </div>
                
                <div class="testimonial-card">
                    <div class="testimonial-text">
                        "Порадовала возможность trade-in. Сдал старую Audi, добавил разницу и стал владельцем нового Porsche. Весь процесс занял минимум времени."
                    </div>
                    <div class="testimonial-author">
                        <div class="author-image">
                            <img src="https://randomuser.me/api/portraits/men/62.jpg" alt="Александр Петров">
                        </div>
                        <div>
                            <h4>Александр Петров</h4>
                            <p>Клиент</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact -->
    <section class="contact" id="contact">
        <div class="container">
            <h2 class="section-title">Контакты</h2>
            <div class="contact-content">
                <div class="contact-info">
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-map-marker-alt"></i>
                        </div>
                        <div>
                            <h3>Адрес</h3>
                            <p>г. Москва, Ленинский проспект, д. 42</p>
                        </div>
                    </div>
                    
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-phone"></i>
                        </div>
                        <div>
                            <h3>Телефон</h3>
                            <p>+7 (495) 123-45-67</p>
                        </div>
                    </div>
                    
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-envelope"></i>
                        </div>
                        <div>
                            <h3>Email</h3>
                            <p>info@premiumauto.ru</p>
                        </div>
                    </div>
                    
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-clock"></i>
                        </div>
                        <div>
                            <h3>Время работы</h3>
                            <p>Пн-Пт: 9:00 - 21:00<br>Сб-Вс: 10:00 - 20:00</p>
                        </div>
                    </div>
                </div>
                
                <div class="contact-form">
                    <h3>Оставить заявку</h3>
                    <form>
                        <div class="form-group">
                            <label for="name">Ваше имя</label>
                            <input type="text" id="name" placeholder="Введите ваше имя" required>
                        </div>
                        
                        <div class="form-group">
                            <label for="phone">Телефон</label>
                            <input type="tel" id="phone" placeholder="+7 (XXX) XXX-XX-XX" required>
                        </div>
                        
                        <div class="form-group">
                            <label for="email">Email</label>
                            <input type="email" id="email" placeholder="Введите ваш email" required>
                        </div>
                        
                        <div class="form-group">
                            <label for="message">Сообщение</label>
                            <textarea id="message" placeholder="Введите ваше сообщение"></textarea>
                        </div>
                        
                        <button type="submit" class="btn">Отправить заявку</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-column">
                    <h3>PremiumAuto</h3>
                    <p>Автосалон премиум-класса с лучшим выбором автомобилей и качественным сервисом.</p>
                    <div class="social-links">
                        <a href="#"><i class="fab fa-vk"></i></a>
                        <a href="#"><i class="fab fa-telegram"></i></a>
                        <a href="#"><i class="fab fa-youtube"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                    </div>
                </div>
                
                <div class="footer-column">
                    <h3>Автомобили</h3>
                    <ul>
                        <li><a href="#">Новые автомобили</a></li>
                        <li><a href="#">Автомобили с пробегом</a></li>
                        <li><a href="#">Электромобили</a></li>
                        <li><a href="#">Спецпредложения</a></li>
                    </ul>
                </div>
                
                <div class="footer-column">
                    <h3>Услуги</h3>
                    <ul>
                        <li><a href="#">Трейд-ин</a></li>
                        <li><a href="#">Автокредит</a></li>
                        <li><a href="#">Страхование</a></li>
                        <li><a href="#">Сервис и ремонт</a></li>
                    </ul>
                </div>
                
                <div class="footer-column">
                    <h3>Контакты</h3>
                    <ul>
                        <li><i class="fas fa-map-marker-alt"></i> г. Москва, Ленинский проспект, д. 42</li>
                        <li><i class="fas fa-phone"></i> +7 (495) 123-45-67</li>
                        <li><i class="fas fa-envelope"></i> info@premiumauto.ru</li>
                    </ul>
                </div>
            </div>
            
            <div class="copyright">
                <p>&copy; 2023 PremiumAuto. Все права защищены.</p>
            </div>
        </div>
    </footer>

    <script>
        // Плавная прокрутка для навигационных ссылок
        document.querySelectorAll('nav a, .btn[href^="#"]').forEach(anchor => {
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
        
        // Обработка формы
        const contactForm = document.querySelector('.contact-form form');
        if (contactForm) {
            contactForm.addEventListener('submit', function(e) {
                e.preventDefault();
                alert('Спасибо! Ваша заявка отправлена. Мы свяжемся с вами в ближайшее время.');
                this.reset();
            });
        }
        
        // Маска для телефона
        const phoneInput = document.getElementById('phone');
        if (phoneInput) {
            phoneInput.addEventListener('input', function(e) {
                const x = e.target.value.replace(/\D/g, '').match(/(\d{0,1})(\d{0,3})(\d{0,3})(\d{0,2})(\d{0,2})/);
                e.target.value = '+7' + (x[2] ? ' (' + x[2] : '') + (x[3] ? ') ' + x[3] : '') + (x[4] ? '-' + x[4] : '') + (x[5] ? '-' + x[5] : '');
            });
        }
    </script>
</body>
</html>
