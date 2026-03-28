<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">
    <title>AMani Exports | Premium Fruits & Vegetables Export from India</title>
    <meta name="description" content="AMani Exports - Premium fresh fruits and vegetables export from India to Russia, Europe, Gulf Countries (Qatar, Bahrain, Kuwait, Saudi Arabia) and worldwide. Quality guaranteed since 2008.">
    <meta name="keywords" content="fruit export India, vegetable export, Russia import, Gulf countries, Qatar, Bahrain, Kuwait, Saudi Arabia, fresh produce">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <link rel="stylesheet" href="css/style.css">
</head>
<body>

    <!-- Dark/Light Theme Toggle -->
    <div class="theme-toggle-wrapper">
        <button class="theme-toggle" id="themeToggle" aria-label="Toggle Theme">
            <i class="fas fa-moon"></i>
            <i class="fas fa-sun"></i>
        </button>
    </div>

    <!-- Navigation Bar -->
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

    <main id="app" class="app-container">
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
                    <div class="hero-img-wrapper">
                        <i class="fas fa-apple-alt"></i>
                        <i class="fas fa-carrot"></i>
                        <i class="fas fa-shipping-fast"></i>
                    </div>
                </div>
            </div>
            
            <!-- Features Section -->
            <div class="features">
                <div class="feature-card">
                    <i class="fas fa-leaf"></i>
                    <h3>100% Fresh</h3>
                    <p>Direct from farm with cold chain logistics</p>
                </div>
                <div class="feature-card">
                    <i class="fas fa-globe"></i>
                    <h3>Global Reach</h3>
                    <p>Russia, Europe, Gulf, Middle East</p>
                </div>
                <div class="feature-card">
                    <i class="fas fa-certificate"></i>
                    <h3>Certified Quality</h3>
                    <p>Global GAP, ISO 22000, APEDA Registered</p>
                </div>
            </div>
        </section>

        <!-- Products Page (Dynamic Data) -->
        <section id="products-page" class="page">
            <div class="container">
                <h2 class="section-title"><i class="fas fa-apple-alt"></i> Our Premium Products</h2>
                <!-- Search and Filter -->
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
                        <div class="country-list">Russia, Germany, France, Netherlands, United Kingdom, Poland</div>
                    </div>
                    <div class="region">
                        <h3><i class="fas fa-oil-can"></i> Gulf Cooperation Council</h3>
                        <div class="country-list">🇶🇦 Qatar, 🇧🇭 Bahrain, 🇰🇼 Kuwait, 🇸🇦 Saudi Arabia, 🇴🇲 Oman, 🇦🇪 UAE</div>
                    </div>
                    <div class="region">
                        <h3><i class="fas fa-map"></i> Other Markets</h3>
                        <div class="country-list">Canada, Malaysia, Singapore, Bangladesh, Sri Lanka, Maldives</div>
                    </div>
                </div>
                <div class="export-map">
                    <i class="fas fa-chart-line"></i>
                    <p>35% export growth in 2024-25 | Leading supplier in the Gulf region</p>
                </div>
            </div>
        </section>

        <!-- About Us Page -->
        <section id="about-page" class="page">
            <div class="container about-container">
                <div class="about-text">
                    <h2 class="section-title">About AMani Exports</h2>
                    <p>We are a premier fresh fruit and vegetable exporter from India, dedicated to delivering the finest quality produce to global markets. Our journey began in 2008, and today we proudly serve over 25 countries with unwavering commitment to quality and freshness.</p>
                    <p><strong>Our Mission:</strong> To bring the richness of Indian agriculture to the world, ensuring international quality standards while supporting local farmers with fair trade practices.</p>
                    <div class="milestones">
                        <div><i class="fas fa-truck"></i> 5000+ Shipments</div>
                        <div><i class="fas fa-smile"></i> 200+ Happy Clients</div>
                        <div><i class="fas fa-award"></i> FSSAI & APEDA Certified</div>
                        <div><i class="fas fa-clock"></i> 15+ Years Experience</div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Contact Page -->
        <section id="contact-page" class="page">
            <div class="container contact-wrapper">
                <div class="contact-info">
                    <h2 class="section-title">Export Inquiry</h2>
                    <p>Based in Russia, Europe, or the Gulf region? Contact us for bulk orders and partnership opportunities.</p>
                    <div class="contact-details">
                        <div><i class="fas fa-phone-alt"></i> <a href="tel:+917040118014">+91 7040118014</a></div>
                        <div><i class="fas fa-envelope"></i> <a href="mailto:rafeymaniyar@gmail.com">rafeymaniyar@gmail.com</a></div>
                        <div><i class="fas fa-map-marker-alt"></i> Mumbai, India (Head Office)</div>
                        <div><i class="fas fa-clock"></i> Mon-Sat: 9:00 AM - 7:00 PM IST</div>
                    </div>
                    <div class="social-links">
                        <a href="#" aria-label="WhatsApp"><i class="fab fa-whatsapp"></i></a>
                        <a href="#" aria-label="LinkedIn"><i class="fab fa-linkedin"></i></a>
                        <a href="#" aria-label="Email"><i class="fas fa-envelope"></i></a>
                    </div>
                </div>
                <div class="contact-form-card">
                    <form id="contactForm">
                        <h3>Send Inquiry</h3>
                        <div class="form-group">
                            <input type="text" id="name" placeholder="Full Name / Company Name" required>
                            <small class="error-msg" id="nameError"></small>
                        </div>
                        <div class="form-group">
                            <input type="email" id="email" placeholder="Email Address" required>
                            <small class="error-msg" id="emailError"></small>
                        </div>
                        <div class="form-group">
                            <input type="text" id="country" placeholder="Country (Russia, Qatar, etc.)" required>
                            <small class="error-msg" id="countryError"></small>
                        </div>
                        <div class="form-group">
                            <textarea id="message" rows="4" placeholder="Product requirements / Quantity / Specific details..." required></textarea>
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
        <p>© 2025 AMani Exports | Premium Fruits & Vegetables Export from India to Russia, Europe, Gulf (Qatar, Bahrain, Kuwait, Saudi Arabia) | <a href="mailto:rafeymaniyar@gmail.com">rafeymaniyar@gmail.com</a> | +91 7040118014</p>
    </footer>

    <script src="js/main.js"></script>
</body>
</html>
