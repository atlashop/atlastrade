<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Atlas Trade - Advanced Trading Platform</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        /* الأساسيات */
        :root {
            --primary: #0f2b5b;
            --secondary: #f4b400;
            --accent: #00a86b;
            --light: #f8f9fa;
            --dark: #343a40;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background-color: #f5f7fa;
            color: var(--dark);
            line-height: 1.6;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* شريط اللغات */
        .language-bar {
            background: var(--dark);
            color: white;
            padding: 0.5rem 0;
            text-align: center;
            font-size: 0.9rem;
        }

        .language-bar select {
            background: transparent;
            color: white;
            border: 1px solid #666;
            padding: 0.2rem 0.5rem;
            border-radius: 3px;
            margin: 0 0.5rem;
        }

        /* الشريط العلوي */
        header {
            background: linear-gradient(to right, var(--primary), #1a3a7a);
            color: white;
            padding: 0;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1rem 0;
        }

        .logo {
            font-size: 2.2rem;
            font-weight: 800;
            color: white;
            text-decoration: none;
            display: flex;
            align-items: center;
        }
        .logo span { 
            color: var(--secondary);
            margin-right: 0.5rem;
        }
        .logo-icon {
            font-size: 2rem;
            margin-left: 0.8rem;
            color: var(--secondary);
        }

        .nav-links {
            display: flex;
            list-style: none;
        }
        .nav-links li { margin-right: 1.8rem; }
        .nav-links a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
            font-size: 1.05rem;
        }
        .nav-links a:hover { color: var(--secondary); }

        .auth-buttons a {
            margin-right: 0.8rem;
            padding: 0.6rem 1.5rem;
            border-radius: 5px;
            text-decoration: none;
            font-weight: 600;
        }
        .login { color: white; border: 1px solid white; }
        .signup { background: var(--secondary); color: var(--primary); }

        /* قسم البطل */
        .hero {
            background: linear-gradient(rgba(15, 43, 91, 0.85), rgba(15, 43, 91, 0.8)), url('https://images.unsplash.com/photo-1611974789855-9c2a0a7236a3?ixlib=rb-4.0.3&auto=format&fit=crop&w=1350&q=80');
            background-size: cover;
            background-position: center;
            color: white;
            padding: 5rem 0;
            text-align: center;
            position: relative;
            overflow: hidden;
        }
        .hero-content {
            position: relative;
            z-index: 2;
        }
        .hero h1 { 
            font-size: 3.2rem; 
            margin-bottom: 1.5rem;
            text-shadow: 2px 2px 8px rgba(0, 0, 0, 0.3);
        }
        .hero p { 
            font-size: 1.3rem; 
            margin-bottom: 2.5rem; 
            max-width: 800px; 
            margin-left: auto; 
            margin-right: auto;
            line-height: 1.8;
        }
        .cta-button {
            display: inline-block;
            background: var(--secondary);
            color: var(--primary);
            padding: 1.2rem 3rem;
            font-size: 1.2rem;
            font-weight: 700;
            border-radius: 8px;
            text-decoration: none;
            transition: all 0.3s;
            box-shadow: 0 6px 15px rgba(244, 180, 0, 0.3);
        }
        .cta-button:hover { 
            background: #ffcc00; 
            transform: translateY(-5px); 
            box-shadow: 0 12px 25px rgba(0, 0, 0, 0.25); 
        }

        /* صور العوامة */
        .floating-images {
            position: absolute;
            width: 100%;
            height: 100%;
            top: 0;
            left: 0;
            pointer-events: none;
            z-index: 1;
        }
        .floating-img {
            position: absolute;
            border-radius: 10px;
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.3);
            opacity: 0.7;
            transition: opacity 0.5s;
        }
        .floating-img:hover { opacity: 1; }
        .img1 { 
            width: 180px; 
            top: 20%; 
            right: 5%; 
            border: 3px solid var(--secondary);
        }
        .img2 { 
            width: 220px; 
            bottom: 15%; 
            left: 8%; 
            border: 3px solid var(--accent);
        }
        .img3 { 
            width: 160px; 
            top: 40%; 
            left: 15%; 
            border: 3px solid white;
        }

        /* قسم التقييمات */
        .testimonials {
            background: white;
            padding: 5rem 0;
        }
        .testimonials-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }
        .testimonial-card {
            background: var(--light);
            border-radius: 12px;
            padding: 2rem;
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.08);
            border-left: 5px solid var(--secondary);
            transition: transform 0.3s;
        }
        .testimonial-card:hover {
            transform: translateY(-8px);
        }
        .testimonial-header {
            display: flex;
            align-items: center;
            margin-bottom: 1.2rem;
        }
        .testimonial-avatar {
            width: 60px;
            height: 60px;
            border-radius: 50%;
            background: var(--primary);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 1.5rem;
            font-weight: bold;
            margin-left: 1rem;
        }
        .testimonial-name {
            font-weight: 700;
            color: var(--primary);
            font-size: 1.2rem;
        }
        .testimonial-role {
            color: #666;
            font-size: 0.9rem;
        }
        .testimonial-stars {
            color: var(--secondary);
            margin: 0.5rem 0;
        }
        .testimonial-text {
            font-style: italic;
            line-height: 1.7;
            color: #555;
        }

        /* قسم المنتجات */
        .services {
            padding: 5rem 0;
            text-align: center;
            background: linear-gradient(to bottom, #f8f9fa, #e9ecef);
        }
        .section-title {
            font-size: 2.8rem;
            color: var(--primary);
            margin-bottom: 1rem;
            position: relative;
            display: inline-block;
        }
        .section-title:after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 100px;
            height: 4px;
            background: var(--secondary);
            border-radius: 2px;
        }
        .section-subtitle {
            color: #666;
            margin-bottom: 3rem;
            font-size: 1.2rem;
            max-width: 700px;
            margin-left: auto;
            margin-right: auto;
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 2.5rem;
            margin-top: 2rem;
        }
        .service-card {
            background: white;
            border-radius: 12px;
            padding: 2.5rem 2rem;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            transition: all 0.4s;
            border-top: 6px solid var(--primary);
            overflow: hidden;
            position: relative;
        }
        .service-card:before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 5px;
            background: linear-gradient(to right, var(--primary), var(--accent));
        }
        .service-card:hover {
            transform: translateY(-12px);
            box-shadow: 0 18px 40px rgba(0, 0, 0, 0.15);
        }
        .service-icon {
            font-size: 3rem;
            color: var(--primary);
            margin-bottom: 1.5rem;
        }
        .service-card h3 { 
            margin-bottom: 1.2rem; 
            color: var(--primary);
            font-size: 1.6rem;
        }
        .service-image {
            width: 100%;
            height: 180px;
            background-size: cover;
            background-position: center;
            border-radius: 8px;
            margin: 1.5rem 0;
            border: 2px solid #eee;
        }
        .price { 
            color: var(--accent); 
            font-size: 1.8rem; 
            font-weight: 800; 
            margin: 1.2rem 0;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        .price span {
            font-size: 1rem;
            color: #777;
            margin-right: 0.5rem;
        }
        .service-button {
            display: inline-block;
            background: linear-gradient(to right, var(--primary), #1a3a7a);
            color: white;
            padding: 0.9rem 2rem;
            border-radius: 6px;
            text-decoration: none;
            font-weight: 600;
            margin-top: 1rem;
            transition: all 0.3s;
            border: none;
            cursor: pointer;
            width: 100%;
            text-align: center;
        }
        .service-button:hover { 
            background: linear-gradient(to right, #1a3a7a, var(--primary));
            box-shadow: 0 6px 15px rgba(15, 43, 91, 0.3);
        }

        /* قسم الاشتراكات */
        .pricing {
            background: url('https://images.unsplash.com/photo-1613243555978-636c48dc653c?ixlib=rb-4.0.3&auto=format&fit=crop&w=1350&q=80');
            background-size: cover;
            background-attachment: fixed;
            padding: 6rem 0;
            position: relative;
        }
        .pricing:before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(15, 43, 91, 0.88);
        }
        .pricing .container {
            position: relative;
            z-index: 2;
        }
        .pricing .section-title {
            color: white;
        }
        .pricing .section-subtitle {
            color: rgba(255, 255, 255, 0.85);
        }
        .pricing-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2.5rem;
            margin-top: 3rem;
        }
        .pricing-card {
            background: rgba(255, 255, 255, 0.95);
            border-radius: 12px;
            padding: 2.5rem 2rem;
            text-align: center;
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.2);
            position: relative;
            transition: transform 0.4s;
            backdrop-filter: blur(10px);
        }
        .pricing-card:hover {
            transform: translateY(-10px);
        }
        .pricing-card.popular {
            border: 3px solid var(--secondary);
            transform: scale(1.05);
        }
        .pricing-card.popular:hover {
            transform: scale(1.05) translateY(-10px);
        }
        .popular-tag {
            position: absolute;
            top: -15px;
            left: 50%;
            transform: translateX(-50%);
            background: var(--secondary);
            color: var(--primary);
            padding: 0.5rem 2rem;
            border-radius: 25px;
            font-weight: 800;
            font-size: 1rem;
            box-shadow: 0 5px 15px rgba(244, 180, 0, 0.4);
        }
        .pricing-card h3 { 
            color: var(--primary); 
            margin-bottom: 1.5rem;
            font-size: 1.8rem;
        }
        .pricing-card .price { 
            font-size: 3rem; 
            color: var(--dark);
            margin: 1.5rem 0;
        }
        .pricing-card ul {
            list-style: none;
            margin: 2rem 0;
            text-align: right;
        }
        .pricing-card ul li {
            padding: 0.8rem 0;
            border-bottom: 1px solid rgba(0, 0, 0, 0.1);
            display: flex;
            align-items: center;
            justify-content: space-between;
        }
        .pricing-card ul li i.fa-check { 
            color: var(--accent); 
            font-size: 1.2rem;
        }
        .pricing-card ul li i.fa-times { 
            color: #ccc;
            font-size: 1.2rem;
        }

        /* نافذة الدفع */
        .payment-modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.8);
            z-index: 2000;
            align-items: center;
            justify-content: center;
        }

        .payment-modal.active {
            display: flex;
        }

        .payment-content {
            background: white;
            border-radius: 15px;
            width: 90%;
            max-width: 500px;
            padding: 2.5rem;
            position: relative;
            animation: modalSlide 0.3s ease;
        }

        @keyframes modalSlide {
            from { transform: translateY(-50px); opacity: 0; }
            to { transform: translateY(0); opacity: 1; }
        }

        .close-modal {
            position: absolute;
            top: 15px;
            left: 15px;
            background: #ff4757;
            color: white;
            width: 35px;
            height: 35px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            font-size: 1.2rem;
            transition: all 0.3s;
        }

        .close-modal:hover {
            background: #ff3742;
            transform: rotate(90deg);
        }

        .payment-modal h3 {
            color: var(--primary);
            margin-bottom: 1.5rem;
            text-align: center;
            font-size: 1.8rem;
        }

        .payment-modal .product-info {
            background: var(--light);
            padding: 1.2rem;
            border-radius: 8px;
            margin-bottom: 1.5rem;
            border-right: 4px solid var(--accent);
        }

        .payment-modal .product-name {
            font-weight: 700;
            color: var(--primary);
            font-size: 1.3rem;
            margin-bottom: 0.5rem;
        }

        .payment-modal .product-price {
            color: var(--accent);
            font-size: 1.8rem;
            font-weight: 800;
        }

        .payment-options {
            margin-top: 2rem;
        }

        .payment-option {
            background: #f8f9fa;
            border: 2px solid #dee2e6;
            border-radius: 10px;
            padding: 1.2rem;
            margin-bottom: 1rem;
            cursor: pointer;
            transition: all 0.3s;
            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        .payment-option:hover {
            border-color: var(--primary);
            background: #e9ecef;
        }

        .payment-option.selected {
            border-color: var(--secondary);
            background: rgba(244, 180, 0, 0.1);
        }

        .payment-option i {
            font-size: 1.8rem;
            margin-left: 1rem;
        }

        .payment-option.paypal i { color: #003087; }
        .payment-option.bitcoin i { color: #f7931a; }
        .payment-option.usdt i { color: #26a17b; }

        .payment-option span {
            font-weight: 600;
            font-size: 1.1rem;
            color: var(--dark);
        }

        .payment-instructions {
            background: #fff8e1;
            border-radius: 8px;
            padding: 1.2rem;
            margin-top: 1.5rem;
            display: none;
        }

        .payment-instructions.active {
            display: block;
        }

        .crypto-instruction {
            font-size: 0.9rem;
            color: #666;
            margin-bottom: 0.8rem;
            display: flex;
            align-items: center;
        }

        .crypto-instruction i {
            margin-left: 0.5rem;
            color: var(--accent);
        }

        .crypto-address-box {
            background: white;
            border: 1px solid #ddd;
            border-radius: 6px;
            padding: 0.8rem;
            margin: 0.8rem 0;
            font-family: monospace;
            font-size: 0.9rem;
            word-break: break-all;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .copy-btn {
            background: var(--primary);
            color: white;
            border: none;
            padding: 0.4rem 0.8rem;
            border-radius: 4px;
            cursor: pointer;
            font-size: 0.8rem;
            transition: background 0.3s;
        }

        .copy-btn:hover {
            background: #1a3a7a;
        }

        .verify-btn {
            display: inline-block;
            background: var(--accent);
            color: white;
            padding: 0.9rem 2rem;
            border-radius: 6px;
            text-decoration: none;
            font-weight: 600;
            margin-top: 1.5rem;
            width: 100%;
            text-align: center;
            transition: background 0.3s;
        }

        .verify-btn:hover {
            background: #009658;
        }

        /* قسم طرق الدفع في الفوتر */
        .payment-methods {
            background: rgba(255, 255, 255, 0.05);
            padding: 2rem;
            border-radius: 12px;
            margin: 2rem 0;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        .payment-methods h4 {
            color: var(--secondary);
            margin-bottom: 1.5rem;
            font-size: 1.3rem;
            text-align: center;
        }

        .payment-icons {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 1.5rem;
            margin-bottom: 1.5rem;
        }

        .payment-icon {
            background: rgba(255, 255, 255, 0.1);
            border-radius: 10px;
            padding: 1.2rem 1.5rem;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            min-width: 120px;
            transition: all 0.3s;
            cursor: pointer;
            border: 2px solid transparent;
        }

        .payment-icon:hover {
            background: rgba(255, 255, 255, 0.15);
            transform: translateY(-5px);
            border-color: var(--secondary);
        }

        .payment-icon.paypal {
            background: linear-gradient(135deg, rgba(0, 48, 135, 0.2), rgba(0, 156, 222, 0.2));
        }

        .payment-icon.crypto {
            background: linear-gradient(135deg, rgba(247, 147, 26, 0.2), rgba(255, 195, 0, 0.2));
        }

        .payment-icon i {
            font-size: 2.2rem;
            margin-bottom: 0.8rem;
        }

        .payment-icon.paypal i { color: #003087; }
        .payment-icon.crypto i { color: #f7931a; }

        .payment-icon span {
            font-weight: 600;
            font-size: 1rem;
            color: white;
        }

        .crypto-address {
            font-size: 0.7rem;
            color: #aaa;
            word-break: break-all;
            margin-top: 0.5rem;
            text-align: center;
            display: none;
        }

        .payment-icon:hover .crypto-address {
            display: block;
        }

        .payment-note {
            text-align: center;
            color: #ccc;
            margin-top: 1.5rem;
            padding-top: 1rem;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }

        .payment-note a {
            color: var(--secondary);
            text-decoration: none;
            margin: 0 0.5rem;
            font-weight: 600;
        }

        .payment-note a:hover {
            text-decoration: underline;
        }

        /* التذييل */
        footer {
            background: linear-gradient(to right, #1a1a2e, var(--dark));
            color: white;
            padding: 4rem 0 2rem;
        }
        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 3rem;
            margin-bottom: 3rem;
        }
        .footer-logo {
            font-size: 2.2rem;
            font-weight: 800;
            margin-bottom: 1rem;
            display: flex;
            align-items: center;
        }
        .footer-logo span {
            color: var(--secondary);
            margin-right: 0.5rem;
        }
        .footer-links h4 {
            color: var(--secondary);
            margin-bottom: 1.5rem;
            font-size: 1.3rem;
            border-bottom: 2px solid rgba(255, 255, 255, 0.1);
            padding-bottom: 0.7rem;
            display: inline-block;
        }
        .footer-links a {
            color: #ccc;
            text-decoration: none;
            display: block;
            margin-bottom: 0.8rem;
            transition: all 0.3s;
            padding: 0.3rem 0;
        }
        .footer-links a:hover { 
            color: var(--secondary); 
            transform: translateX(-5px);
        }
        .footer-links a i {
            margin-left: 0.8rem;
            width: 20px;
        }
        .copyright {
            text-align: center;
            padding-top: 2rem;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: #aaa;
            font-size: 0.95rem;
            line-height: 1.8;
        }

        /* التجاوب مع الأجهزة المحمولة */
        @media (max-width: 992px) {
            .navbar { flex-direction: column; padding: 1.5rem 0; }
            .nav-links { margin: 1.5rem 0; flex-wrap: wrap; justify-content: center; }
            .nav-links li { margin: 0.5rem 1rem; }
            .auth-buttons { margin-top: 1rem; }
            .hero h1 { font-size: 2.5rem; }
            .hero p { font-size: 1.1rem; }
            .floating-images { display: none; }
            .pricing-card.popular { transform: none; }
            .pricing-card.popular:hover { transform: translateY(-10px); }
        }

        @media (max-width: 768px) {
            .hero h1 { font-size: 2rem; }
            .section-title { font-size: 2.2rem; }
            .services-grid, .pricing-grid, .testimonials-grid { 
                grid-template-columns: 1fr;
                gap: 2rem;
            }
            .logo { font-size: 1.8rem; }
            .payment-icons {
                flex-direction: column;
                align-items: center;
            }
            
            .payment-icon {
                width: 100%;
                max-width: 250px;
            }
            .payment-content {
                padding: 1.5rem;
                width: 95%;
            }
        }
    </style>
</head>
<body>
    <!-- شريط اللغات -->
    <div class="language-bar">
        <div class="container">
            <span>اللغة / Language / Langue:</span>
            <select id="languageSelect">
                <option value="ar">العربية</option>
                <option value="en">English</option>
                <option value="fr">Français</option>
            </select>
            <span id="current-language">العربية</span>
        </div>
    </div>

    <!-- شريط التنقل العلوي -->
    <header>
        <div class="container">
            <nav class="navbar">
                <a href="#" class="logo">
                    <i class="fas fa-globe-americas logo-icon"></i>
                    <span>Atlas</span>Trade
                </a>
                <ul class="nav-links">
                    <li><a href="#"><i class="fas fa-home"></i> الرئيسية</a></li>
                    <li><a href="#courses"><i class="fas fa-graduation-cap"></i> الكورسات</a></li>
                    <li><a href="#indicators"><i class="fas fa-chart-line"></i> المؤشرات</a></li>
                    <li><a href="#pricing"><i class="fas fa-crown"></i> الاشتراكات</a></li>
                    <li><a href="#testimonials"><i class="fas fa-star"></i> التقييمات</a></li>
                    <li><a href="#"><i class="fas fa-robot"></i> الروبوتات</a></li>
                </ul>
                <div class="auth-buttons">
                    <a href="#" class="login">تسجيل الدخول</a>
                    <a href="#" class="signup">حساب جديد</a>
                </div>
            </nav>
        </div>
    </header>

    <!-- القسم الرئيسي -->
    <section class="hero">
        <div class="floating-images">
            <img src="https://images.unsplash.com/photo-1642790553124-4c56d74c5a65?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80" alt="تداول آلي" class="floating-img img1">
            <img src="https://images.unsplash.com/photo-1611974789855-9c2a0a7236a3?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80" alt="تحليل الأسواق" class="floating-img img2">
            <img src="https://images.unsplash.com/photo-1613243555978-636c48dc653c?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=60" alt="بورصة عالمية" class="floating-img img3">
        </div>
        <div class="container hero-content">
            <h1>الذكاء الاصطناعي يلتقي بالتحليل المالي</h1>
            <p>Atlas Trade يوفر لك منصة متكاملة تجمع بين أحدث تقنيات الروبوتات التداولية، المؤشرات الذكية، والتعليم الاحترافي. انضم إلى آلاف المتداولين الذين حوّلوا استراتيجياتهم معنا.</p>
            <a href="#pricing" class="cta-button">ابدأ رحلتك الآن <i class="fas fa-arrow-left"></i></a>
        </div>
    </section>

    <!-- قسم التقييمات -->
    <section class="testimonials" id="testimonials">
        <div class="container">
            <h2 class="section-title">آراء عملائنا</h2>
            <p class="section-subtitle">إنضم أكثر من 5,000 متداول إلى مجتمع Atlas Trade وأثنوا على خدماتنا</p>

            <div class="testimonials-grid">
                <!-- تقييم 1 -->
                <div class="testimonial-card">
                    <div class="testimonial-header">
                        <div class="testimonial-avatar">م.ع</div>
                        <div>
                            <div class="testimonial-name">محمد العلي</div>
                            <div class="testimonial-role">مستثمر محترف - 4 سنوات</div>
                        </div>
                    </div>
                    <div class="testimonial-stars">
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                    </div>
                    <p class="testimonial-text">"روبوت التداول الذي حصلت عليه من Atlas Trade غيّر أسلوبي تماماً. الدقة في الإشارات تتجاوز 85% وقد رفعت أرباحي بنسبة 40% في أول شهرين."</p>
                </div>

                <!-- تقييم 2 -->
                <div class="testimonial-card">
                    <div class="testimonial-header">
                        <div class="testimonial-avatar">س.ف</div>
                        <div>
                            <div class="testimonial-name">سارة فتحي</div>
                            <div class="testimonial-role">مبتدئة تحولت إلى محترفة - 8 شهور</div>
                        </div>
                    </div>
                    <div class="testimonial-stars">
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star-half-alt"></i>
                    </div>
                    <p class="testimonial-text">"الدورة الشاملة كانت نقطة تحولي. من لا أعرف شيء عن الأسواق إلى تحقيق أرباح ثابتة. الدعم الفني كان ممتازاً ويجاوبون على جميع استفساراتك."</p>
                </div>

                <!-- تقييم 3 -->
                <div class="testimonial-card">
                    <div class="testimonial-header">
                        <div class="testimonial-avatar">خ.ب</div>
                        <div>
                            <div class="testimonial-name">خالد بدر</div>
                            <div class="testimonial-role">مدير محفظة استثمارية - 6 سنوات</div>
                        </div>
                    </div>
                    <div class="testimonial-stars">
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                    </div>
                    <p class="testimonial-text">"مؤشرات التحليل المتقدمة التي يقدمونها توفر لي ساعات من العمل يومياً. الدقة عالية والواجهة سهلة الاستخدام. أنصح أي متداول جاد بالاشتراك معهم."</p>
                </div>
            </div>
        </div>
    </section>

    <!-- قسم المنتجات والخدمات -->
    <section class="services" id="courses">
        <div class="container">
            <h2 class="section-title">منتجاتنا المتطورة</h2>
            <p class="section-subtitle">مجموعة متكاملة من الأدوات التعليمية والتقنية المدعومة بالذكاء الاصطناعي</p>

            <div class="services-grid">
                <!-- كورس 1 -->
                <div class="service-card" data-product="روبوت التداول الذكي AI-Trader" data-price="499">
                    <div class="service-icon"><i class="fas fa-robot"></i></div>
                    <h3>روبوت التداول الذكي AI-Trader</h3>
                    <p>روبوت تداول آلي يستخدم خوارزميات الذكاء الاصطناعي للتعلم من تحركات السوق وتنفيذ الصفقات تلقائياً بنسبة دقة عالية.</p>
                    <div class="service-image" style="background-image: url('https://images.unsplash.com/photo-1642790553124-4c56d74c5a65?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80');"></div>
                    <div class="price">$499 <span>(رخصة سنوية)</span></div>
                    <a href="#" class="service-button buy-btn">شراء الروبوت</a>
                </div>

                <!-- كورس 2 -->
                <div class="service-card" data-product="حزمة المؤشرات المتقدمة" data-price="299">
                    <div class="service-icon"><i class="fas fa-chart-bar"></i></div>
                    <h3>حزمة المؤشرات المتقدمة</h3>
                    <p>15 مؤشر فني ذكي مع إمكانية التنبؤ بحركة السعر، اكتشاف الفرص، وتحليل الاتجاهات بدقة غير مسبوقة.</p>
                    <div class="service-image" style="background-image: url('https://images.unsplash.com/photo-1611974789855-9c2a0a7236a3?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80');"></div>
                    <div class="price">$299 <span>(تحديثات مجانية لمدة عام)</span></div>
                    <a href="#" class="service-button buy-btn">شراء المؤشرات</a>
                </div>

                <!-- كورس 3 -->
                <div class="service-card" data-product="أكاديمية التداول الاحترافي" data-price="349">
                    <div class="service-icon"><i class="fas fa-graduation-cap"></i></div>
                    <h3>أكاديمية التداول الاحترافي</h3>
                    <p>دورة متكاملة من البداية إلى الاحتراف: 45 ساعة فيديو، تدريبات عملية، ومتابعة شخصية مع مدربين محترفين.</p>
                    <div class="service-image" style="background-image: url('https://images.unsplash.com/photo-1553877522-43269d4ea984?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80');"></div>
                    <div class="price">$349 <span>(وصول دائم + تحديثات)</span></div>
                    <a href="#" class="service-button buy-btn">الاشتراك في الدورة</a>
                </div>
            </div>
        </div>
    </section>

    <!-- قسم باقات الاشتراك -->
    <section class="pricing" id="pricing">
        <div class="container">
            <h2 class="section-title">باقات العضوية الشهرية</h2>
            <p class="section-subtitle">اختر الباقة التي تناسب أهدافك التداولية واحصل على دعم فني متكامل</p>

            <div class="pricing-grid">
                <!-- الباقة الأساسية -->
                <div class="pricing-card" data-product="الباقة الأساسية" data-price="79" data-type="شهري">
                    <h3>الباقة الأساسية</h3>
                    <div class="price">$79<span>/شهر</span></div>
                    <ul>
                        <li><i class="fas fa-check"></i> <span>روبوت تداول أساسي</span></li>
                        <li><i class="fas fa-check"></i> <span>5 مؤشرات فنية</span></li>
                        <li><i class="fas fa-check"></i> <span>3 إشارات تداول أسبوعية</span></li>
                        <li><i class="fas fa-times"></i> <span>لا يشمل دعم فني مخصص</span></li>
                        <li><i class="fas fa-times"></i> <span>لا يشمل جلسات تدريبية</span></li>
                    </ul>
                    <a href="#" class="service-button buy-btn">اشترك الآن</a>
                </div>

                <!-- الباقة المميزة (موصى بها) -->
                <div class="pricing-card popular" data-product="الباقة الاحترافية" data-price="149" data-type="شهري">
                    <div class="popular-tag">الأكثر طلباً</div>
                    <h3>الباقة الاحترافية</h3>
                    <div class="price">$149<span>/شهر</span></div>
                    <ul>
                        <li><i class="fas fa-check"></i> <span>روبوت تداول متقدم بالذكاء الاصطناعي</span></li>
                        <li><i class="fas fa-check"></i> <span>جميع المؤشرات المتقدمة (15 مؤشر)</span></li>
                        <li><i class="fas fa-check"></i> <span>إشارات تداول يومية (5-7 إشارات)</span></li>
                        <li><i class="fas fa-check"></i> <span>دعم فني مخصص عبر الهاتف والبريد</span></li>
                        <li><i class="fas fa-check"></i> <span>جلسة تدريبية شهرية</span></li>
                    </ul>
                    <a href="#" class="service-button buy-btn" style="background: linear-gradient(to right, var(--secondary), #ffcc00); color: var(--primary);">اشترك الآن</a>
                </div>

                <!-- الباقة الاحترافية -->
                <div class="pricing-card" data-product="الباقة المؤسسية" data-price="299" data-type="شهري">
                    <h3>الباقة المؤسسية</h3>
                    <div class="price">$299<span>/شهر</span></div>
                    <ul>
                        <li><i class="fas fa-check"></i> <span>روبوت تداول مؤسسي متعدد الاستراتيجيات</span></li>
                        <li><i class="fas fa-check"></i> <span>جميع المؤشرات + أدوات تحليل حصرية</span></li>
                        <li><i class="fas fa-check"></i> <span>إشارات تداول فورية (Real-Time)</span></li>
                        <li><i class="fas fa-check"></i> <span>دعم فني على مدار الساعة</span></li>
                        <li><i class="fas fa-check"></i> <span>تدريب أسبوعي + تحليل محفظة شخصي</span></li>
                    </ul>
                    <a href="#" class="service-button buy-btn">اشترك الآن</a>
                </div>
            </div>
        </div>
    </section>

    <!-- نافذة الدفع -->
    <div class="payment-modal" id="paymentModal">
        <div class="payment-content">
            <div class="close-modal" onclick="closePaymentModal()">×</div>
            <h3>إتمام عملية الشراء</h3>
            
            <div class="product-info">
                <div class="product-name" id="modalProductName">روبوت التداول الذكي AI-Trader</div>
                <div class="product-price" id="modalProductPrice">$499</div>
                <div id="modalProductType"></div>
            </div>

            <div class="payment-options">
                <div class="payment-option paypal" onclick="selectPayment('paypal')">
                    <div>
                        <i class="fab fa-paypal"></i>
                        <span>الدفع عبر PayPal</span>
                    </div>
                    <i class="fas fa-chevron-left"></i>
                </div>
                
                <div class="payment-option bitcoin" onclick="selectPayment('bitcoin')">
                    <div>
                        <i class="fab fa-bitcoin"></i>
                        <span>الدفع بـ Bitcoin</span>
                    </div>
                    <i class="fas fa-chevron-left"></i>
                </div>
                
                <div class="payment-option usdt" onclick="selectPayment('usdt')">
                    <div>
                        <i class="fas fa-coins"></i>
                        <span>الدفع بـ USDT (TRC20)</span>
                    </div>
                    <i class="fas fa-chevron-left"></i>
                </div>
            </div>

            <!-- تعليمات البيتكوين -->
            <div class="payment-instructions" id="bitcoinInstructions">
                <h4>تعليمات الدفع بـ Bitcoin:</h4>
                <div class="crypto-instruction"><i class="fas fa-check-circle"></i> قم بإرسال المبلغ بالضبط إلى العنوان التالي:</div>
                <div class="crypto-address-box">
                    <span id="btcAddressModal">1PxVQwUutmSpf6yficDeYM1RCyeCW3tVPC</span>
                    <button class="copy-btn" onclick="copyAddress('btcAddressModal')">نسخ</button>
                </div>
                <div class="crypto-instruction"><i class="fas fa-check-circle"></i> تأكد من دقة العنوان قبل الإرسال</div>
                <div class="crypto-instruction"><i class="fas fa-check-circle"></i> بعد الإرسال، أرسل إشعار الدفع عبر WhatsApp أو Telegram</div>
                
                <a href="https://wa.me/212626995045?text=لقد%20قمت%20بإرسال%20الدفع%20عبر%20Bitcoin%20للمنتج:%20" target="_blank" class="verify-btn" id="whatsappVerifyBTC">
                    <i class="fab fa-whatsapp"></i> تأكيد الدفع عبر واتساب
                </a>
            </div>

            <!-- تعليمات USDT -->
            <div class="payment-instructions" id="usdtInstructions">
                <h4>تعليمات الدفع بـ USDT:</h4>
                <div class="crypto-instruction"><i class="fas fa-check-circle"></i> قم بإرسال المبلغ بالضبط إلى العنوان التالي (شبكة TRC20):</div>
                <div class="crypto-address-box">
                    <span id="usdtAddressModal">TAThDq59eRyoZL544CEGo6c7yf9JKSoDkM</span>
                    <button class="copy-btn" onclick="copyAddress('usdtAddressModal')">نسخ</button>
                </div>
                <div class="crypto-instruction"><i class="fas fa-check-circle"></i> تأكد من استخدام شبكة TRC20 فقط</div>
                <div class="crypto-instruction"><i class="fas fa-check-circle"></i> بعد الإرسال، أرسل إشعار الدفع عبر WhatsApp أو Telegram</div>
                
                <a href="https://wa.me/212626995045?text=لقد%20قمت%20بإرسال%20الدفع%20عبر%20USDT%20للمنتج:%20" target="_blank" class="verify-btn" id="whatsappVerifyUSDT">
                    <i class="fab fa-whatsapp"></i> تأكيد الدفع عبر واتساب
                </a>
            </div>

            <!-- تعليمات PayPal -->
            <div class="payment-instructions" id="paypalInstructions">
                <h4>تعليمات الدفع عبر PayPal:</h4>
                <div class="crypto-instruction"><i class="fas fa-check-circle"></i> سيتم تحويلك إلى صفحة PayPal الآمنة</div>
                <div class="crypto-instruction"><i class="fas fa-check-circle"></i> أكمل عملية الدفع باستخدام حساب PayPal الخاص بك</div>
                <div class="crypto-instruction"><i class="fas fa-check-circle"></i> سيتم تفعيل المنتج تلقائياً بعد تأكيد الدفع</div>
                
                <a href="https://www.paypal.com/paypalme/atlastrade" target="_blank" class="verify-btn">
                    <i class="fab fa-paypal"></i> الانتقال إلى PayPal
                </a>
            </div>
        </div>
    </div>

    <!-- التذييل -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div>
                    <div class="footer-logo">
                        <span>Atlas</span>Trade
                    </div>
                    <p>منصة عالمية تجمع بين أحدث تقنيات الذكاء الاصطناعي والخبرة المالية لتوفير أدوات تداول متطورة وموارد تعليمية احترافية.</p>
                    <div style="margin-top: 1.5rem;">
                        <img src="https://images.unsplash.com/photo-1613243555978-636c48dc653c?ixlib=rb-4.0.3&auto=format&fit=crop&w=200&q=80" alt="البورصة العالمية" style="width: 100%; border-radius: 8px; margin-top: 1rem;">
                    </div>
                </div>
                <div class="footer-links">
                    <h4>روابط سريعة</h4>
                    <a href="#"><i class="fas fa-chevron-left"></i> من نحن</a>
                    <a href="#"><i class="fas fa-chevron-left"></i> المدونة والأخبار</a>
                    <a href="#"><i class="fas fa-chevron-left"></i> الشروط والأحكام</a>
                    <a href="#"><i class="fas fa-chevron-left"></i> سياسة الخصوصية</a>
                    <a href="#"><i class="fas fa-chevron-left"></i> إخلاء المسؤولية</a>
                    <a href="#"><i class="fas fa-chevron-left"></i> اتصل بنا</a>
                </div>
                <div class="footer-links">
                    <h4>وسائل التواصل</h4>
                    <a href="#"><i class="fab fa-whatsapp"></i> واتساب</a>
                    <a href="#"><i class="fab fa-telegram"></i> تيليجرام</a>
                    <a href="#"><i class="fab fa-twitter"></i> تويتر</a>
                    <a href="#"><i class="fab fa-youtube"></i> يوتيوب</a>
                    <a href="#"><i class="fas fa-envelope"></i> البريد الإلكتروني</a>
                    <a href="#"><i class="fas fa-phone"></i> الدعم الهاتفي</a>
                </div>
            </div>
            
            <!-- قسم طرق الدفع الجديد -->
            <div class="payment-methods">
                <h4>طرق الدفع المتاحة</h4>
                <div class="payment-icons">
                    <!-- PayPal -->
                    <a href="https://paypal.com" target="_blank" class="payment-icon paypal" title="PayPal">
                        <i class="fab fa-paypal"></i>
                        <span>PayPal</span>
                    </a>
                    <!-- Bitcoin -->
                    <div class="payment-icon crypto" title="Bitcoin" onclick="copyCrypto('btc')">
                        <i class="fab fa-bitcoin"></i>
                        <span>Bitcoin</span>
                        <div class="crypto-address" id="btc-address">1PxVQwUutmSpf6yficDeYM1RCyeCW3tVPC</div>
                    </div>
                    <!-- USDT -->
                    <div class="payment-icon crypto" title="USDT (TRC20)" onclick="copyCrypto('usdt')">
                        <i class="fas fa-coins"></i>
                        <span>USDT</span>
                        <div class="crypto-address" id="usdt-address">TAThDq59eRyoZL544CEGo6c7yf9JKSoDkM</div>
                    </div>
                </div>
                <p class="payment-note">للاستفسارات حول الدفع: <a href="https://wa.me/212626995045" target="_blank"><i class="fab fa-whatsapp"></i> 0626995045</a> | <a href="https://t.me/atlasea" target="_blank"><i class="fab fa-telegram"></i> @atlasea</a></p>
            </div>
            
            <div class="copyright">
                <p>© 2023 Atlas Trade. جميع الحقوق محفوظة. التداول في الأسواق المالية ينطوي على مخاطر قد تؤدي إلى خسارة رأس المال.</p>
                <p><strong>إخلاء المسؤولية:</strong> منتجاتنا وخدماتنا لأغراض تعليمية وإعلامية فقط. الأداء السابق لا يضمن النتائج المستقبلية. يجب أن تستند قرارات التداول إلى بحثك الشخصي.</p>
            </div>
        </div>
    </footer>

    <script>
        // تبديل اللغات
        document.getElementById('languageSelect').addEventListener('change', function() {
            const languages = {
                'ar': 'العربية',
                'en': 'English',
                'fr': 'Français'
            };
            document.getElementById('current-language').textContent = languages[this.value];
            
            // هنا يمكنك إضافة كود لتحميل المحتوى بلغة مختلفة
            alert('سيتم تحويل الموقع إلى ' + languages[this.value] + '. في التطبيق الحقيقي، سيتم تحميل المحتوى بلغة مختلفة.');
        });

        // التنقل السلس
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                const targetId = this.getAttribute('href');
                if(targetId === '#') return;
                const targetElement = document.querySelector(targetId);
                if(targetElement) {
                    window.scrollTo({
                        top: targetElement.offsetTop - 100,
                        behavior: 'smooth'
                    });
                }
            });
        });

        // تحريك الصور العائمة
        document.addEventListener('mousemove', function(e) {
            const floatingImages = document.querySelectorAll('.floating-img');
            const mouseX = e.clientX / window.innerWidth;
            const mouseY = e.clientY / window.innerHeight;
            
            floatingImages.forEach((img, index) => {
                const speed = 0.02 + (index * 0.01);
                const x = (mouseX * 30 - 15) * speed;
                const y = (mouseY * 30 - 15) * speed;
                
                img.style.transform = `translate(${x}px, ${y}px)`;
            });
        });

        // نسخ عناوين العملات المشفرة
        function copyCrypto(type) {
            let address = '';
            let currency = '';
            
            if (type === 'btc') {
                address = '1PxVQwUutmSpf6yficDeYM1RCyeCW3tVPC';
                currency = 'Bitcoin';
            } else if (type === 'usdt') {
                address = 'TAThDq59eRyoZL544CEGo6c7yf9JKSoDkM';
                currency = 'USDT (TRC20)';
            }
            
            navigator.clipboard.writeText(address).then(() => {
                alert(`✓ تم نسخ عنوان ${currency}: ${address}`);
            }).catch(err => {
                prompt(`انسخ عنوان ${currency} يدوياً:`, address);
            });
        }

        // متغيرات الدفع
        let currentProduct = '';
        let currentPrice = '';
        let currentProductType = '';
        let selectedPaymentMethod = '';

        // فتح نافذة الدفع
        document.querySelectorAll('.buy-btn').forEach(button => {
            button.addEventListener('click', function(e) {
                e.preventDefault();
                e.stopPropagation();
                
                // الحصول على بيانات المنتج
                const card = this.closest('.service-card, .pricing-card');
                currentProduct = card.getAttribute('data-product');
                currentPrice = card.getAttribute('data-price');
                currentProductType = card.getAttribute('data-type') || 'للمرة الواحدة';
                
                // تحديث محتوى النافذة
                document.getElementById('modalProductName').textContent = currentProduct;
                document.getElementById('modalProductPrice').textContent = '$' + currentPrice;
                document.getElementById('modalProductType').textContent = currentProductType;
                
                // تحديث روابط واتساب
                const whatsappMessage = encodeURIComponent(`لقد قمت بطلب المنتج: ${currentProduct} - السعر: $${currentPrice} - ${currentProductType}`);
                document.getElementById('whatsappVerifyBTC').href = `https://wa.me/212626995045?text=${whatsappMessage}%20(دفع%20Bitcoin)`;
                document.getElementById('whatsappVerifyUSDT').href = `https://wa.me/212626995045?text=${whatsappMessage}%20(دفع%20USDT)`;
                
                // إظهار نافذة الدفع
                document.getElementById('paymentModal').classList.add('active');
                document.body.style.overflow = 'hidden';
                
                // إخفاء جميع التعليمات
                document.querySelectorAll('.payment-instructions').forEach(el => {
                    el.classList.remove('active');
                });
                
                // إزالة التحديد من جميع خيارات الدفع
                document.querySelectorAll('.payment-option').forEach(el => {
                    el.classList.remove('selected');
                });
                
                selectedPaymentMethod = '';
            });
        });

        // إغلاق نافذة الدفع
        function closePaymentModal() {
            document.getElementById('paymentModal').classList.remove('active');
            document.body.style.overflow = 'auto';
            selectedPaymentMethod = '';
        }

        // اختيار طريقة الدفع
        function selectPayment(method) {
            // إزالة التحديد من جميع الخيارات
            document.querySelectorAll('.payment-option').forEach(el => {
                el.classList.remove('selected');
            });
            
            // إضافة التحديد للخيار المختار
            event.currentTarget.classList.add('selected');
            selectedPaymentMethod = method;
            
            // إخفاء جميع التعليمات
            document.querySelectorAll('.payment-instructions').forEach(el => {
                el.classList.remove('active');
            });
            
            // إظهار التعليمات المناسبة
            if (method === 'bitcoin') {
                document.getElementById('bitcoinInstructions').classList.add('active');
            } else if (method === 'usdt') {
                document.getElementById('usdtInstructions').classList.add('active');
            } else if (method === 'paypal') {
                document.getElementById('paypalInstructions').classList.add('active');
            }
        }

        // نسخ العنوان في النافذة
        function copyAddress(elementId) {
            const address = document.getElementById(elementId).textContent;
            navigator.clipboard.writeText(address).then(() => {
                alert('✓ تم نسخ العنوان: ' + address);
            }).catch(err => {
                prompt('انسخ العنوان يدوياً:', address);
            });
        }

        // إغلاق النافذة عند النقر خارجها
        document.getElementById('paymentModal').addEventListener('click', function(e) {
            if (e.target === this) {
                closePaymentModal();
            }
        });

        // إغلاق النافذة بالزر Escape
        document.addEventListener('keydown', function(e) {
            if (e.key === 'Escape' && document.getElementById('paymentModal').classList.contains('active')) {
                closePaymentModal();
            }
        });
    </script>
</body>
</html>
