<DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">
    <title>AMani Exports | Экспорт фруктов и овощей из Индии</title>
    <meta name="description" content="AMani Exports - экспорт свежих фруктов и овощей премиум-класса из Индии в Россию, Европу, страны Персидского залива (Катар, Бахрейн, Кувейт, Саудовская Аравия) и по всему миру.">
    <meta name="keywords" content="экспорт фруктов Индия, экспорт овощей, Россия, страны Персидского залива, Катар, Бахрейн, Кувейт, Саудовская Аравия">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --primary: #2e7d32;
            --primary-dark: #1b5e20;
            --secondary: #ff8c42;
            --bg: #ffffff;
            --text: #1f2937;
            --text-light: #6b7280;
            --card-bg: #ffffff;
            --border: #e5e7eb;
            --shadow: 0 10px 25px -5px rgba(0,0,0,0.05), 0 8px 10px -6px rgba(0,0,0,0.02);
            --navbar-bg: rgba(255,255,255,0.95);
            --transition: all 0.3s ease;
        }

        [data-theme="dark"] {
            --primary: #4caf50;
            --primary-dark: #388e3c;
            --bg: #0f172a;
            --text: #f1f5f9;
            --text-light: #94a3b8;
            --card-bg: #1e293b;
            --border: #334155;
            --shadow: 0 10px 25px -5px rgba(0,0,0,0.3);
            --navbar-bg: rgba(15,23,42,0.95);
        }

        body {
            font-family: 'Poppins', 'Inter', sans-serif;
            background: var(--bg);
            color: var(--text);
            transition: background 0.3s, color 0.2s;
            line-height: 1.6;
            overflow-x: hidden;
        }

        /* Language Switcher */
        .language-switcher {
            position: fixed;
            top: 20px;
            left: 20px;
            z-index: 1000;
            display: flex;
            gap: 8px;
            background: var(--card-bg);
            padding: 8px 12px;
            border-radius: 50px;
            border: 1px solid var(--border);
            box-shadow: var(--shadow);
        }

        .lang-btn {
            background: transparent;
            border: none;
            cursor: pointer;
            padding: 6px 12px;
            border-radius: 30px;
            font-weight: 500;
            transition: var(--transition);
            color: var(--text);
            font-size: 0.85rem;
        }

        .lang-btn.active {
            background: var(--primary);
            color: white;
        }

        .lang-btn:hover:not(.active) {
            background: var(--border);
        }

        /* Theme Toggle */
        .theme-toggle-wrapper {
            position: fixed;
            top: 20px;
            right: 20px;
            z-index: 1000;
        }

        .theme-toggle {
            background: var(--card-bg);
            border: 1px solid var(--border);
            border-radius: 50px;
            padding: 10px 14px;
            cursor: pointer;
            font-size: 1.2rem;
            box-shadow: var(--shadow);
            transition: var(--transition);
        }

        .theme-toggle i:first-child { display: inline; }
        .theme-toggle i:last-child { display: none; }

        [data-theme="dark"] .theme-toggle i:first-child { display: none; }
        [data-theme="dark"] .theme-toggle i:last-child { display: inline; }

        /* Navbar */
        .navbar {
            background: var(--navbar-bg);
            backdrop-filter: blur(10px);
            position: sticky;
            top: 0;
            z-index: 999;
            border-bottom: 1px solid var(--border);
            padding: 1rem 0;
        }

        .nav-container {
            max-width: 1280px;
            margin: 0 auto;
            padding: 0 2rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: 700;
            color: var(--primary);
        }

        .logo i { margin-right: 8px; }

        .nav-links {
            display: flex;
            gap: 2rem;
            list-style: none;
        }

        .nav-links a {
            text-decoration: none;
            color: var(--text);
            font-weight: 500;
            transition: color 0.3s;
            position: relative;
        }

        .nav-links a:hover, .nav-links a.active {
            color: var(--primary);
        }

        .nav-links a.active::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 100%;
            height: 2px;
            background: var(--primary);
        }

        .hamburger {
            display: none;
            font-size: 1.5rem;
            cursor: pointer;
        }

        /* Pages */
        .page {
            display: none;
            padding: 3rem 1rem;
            animation: fade 0.4s ease;
        }

        .active-page {
            display: block;
        }

        @keyframes fade {
            from { opacity: 0; transform: translateY(10px);}
            to { opacity: 1; transform: translateY(0);}
        }

        .container {
            max-width: 1280px;
            margin: 0 auto;
            padding: 0 1rem;
        }

        .section-title {
            font-size: 2rem;
            margin-bottom: 2rem;
            text-align: center;
            position: relative;
        }

        .section-title::after {
            content: '';
            display: block;
            width: 60px;
            height: 3px;
            background: var(--primary);
            margin: 0.5rem auto 0;
        }

        .highlight {
            color: var(--secondary);
        }

        /* Hero Section */
        .hero {
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            justify-content: space-between;
            gap: 2rem;
            max-width: 1280px;
            margin: 0 auto;
        }

        .hero-content {
            flex: 1;
        }

        .badge {
            background: var(--primary);
            color: white;
            padding: 0.3rem 1rem;
            border-radius: 50px;
            display: inline-block;
            margin-bottom: 1rem;
            font-size: 0.9rem;
        }

        .hero h1 {
            font-size: 3rem;
            margin-bottom: 0.5rem;
            line-height: 1.2;
        }

        .hero p {
            color: var(--text-light);
            margin: 1rem 0;
        }

        .stats {
            display: flex;
            gap: 2rem;
            margin: 1.5rem 0;
        }

        .stat span {
            font-size: 1.8rem;
            font-weight: bold;
            color: var(--primary);
            display: block;
        }

        .hero-image i {
            font-size: 6rem;
            color: var(--primary);
            margin: 0 0.5rem;
            animation: float 3s ease-in-out infinite;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-10px); }
        }

        /* Buttons */
        .btn-primary, .btn-secondary {
            padding: 12px 28px;
            border-radius: 40px;
            border: none;
            font-weight: 600;
            cursor: pointer;
            transition: var(--transition);
            font-size: 1rem;
        }

        .btn-primary {
            background: var(--primary);
            color: white;
        }

        .btn-primary:hover {
            background: var(--primary-dark);
            transform: scale(1.02);
        }

        .btn-secondary {
            background: transparent;
            border: 2px solid var(--primary);
            color: var(--primary);
        }

        .btn-secondary:hover {
            background: var(--primary);
            color: white;
        }

        /* Features */
        .features {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 2rem;
            margin-top: 4rem;
        }

        .feature-card {
            background: var(--card-bg);
            padding: 1.8rem;
            border-radius: 20px;
            text-align: center;
            width: 260px;
            box-shadow: var(--shadow);
            transition: var(--transition);
            border: 1px solid var(--border);
        }

        .feature-card:hover {
            transform: translateY(-8px);
        }

        .feature-card i {
            font-size: 2.5rem;
            color: var(--primary);
            margin-bottom: 1rem;
        }

        /* Filter Bar */
        .filter-bar {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            margin-bottom: 2rem;
            gap: 1rem;
        }

        .search-input {
            padding: 12px 20px;
            border-radius: 40px;
            border: 1px solid var(--border);
            background: var(--card-bg);
            color: var(--text);
            width: 300px;
            transition: var(--transition);
        }

        .search-input:focus {
            outline: none;
            border-color: var(--primary);
        }

        .filter-buttons {
            display: flex;
            gap: 0.8rem;
            flex-wrap: wrap;
        }

        .filter-chip {
            padding: 8px 20px;
            border-radius: 40px;
            background: var(--card-bg);
            border: 1px solid var(--border);
            cursor: pointer;
            transition: var(--transition);
            font-weight: 500;
        }

        .filter-chip.active, .filter-chip:hover {
            background: var(--primary);
            color: white;
        }

        /* Products Grid */
        .products-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 1.8rem;
        }

        .product-card {
            background: var(--card-bg);
            border-radius: 20px;
            padding: 1.5rem;
            box-shadow: var(--shadow);
            transition: var(--transition);
            border: 1px solid var(--border);
        }

        .product-card:hover {
            transform: translateY(-6px);
        }

        .product-card i {
            font-size: 2.5rem;
            color: var(--primary);
            margin-bottom: 1rem;
        }

        .product-card h3 {
            margin-bottom: 0.5rem;
        }

        /* Countries Section */
        .countries-showcase {
            display: flex;
            flex-wrap: wrap;
            gap: 2rem;
            justify-content: center;
            margin-bottom: 2rem;
        }

        .region {
            background: var(--card-bg);
            padding: 1.8rem;
            border-radius: 20px;
            flex: 1;
            min-width: 260px;
            box-shadow: var(--shadow);
            border: 1px solid var(--border);
        }

        .region h3 {
            margin-bottom: 1rem;
            color: var(--primary);
        }

        .country-list {
            line-height: 1.8;
            color: var(--text-light);
        }

        .export-map {
            text-align: center;
            padding: 2rem;
            background: var(--card-bg);
            border-radius: 20px;
            margin-top: 2rem;
        }

        .export-map i {
            font-size: 2rem;
            color: var(--primary);
            margin-bottom: 1rem;
        }

        /* About Section */
        .about-container {
            max-width: 900px;
            margin: 0 auto;
        }

        .milestones {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 1.5rem;
            margin-top: 2rem;
        }

        .milestones div {
            background: var(--card-bg);
            padding: 1.2rem;
            border-radius: 15px;
            text-align: center;
            border: 1px solid var(--border);
        }

        .milestones i {
            font-size: 1.8rem;
            color: var(--primary);
            margin-bottom: 0.5rem;
            display: block;
        }

        /* Contact Section */
        .contact-wrapper {
            display: flex;
            flex-wrap: wrap;
            gap: 3rem;
        }

        .contact-info, .contact-form-card {
            flex: 1;
        }

        .contact-details div {
            margin: 1.2rem 0;
            display: flex;
            align-items: center;
            gap: 1rem;
        }

        .contact-details i {
            width: 30px;
            color: var(--primary);
            font-size: 1.2rem;
        }

        .contact-details a {
            color: var(--text);
            text-decoration: none;
        }

        .contact-details a:hover {
            color: var(--primary);
        }

        .contact-flags {
            display: flex;
            gap: 0.5rem;
            align-items: center;
            font-size: 0.8rem;
            color: var(--text-light);
        }

        .social-links {
            display: flex;
            gap: 1.2rem;
            margin-top: 2rem;
        }

        .social-links a {
            background: var(--card-bg);
            width: 45px;
            height: 45px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--text);
            font-size: 1.3rem;
            transition: var(--transition);
            border: 1px solid var(--border);
        }

        .social-links a:hover {
            background: var(--primary);
            color: white;
        }

        /* Form Styles */
        .contact-form-card {
            background: var(--card-bg);
            padding: 2rem;
            border-radius: 24px;
            box-shadow: var(--shadow);
            border: 1px solid var(--border);
        }

        .contact-form-card h3 {
            margin-bottom: 1.5rem;
            color: var(--primary);
        }

        .form-group {
            margin-bottom: 1.2rem;
        }

        .form-group input, .form-group textarea {
            width: 100%;
            padding: 12px 16px;
            border-radius: 12px;
            border: 1px solid var(--border);
            background: var(--bg);
            color: var(--text);
            font-family: inherit;
        }

        .form-group input:focus, .form-group textarea:focus {
            outline: none;
            border-color: var(--primary);
        }

        .error-msg {
            color: #ef4444;
            font-size: 0.7rem;
            display: block;
            margin-top: 0.3rem;
        }

        .form-feedback {
            margin-top: 1rem;
            font-weight: 500;
            text-align: center;
        }

        .submit-btn {
            width: 100%;
            margin-top: 0.5rem;
        }

        /* Footer */
        footer {
            text-align: center;
            padding: 2rem;
            border-top: 1px solid var(--border);
            margin-top: 2rem;
            color: var(--text-light);
            font-size: 0.85rem;
        }

        footer a {
            color: var(--primary);
            text-decoration: none;
        }

        .loading-spinner {
            text-align: center;
            padding: 3rem;
        }

        .no-results {
            text-align: center;
            padding: 3rem;
        }

        /* Responsive */
        @media (max-width: 768px) {
            .language-switcher {
                top: 10px;
                left: 10px;
                padding: 5px 8px;
            }
            
            .lang-btn {
                padding: 4px 8px;
                font-size: 0.7rem;
            }
            
            .theme-toggle-wrapper {
                top: 10px;
                right: 10px;
            }
            
            .nav-links {
                display: none;
                flex-direction: column;
                background: var(--navbar-bg);
                position: absolute;
                top: 70px;
                left: 0;
                width: 100%;
                padding: 1.5rem;
                text-align: center;
                gap: 1.2rem;
                border-bottom: 1px solid var(--border);
            }
            
            .nav-links.active {
                display: flex;
            }
            
            .hamburger {
                display: block;
            }
            
            .hero h1 {
                font-size: 2rem;
            }
            
            .hero-image i {
                font-size: 3rem;
            }
            
            .filter-bar {
                flex-direction: column;
            }
            
            .search-input {
                width: 100%;
            }
            
            .contact-wrapper {
                flex-direction: column;
            }
        }

        @media (max-width: 480px) {
            .hero-buttons {
                display: flex;
                flex-direction: column;
                gap: 1rem;
            }
            
            .feature-card {
                width: 100%;
            }
        }
    </style>
</head>
<body>

    <!-- Language Switcher -->
    <div class="language-switcher">
        <button class="lang-btn active" data-lang="ru">🇷🇺 RU</button>
        <button class="lang-btn" data-lang="en">🇬🇧 EN</button>
        <button class="lang-btn" data-lang="hi">🇮🇳 HI</button>
        <button class="lang-btn" data-lang="ar">🇸🇦 AR</button>
    </div>

    <!-- Theme Toggle -->
    <div class="theme-toggle-wrapper">
        <button class="theme-toggle" id="themeToggle">
            <i class="fas fa-moon"></i>
            <i class="fas fa-sun"></i>
        </button>
    </div>

    <!-- Navigation -->
    <nav class="navbar">
        <div class="nav-container">
            <div class="logo">
                <i class="fas fa-seedling"></i> 
                <span class="brand-name">AMani Exports</span>
            </div>
            <ul class="nav-links" id="navLinks">
                <li><a href="#home" class="nav-link active" data-page="home" data-key="nav_home">Home</a></li>
                <li><a href="#products" class="nav-link" data-page="products" data-key="nav_products">Products</a></li>
                <li><a href="#countries" class="nav-link" data-page="countries" data-key="nav_markets">Export Markets</a></li>
                <li><a href="#about" class="nav-link" data-page="about" data-key="nav_about">About Us</a></li>
                <li><a href="#contact" class="nav-link" data-page="contact" data-key="nav_contact">Contact</a></li>
            </ul>
            <div class="hamburger" id="hamburger">
                <i class="fas fa-bars"></i>
            </div>
        </div>
    </nav>

    <main id="app">
        <!-- Home Page -->
        <section id="home-page" class="page active-page">
            <div class="hero">
                <div class="hero-content">
                    <span class="badge" data-key="badge">🇮🇳 India's Premium Exporter</span>
                    <h1><span data-key="hero_title1">Global Journey of</span> <span class="highlight" data-key="hero_title2">Freshness</span></h1>
                    <p data-key="hero_desc">AMani Exports - 15+ years of excellence, exporting to 25+ countries worldwide. Trusted supplier of fresh fruits and vegetables to Russia, Europe, and Gulf nations including Qatar, Bahrain, Kuwait, and Saudi Arabia.</p>
                    <div class="stats">
                        <div class="stat"><span>25+</span> <span data-key="stat_countries">Countries</span></div>
                        <div class="stat"><span>500+</span> <span data-key="stat_tons">Tons/Month</span></div>
                        <div class="stat"><span>100%</span> <span data-key="stat_fresh">Fresh</span></div>
                    </div>
                    <div class="hero-buttons">
                        <button class="btn-primary" id="viewProductsBtn" data-key="btn_products">🍎 View Products</button>
                        <button class="btn-secondary" id="contactQuickBtn" data-key="btn_inquiry">📞 Export Inquiry</button>
                    </div>
                </div>
                <div class="hero-image">
                    <i class="fas fa-apple-alt"></i>
                    <i class="fas fa-carrot"></i>
                    <i class="fas fa-shipping-fast"></i>
                </div>
            </div>
            
            <div class="features">
                <div class="feature-card">
                    <i class="fas fa-leaf"></i>
                    <h3 data-key="feature1_title">100% Fresh</h3>
                    <p data-key="feature1_desc">Direct from farm with cold chain</p>
                </div>
                <div class="feature-card">
                    <i class="fas fa-globe"></i>
                    <h3 data-key="feature2_title">Global Reach</h3>
                    <p data-key="feature2_desc">Russia, Europe, Gulf, Middle East</p>
                </div>
                <div class="feature-card">
                    <i class="fas fa-certificate"></i>
                    <h3 data-key="feature3_title">Certified Quality</h3>
                    <p data-key="feature3_desc">Global GAP, ISO 22000, APEDA</p>
                </div>
            </div>
        </section>

        <!-- Products Page -->
        <section id="products-page" class="page">
            <div class="container">
                <h2 class="section-title"><i class="fas fa-apple-alt"></i> <span data-key="products_title">Our Premium Products</span></h2>
                <div class="filter-bar">
                    <input type="text" id="productSearch" placeholder="🔍 Search products..." class="search-input" data-key-placeholder="search_placeholder">
                    <div class="filter-buttons">
                        <button class="filter-chip active" data-filter="all" data-key="filter_all">All</button>
                        <button class="filter-chip" data-filter="Fruits" data-key="filter_fruits">🍎 Fruits</button>
                        <button class="filter-chip" data-filter="Vegetables" data-key="filter_veg">🥬 Vegetables</button>
                        <button class="filter-chip" data-filter="Special" data-key="filter_special">⭐ Special</button>
                    </div>
                </div>
                <div id="productsGrid" class="products-grid">
                    <div class="loading-spinner"><i class="fas fa-spinner fa-pulse"></i> <span data-key="loading">Loading products...</span></div>
                </div>
            </div>
        </section>

        <!-- Export Markets Page -->
        <section id="countries-page" class="page">
            <div class="container">
                <h2 class="section-title"><i class="fas fa-map-marked-alt"></i> <span data-key="markets_title">Our Export Destinations</span></h2>
                <div class="countries-showcase">
                    <div class="region">
                        <h3><i class="fas fa-globe-europe"></i> <span data-key="region_europe">Europe</span></h3>
                        <div class="country-list" data-key="europe_countries">Russia, Germany, France, Netherlands, United Kingdom</div>
                    </div>
                    <div class="region">
                        <h3><i class="fas fa-oil-can"></i> <span data-key="region_gcc">Gulf Cooperation Council</span></h3>
                        <div class="country-list" data-key="gcc_countries">🇶🇦 Qatar, 🇧🇭 Bahrain, 🇰🇼 Kuwait, 🇸🇦 Saudi Arabia, 🇴🇲 Oman, 🇦🇪 UAE</div>
                    </div>
                    <div class="region">
                        <h3><i class="fas fa-map"></i> <span data-key="region_other">Other Markets</span></h3>
                        <div class="country-list" data-key="other_countries">Canada, Malaysia, Singapore, Bangladesh, Sri Lanka</div>
                    </div>
                </div>
                <div class="export-map">
                    <i class="fas fa-chart-line"></i>
                    <p data-key="export_growth">35% export growth in 2024-25 | Leading supplier in the Gulf region</p>
                </div>
            </div>
        </section>

        <!-- About Page -->
        <section id="about-page" class="page">
            <div class="container about-container">
                <h2 class="section-title"><span data-key="about_title">About AMani Exports</span></h2>
                <p data-key="about_desc1">We are a premier fresh fruit and vegetable exporter from India, dedicated to delivering the finest quality produce to global markets. Our journey began in 2008, and today we proudly serve over 25 countries.</p>
                <p><strong data-key="mission_title">Our Mission:</strong> <span data-key="mission_desc">To bring the richness of Indian agriculture to the world, ensuring international quality standards while supporting local farmers.</span></p>
                <div class="milestones">
                    <div><i class="fas fa-truck"></i> <span data-key="milestone1">5000+ Shipments</span></div>
                    <div><i class="fas fa-smile"></i> <span data-key="milestone2">200+ Happy Clients</span></div>
                    <div><i class="fas fa-award"></i> <span data-key="milestone3">FSSAI & APEDA Certified</span></div>
                    <div><i class="fas fa-clock"></i> <span data-key="milestone4">15+ Years Experience</span></div>
                </div>
            </div>
        </section>

        <!-- Contact Page -->
        <section id="contact-page" class="page">
            <div class="container contact-wrapper">
                <div class="contact-info">
                    <h2 class="section-title"><span data-key="contact_title">Export Inquiry</span></h2>
                    <p data-key="contact_desc">Based in Russia, Europe, or the Gulf region? Contact us for bulk orders.</p>
                    <div class="contact-details">
                        <div><i class="fas fa-phone-alt"></i> <a href="tel:+917040118014">+91 7040118014</a> <span class="contact-flags">(🇮🇳 India)</span></div>
                        <div><i class="fas fa-phone-alt"></i> <a href="tel:+79934674423">+7 993 467 4423</a> <span class="contact-flags">(🇷🇺 Russia)</span></div>
                        <div><i class="fas fa-envelope"></i> <a href="mailto:rafeymaniyar@gmail.com">rafeymaniyar@gmail.com</a></div>
                        <div><i class="fas fa-map-marker-alt"></i> Mumbai, India (Head Office)</div>
                    </div>
                    <div class="social-links">
                        <a href="https://wa.me/917040118014" target="_blank"><i class="fab fa-whatsapp"></i></a>
                        <a href="https://wa.me/79934674423" target="_blank"><i class="fab fa-whatsapp"></i> <span style="font-size: 0.7rem;">RU</span></a>
                        <a href="mailto:rafeymaniyar@gmail.com"><i class="fas fa-envelope"></i></a>
                    </div>
                </div>
                <div class="contact-form-card">
                    <form id="contactForm">
                        <h3 data-key="form_title">Send Inquiry</h3>
                        <div class="form-group">
                            <input type="text" id="name" placeholder="Full Name / Company" required data-key-placeholder="form_name">
                            <small class="error-msg" id="nameError"></small>
                        </div>
                        <div class="form-group">
                            <input type="email" id="email" placeholder="Email Address" required data-key-placeholder="form_email">
                            <small class="error-msg" id="emailError"></small>
                        </div>
                        <div class="form-group">
                            <input type="text" id="country" placeholder="Country" required data-key-placeholder="form_country">
                            <small class="error-msg" id="countryError"></small>
                        </div>
                        <div class="form-group">
                            <textarea id="message" rows="4" placeholder="Product requirements / Quantity..." required data-key-placeholder="form_message"></textarea>
                            <small class="error-msg" id="messageError"></small>
                        </div>
                        <button type="submit" class="btn-primary submit-btn"><span data-key="form_submit">Send Inquiry</span> <i class="fas fa-paper-plane"></i></button>
                        <div id="formFeedback" class="form-feedback"></div>
                    </form>
                </div>
            </div>
        </section>
    </main>

    <footer>
        <p>© 2025 AMani Exports | <span data-key="footer_text">Export to Russia, Europe, Gulf (Qatar, Bahrain, Kuwait, Saudi Arabia)</span> | <a href="mailto:rafeymaniyar@gmail.com">rafeymaniyar@gmail.com</a> | +91 7040118014 | +7 993 467 4423</p>
    </footer>

    <script>
        // Language Translations
        const translations = {
            ru: {
                nav_home: "Главная",
                nav_products: "Продукты",
                nav_markets: "Рынки экспорта",
                nav_about: "О нас",
                nav_contact: "Контакты",
                badge: "🇷🇺 Ведущий экспортер Индии",
                hero_title1: "Глобальное путешествие",
                hero_title2: "свежести",
                hero_desc: "AMani Exports - 15+ лет опыта, экспорт в 25+ стран мира. Надежный поставщик свежих фруктов и овощей в Россию, Европу и страны Персидского залива: Катар, Бахрейн, Кувейт, Саудовская Аравия.",
                stat_countries: "Стран",
                stat_tons: "Тонн/мес",
                stat_fresh: "Свежесть",
                btn_products: "🍎 Смотреть продукты",
                btn_inquiry: "📞 Запрос на экспорт",
                feature1_title: "100% Свежие",
                feature1_desc: "Прямо с фермы, холодная цепь",
                feature2_title: "Глобальный охват",
                feature2_desc: "Россия, Европа, Персидский залив",
                feature3_title: "Сертифицированное качество",
                feature3_desc: "Global GAP, ISO 22000, APEDA",
                products_title: "Наши премиальные продукты",
                search_placeholder: "🔍 Поиск продуктов...",
                filter_all: "Все",
                filter_fruits: "🍎 Фрукты",
                filter_veg: "🥬 Овощи",
                filter_special: "⭐ Особые",
                loading: "Загрузка продуктов...",
                markets_title: "Наши направления экспорта",
                region_europe: "Европа",
                europe_countries: "Россия, Германия, Франция, Нидерланды, Великобритания",
                region_gcc: "Совет сотрудничества стран Персидского залива",
                gcc_countries: "🇶🇦 Катар, 🇧🇭 Бахрейн, 🇰🇼 Кувейт, 🇸🇦 Саудовская Аравия, 🇴🇲 Оман, 🇦🇪 ОАЭ",
                region_other: "Другие рынки",
                other_countries: "Канада, Малайзия, Сингапур, Бангладеш, Шри-Ланка",
                export_growth: "Рост экспорта на 35% в 2024-25 | Ведущий поставщик в регионе Персидского залива",
                about_title: "О компании AMani Exports",
                about_desc1: "Мы ведущий экспортер свежих фруктов и овощей из Индии, стремящийся поставлять продукцию высочайшего качества на мировые рынки. Наш путь начался в 2008 году, и сегодня мы гордо обслуживаем более 25 стран.",
                mission_title: "Наша миссия:",
                mission_desc: "Донести богатство индийского сельского хозяйства до мира, обеспечивая международные стандарты качества и поддерживая местных фермеров.",
                milestone1: "5000+ Отгрузок",
                milestone2: "200+ Довольных клиентов",
                milestone3: "Сертификация FSSAI и APEDA",
                milestone4: "15+ Лет опыта",
                contact_title: "Экспортный запрос",
                contact_desc: "Находитесь в России, Европе или странах Персидского залива? Свяжитесь с нами для оптовых заказов.",
                form_title: "Отправить запрос",
                form_name: "Полное имя / Компания",
                form_email: "Email адрес",
                form_country: "Страна",
                form_message: "Требования к продукту / Количество...",
                form_submit: "Отправить запрос",
                footer_text: "Экспорт в Россию, Европу, страны Персидского залива (Катар, Бахрейн, Кувейт, Саудовская Аравия)"
            },
            en: {
                nav_home: "Home",
                nav_products: "Products",
                nav_markets: "Export Markets",
                nav_about: "About Us",
                nav_contact: "Contact",
