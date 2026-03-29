<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">
    <title>AMani Exports | Premium Fruits & Vegetables Export from India</title>
    <meta name="description" content="AMani Exports - Premium fresh fruits and vegetables export from India to Russia, Europe, Gulf Countries (Qatar, Bahrain, Kuwait, Saudi Arabia) and worldwide.">
    <meta name="keywords" content="fruit export India, vegetable export, Russia, Gulf countries, Qatar, Bahrain, Kuwait, Saudi Arabia">
    <meta name="author" content="AMani Exports">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
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
            font-family: 'Poppins', sans-serif;
            background: var(--bg);
            color: var(--text);
            transition: background 0.3s, color 0.2s;
            line-height: 1.6;
            overflow-x: hidden;
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
                <span>AMani Exports</span>
            </div>
            <ul class="nav-links" id="navLinks">
                <li><a href="#home" class="nav-link active" data-page="home">Home</a></li>
                <li><a href="#products" class="nav-link" data-page="products">Products</a></li>
                <li><a href="#countries" class="nav-link" data-page="countries">Export Markets</a></li>
                <li><a href="#about" class="nav-link" data-page="about">About Us</a></li>
                <li><a href="#contact" class="nav-link" data-page="contact">Contact</a></li>
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
                    <span class="badge">🇮🇳 India's Premium Exporter</span>
                    <h1>Global Journey of <span class="highlight">Freshness</span></h1>
                    <p>AMani Exports - 15+ years of excellence, exporting to 25+ countries worldwide. Trusted supplier of fresh fruits and vegetables to Russia, Europe, and Gulf nations including Qatar, Bahrain, Kuwait, and Saudi Arabia.</p>
                    <div class="stats">
                        <div class="stat"><span>25+</span> Countries</div>
                        <div class="stat"><span>500+</span> Tons/Month</div>
                        <div class="stat"><span>100%</span> Fresh</div>
                    </div>
                    <div class="hero-buttons">
                        <button class="btn-primary" id="viewProductsBtn">🍎 View Products</button>
                        <button class="btn-secondary" id="contactQuickBtn">📞 Export Inquiry</button>
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
                    <h3>100% Fresh</h3>
                    <p>Direct from farm with cold chain</p>
                </div>
                <div class="feature-card">
                    <i class="fas fa-globe"></i>
                    <h3>Global Reach</h3>
                    <p>Russia, Europe, Gulf, Middle East</p>
                </div>
                <div class="feature-card">
                    <i class="fas fa-certificate"></i>
                    <h3>Certified Quality</h3>
                    <p>Global GAP, ISO 22000, APEDA</p>
                </div>
            </div>
        </section>

        <!-- Products Page -->
        <section id="products-page" class="page">
            <div class="container">
                <h2 class="section-title"><i class="fas fa-apple-alt"></i> Our Premium Products</h2>
                <div class="filter-bar">
                    <input type="text" id="productSearch" placeholder="🔍 Search products..." class="search-input">
                    <div class="filter-buttons">
                        <button class="filter-chip active" data-filter="all">All</button>
                        <button class="filter-chip" data-filter="Fruits">🍎 Fruits</button>
                        <button class="filter-chip" data-filter="Vegetables">🥬 Vegetables</button>
                        <button class="filter-chip" data-filter="Special">⭐ Special</button>
                    </div>
                </div>
                <div id="productsGrid" class="products-grid">
                    <div class="loading-spinner"><i class="fas fa-spinner fa-pulse"></i> Loading products...</div>
                </div>
            </div>
        </section>

        <!-- Export Markets Page -->
        <section id="countries-page" class="page">
            <div class="container">
                <h2 class="section-title"><i class="fas fa-map-marked-alt"></i> Our Export Destinations</h2>
                <div class="countries-showcase">
                    <div class="region">
                        <h3><i class="fas fa-globe-europe"></i> Europe</h3>
                        <div class="country-list">Russia, Germany, France, Netherlands, United Kingdom</div>
                    </div>
                    <div class="region">
                        <h3><i class="fas fa-oil-can"></i> Gulf Cooperation Council</h3>
                        <div class="country-list">🇶🇦 Qatar, 🇧🇭 Bahrain, 🇰🇼 Kuwait, 🇸🇦 Saudi Arabia, 🇴🇲 Oman, 🇦🇪 UAE</div>
                    </div>
                    <div class="region">
                        <h3><i class="fas fa-map"></i> Other Markets</h3>
                        <div class="country-list">Canada, Malaysia, Singapore, Bangladesh, Sri Lanka</div>
                    </div>
                </div>
                <div class="export-map">
                    <i class="fas fa-chart-line"></i>
                    <p>35% export growth in 2024-25 | Leading supplier in the Gulf region</p>
                </div>
            </div>
        </section>

        <!-- About Page -->
        <section id="about-page" class="page">
            <div class="container about-container">
                <h2 class="section-title">About AMani Exports</h2>
                <p>We are a premier fresh fruit and vegetable exporter from India, dedicated to delivering the finest quality produce to global markets. Our journey began in 2008, and today we proudly serve over 25 countries.</p>
                <p><strong>Our Mission:</strong> To bring the richness of Indian agriculture to the world, ensuring international quality standards while supporting local farmers.</p>
                <div class="milestones">
                    <div><i class="fas fa-truck"></i> 5000+ Shipments</div>
                    <div><i class="fas fa-smile"></i> 200+ Happy Clients</div>
                    <div><i class="fas fa-award"></i> FSSAI & APEDA Certified</div>
                    <div><i class="fas fa-clock"></i> 15+ Years Experience</div>
                </div>
            </div>
        </section>

        <!-- Contact Page -->
        <section id="contact-page" class="page">
            <div class="container contact-wrapper">
                <div class="contact-info">
                    <h2 class="section-title">Export Inquiry</h2>
                    <p>Based in Russia, Europe, or the Gulf region? Contact us for bulk orders.</p>
                    <div class="contact-details">
                        <div><i class="fas fa-phone-alt"></i> <a href="tel:+917040118014">+91 7040118014</a></div>
                        <div><i class="fas fa-envelope"></i> <a href="mailto:rafeymaniyar@gmail.com">rafeymaniyar@gmail.com</a></div>
                        <div><i class="fas fa-map-marker-alt"></i> Mumbai, India (Head Office)</div>
                    </div>
                    <div class="social-links">
                        <a href="https://wa.me/917040118014" target="_blank"><i class="fab fa-whatsapp"></i></a>
                        <a href="mailto:rafeymaniyar@gmail.com"><i class="fas fa-envelope"></i></a>
                    </div>
                </div>
                <div class="contact-form-card">
                    <form id="contactForm">
                        <h3>Send Inquiry</h3>
                        <div class="form-group">
                            <input type="text" id="name" placeholder="Full Name / Company" required>
                            <small class="error-msg" id="nameError"></small>
                        </div>
                        <div class="form-group">
                            <input type="email" id="email" placeholder="Email Address" required>
                            <small class="error-msg" id="emailError"></small>
                        </div>
                        <div class="form-group">
                            <input type="text" id="country" placeholder="Country" required>
                            <small class="error-msg" id="countryError"></small>
                        </div>
                        <div class="form-group">
                            <textarea id="message" rows="4" placeholder="Product requirements / Quantity..." required></textarea>
                            <small class="error-msg" id="messageError"></small>
                        </div>
                        <button type="submit" class="btn-primary submit-btn">Send Inquiry <i class="fas fa-paper-plane"></i></button>
                        <div id="formFeedback" class="form-feedback"></div>
                    </form>
                </div>
            </div>
        </section>
    </main>

    <footer>
        <p>© 2025 AMani Exports | Export to Russia, Europe, Gulf (Qatar, Bahrain, Kuwait, Saudi Arabia) | <a href="mailto:rafeymaniyar@gmail.com">rafeymaniyar@gmail.com</a> | +91 7040118014</p>
    </footer>

    <script>
        // Theme Toggle
        const themeToggle = document.getElementById('themeToggle');
        const currentTheme = localStorage.getItem('theme') || 'light';
        if (currentTheme === 'dark') document.documentElement.setAttribute('data-theme', 'dark');
        themeToggle?.addEventListener('click', () => {
            const isDark = document.documentElement.getAttribute('data-theme') === 'dark';
            document.documentElement.setAttribute('data-theme', isDark ? 'light' : 'dark');
            localStorage.setItem('theme', isDark ? 'light' : 'dark');
        });

        // SPA Routing
        const pages = ['home', 'products', 'countries', 'about', 'contact'];
        function showPage(pageId) {
            pages.forEach(p => {
                const el = document.getElementById(`${p}-page`);
                if (el) el.classList.remove('active-page');
            });
            const activePage = document.getElementById(`${pageId}-page`);
            if (activePage) activePage.classList.add('active-page');
            document.querySelectorAll('.nav-link').forEach(link => {
                const linkPage = link.getAttribute('data-page');
                if (linkPage === pageId) link.classList.add('active');
                else link.classList.remove('active');
            });
            window.history.pushState({ pageId }, '', `#${pageId}`);
        }

        document.querySelectorAll('.nav-link').forEach(link => {
            link.addEventListener('click', (e) => {
                e.preventDefault();
                const page = link.getAttribute('data-page');
                if (page) showPage(page);
                document.getElementById('navLinks')?.classList.remove('active');
            });
        });

        window.addEventListener('popstate', () => {
            const hash = window.location.hash.slice(1) || 'home';
            if (pages.includes(hash)) showPage(hash);
        });
        
        if (window.location.hash) {
            const hashPage = window.location.hash.slice(1);
            if (pages.includes(hashPage)) showPage(hashPage);
        } else showPage('home');

        // Buttons
        document.getElementById('viewProductsBtn')?.addEventListener('click', () => showPage('products'));
        document.getElementById('contactQuickBtn')?.addEventListener('click', () => showPage('contact'));

        // Product Data
        const productData = [
            { name: "Fresh Banana", category: "Fruits", exportTo: "Russia, Europe, Gulf", icon: "fa-apple-alt", desc: "Premium quality" },
            { name: "Alphonso Mango", category: "Fruits", exportTo: "Europe, Qatar, Saudi", icon: "fa-apple-alt", desc: "King of mangoes" },
            { name: "Seedless Grapes", category: "Fruits", exportTo: "Russia, Europe, UAE", icon: "fa-apple-alt", desc: "Sweet & fresh" },
            { name: "Red Onion", category: "Vegetables", exportTo: "Gulf, Europe, Russia", icon: "fa-carrot", desc: "Premium quality" },
            { name: "Fresh Tomato", category: "Vegetables", exportTo: "Kuwait, Qatar, UAE", icon: "fa-carrot", desc: "Farm fresh" },
            { name: "Bell Pepper", category: "Vegetables", exportTo: "Europe, Bahrain, Kuwait", icon: "fa-carrot", desc: "Export grade" },
            { name: "Pomegranate", category: "Special", exportTo: "Russia, Saudi, Europe", icon: "fa-apple-alt", desc: "Sweet & juicy" },
            { name: "Fresh Lemon", category: "Special", exportTo: "All Gulf, Europe", icon: "fa-lemon", desc: "Aromatic" }
        ];

        function renderProducts(filterText = '', categoryFilter = 'all') {
            const grid = document.getElementById('productsGrid');
            if (!grid) return;
            let filtered = productData.filter(p => {
                const matchText = p.name.toLowerCase().includes(filterText.toLowerCase()) || p.exportTo.toLowerCase().includes(filterText.toLowerCase());
                const matchCat = categoryFilter === 'all' || p.category === categoryFilter;
                return matchText && matchCat;
            });
            if (filtered.length === 0) {
                grid.innerHTML = '<p class="no-results">😢 No products found</p>';
                return;
            }
            grid.innerHTML = filtered.map(p => `
                <div class="product-card">
                    <i class="fas ${p.icon}"></i>
                    <h3>${p.name}</h3>
                    <p><strong>Category:</strong> ${p.category}</p>
                    <p><strong>Export Markets:</strong> ${p.exportTo}</p>
                    <p><small>${p.desc}</small></p>
                </div>
            `).join('');
        }

        const searchInput = document.getElementById('productSearch');
        let currentFilter = 'all';
        if (searchInput) {
            searchInput.addEventListener('input', (e) => renderProducts(e.target.value, currentFilter));
            document.querySelectorAll('.filter-chip').forEach(chip => {
                chip.addEventListener('click', () => {
                    document.querySelectorAll('.filter-chip').forEach(c => c.classList.remove('active'));
                    chip.classList.add('active');
                    currentFilter = chip.getAttribute('data-filter');
                    renderProducts(searchInput.value, currentFilter);
                });
            });
            renderProducts('', 'all');
        }

        // Contact Form Validation
        const contactForm = document.getElementById('contactForm');
        if(contactForm){
            contactForm.addEventListener('submit', (e) => {
                e.preventDefault();
                let isValid = true;
                const name = document.getElementById('name');
                const email = document.getElementById('email');
                const country = document.getElementById('country');
                const message = document.getElementById('message');
                const feedback = document.getElementById('formFeedback');
                
                if(!name.value.trim()){ isValid=false; }
                if(!email.value.trim() || !email.value.includes('@')){ isValid=false; }
                if(!country.value.trim()){ isValid=false; }
                if(!message.value.trim()){ isValid=false; }
                
                if(isValid){
                    feedback.innerHTML = '<span style="color:green;">✅ Inquiry sent! We will contact you within 24 hours.</span>';
                    contactForm.reset();
                    setTimeout(()=> feedback.innerHTML='', 4000);
                } else {
                    feedback.innerHTML = '<span style="color:red;">❌ Please fill all fields correctly.</span>';
                }
            });
        }

        // Hamburger Menu
        const hamburger = document.getElementById('hamburger');
        hamburger?.addEventListener('click', () => {
            document.getElementById('navLinks').classList.toggle('active');
        });
    </script>
</body>
</html>
