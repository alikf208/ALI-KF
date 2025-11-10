<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Jixoric Cars | Modern Car Buying Experience</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        /* CSS Variables */
        :root {
            --primary: #1a3a5f;
            --secondary: #f8b400;
            --accent: #e74c3c;
            --light: #f5f7fa;
            --dark: #2c3e50;
            --gray: #95a5a6;
            --transition: all 0.3s ease;
        }

        /* Reset & Base Styles */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background-color: var(--light);
            color: var(--dark);
            line-height: 1.6;
        }

        a {
            text-decoration: none;
            color: inherit;
        }

        ul {
            list-style: none;
        }

        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
        }

        .btn {
            display: inline-block;
            padding: 12px 24px;
            background: var(--primary);
            color: white;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            font-weight: 600;
            transition: var(--transition);
        }

        .btn:hover {
            background: #152a42;
            transform: translateY(-2px);
        }

        .btn-secondary {
            background: var(--secondary);
            color: var(--dark);
        }

        .btn-secondary:hover {
            background: #e6a500;
        }

        .section-title {
            text-align: center;
            margin-bottom: 40px;
            position: relative;
        }

        .section-title h2 {
            font-size: 2.2rem;
            color: var(--primary);
            margin-bottom: 10px;
        }

        .section-title::after {
            content: '';
            position: absolute;
            width: 80px;
            height: 3px;
            background: var(--secondary);
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
        }

        /* Header Styles */
        header {
            background-color: white;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 15px 0;
        }

        .logo {
            display: flex;
            align-items: center;
        }

        .logo h1 {
            font-size: 1.8rem;
            color: var(--primary);
            margin-left: 10px;
        }

        .logo span {
            color: var(--secondary);
        }

        nav ul {
            display: flex;
        }

        nav ul li {
            margin-left: 25px;
        }

        nav ul li a {
            font-weight: 500;
            transition: var(--transition);
            position: relative;
        }

        nav ul li a:hover {
            color: var(--secondary);
        }

        nav ul li a::after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            background: var(--secondary);
            bottom: -5px;
            left: 0;
            transition: var(--transition);
        }

        nav ul li a:hover::after {
            width: 100%;
        }

        .header-actions {
            display: flex;
            align-items: center;
        }

        .search-icon, .user-icon, .cart-icon {
            margin-left: 20px;
            font-size: 1.2rem;
            cursor: pointer;
            transition: var(--transition);
        }

        .search-icon:hover, .user-icon:hover, .cart-icon:hover {
            color: var(--secondary);
        }

        .mobile-menu {
            display: none;
            font-size: 1.5rem;
            cursor: pointer;
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(26, 58, 95, 0.8), rgba(26, 58, 95, 0.9)), url('https://images.unsplash.com/photo-1494976388531-d1058494cdd8?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80');
            background-size: cover;
            background-position: center;
            color: white;
            padding: 100px 0;
            text-align: center;
        }

        .hero-content {
            max-width: 800px;
            margin: 0 auto;
        }

        .hero h2 {
            font-size: 3rem;
            margin-bottom: 20px;
        }

        .hero p {
            font-size: 1.2rem;
            margin-bottom: 30px;
            opacity: 0.9;
        }

        .hero-buttons {
            display: flex;
            justify-content: center;
            gap: 20px;
        }

        /* Search Section */
        .search-section {
            background: white;
            padding: 40px 0;
            margin-top: -50px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            position: relative;
            z-index: 10;
        }

        .search-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
        }

        .search-box {
            display: flex;
            flex-direction: column;
        }

        .search-box label {
            margin-bottom: 8px;
            font-weight: 500;
            color: var(--dark);
        }

        .search-box select, .search-box input {
            padding: 12px;
            border: 1px solid #ddd;
            border-radius: 4px;
            font-size: 1rem;
        }

        .search-button {
            align-self: flex-end;
        }

        /* Featured Cars */
        .featured-cars {
            padding: 80px 0;
        }

        .cars-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 30px;
        }

        .car-card {
            background: white;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            transition: var(--transition);
        }

        .car-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
        }

        .car-image {
            height: 200px;
            overflow: hidden;
        }

        .car-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: var(--transition);
        }

        .car-card:hover .car-image img {
            transform: scale(1.05);
        }

        .car-details {
            padding: 20px;
        }

        .car-title {
            display: flex;
            justify-content: space-between;
            margin-bottom: 10px;
        }

        .car-title h3 {
            font-size: 1.3rem;
            color: var(--primary);
        }

        .car-price {
            font-weight: 700;
            color: var(--accent);
            font-size: 1.2rem;
        }

        .car-specs {
            display: flex;
            justify-content: space-between;
            margin: 15px 0;
            color: var(--gray);
        }

        .car-specs span {
            display: flex;
            align-items: center;
        }

        .car-specs i {
            margin-right: 5px;
        }

        .car-actions {
            display: flex;
            justify-content: space-between;
            margin-top: 20px;
        }

        /* Why Choose Us */
        .why-choose {
            background: var(--primary);
            color: white;
            padding: 80px 0;
        }

        .why-choose .section-title h2 {
            color: white;
        }

        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
        }

        .feature-card {
            text-align: center;
            padding: 30px 20px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 8px;
            transition: var(--transition);
        }

        .feature-card:hover {
            transform: translateY(-5px);
            background: rgba(255, 255, 255, 0.15);
        }

        .feature-icon {
            font-size: 2.5rem;
            color: var(--secondary);
            margin-bottom: 20px;
        }

        .feature-card h3 {
            margin-bottom: 15px;
            font-size: 1.3rem;
        }

        /* Testimonials */
        .testimonials {
            padding: 80px 0;
            background: white;
        }

        .testimonials-container {
            max-width: 800px;
            margin: 0 auto;
        }

        .testimonial-slider {
            position: relative;
            overflow: hidden;
        }

        .testimonial-slide {
            padding: 30px;
            text-align: center;
            display: none;
        }

        .testimonial-slide.active {
            display: block;
            animation: fadeIn 0.5s ease;
        }

        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        .testimonial-content {
            background: var(--light);
            padding: 30px;
            border-radius: 8px;
            margin-bottom: 20px;
            position: relative;
        }

        .testimonial-content::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 0;
            height: 0;
            border-left: 10px solid transparent;
            border-right: 10px solid transparent;
            border-top: 10px solid var(--light);
        }

        .client-info {
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .client-avatar {
            width: 60px;
            height: 60px;
            border-radius: 50%;
            overflow: hidden;
            margin-right: 15px;
        }

        .client-avatar img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .slider-controls {
            display: flex;
            justify-content: center;
            margin-top: 30px;
        }

        .slider-dot {
            width: 12px;
            height: 12px;
            border-radius: 50%;
            background: var(--gray);
            margin: 0 5px;
            cursor: pointer;
            transition: var(--transition);
        }

        .slider-dot.active {
            background: var(--primary);
        }

        /* Newsletter */
        .newsletter {
            background: linear-gradient(to right, var(--primary), #2c5282);
            color: white;
            padding: 60px 0;
            text-align: center;
        }

        .newsletter-content {
            max-width: 600px;
            margin: 0 auto;
        }

        .newsletter h2 {
            margin-bottom: 15px;
        }

        .newsletter p {
            margin-bottom: 30px;
            opacity: 0.9;
        }

        .newsletter-form {
            display: flex;
            max-width: 500px;
            margin: 0 auto;
        }

        .newsletter-form input {
            flex: 1;
            padding: 15px;
            border: none;
            border-radius: 4px 0 0 4px;
            font-size: 1rem;
        }

        .newsletter-form button {
            background: var(--secondary);
            color: var(--dark);
            border: none;
            padding: 0 25px;
            border-radius: 0 4px 4px 0;
            font-weight: 600;
            cursor: pointer;
            transition: var(--transition);
        }

        .newsletter-form button:hover {
            background: #e6a500;
        }

        /* Footer */
        footer {
            background: var(--dark);
            color: white;
            padding: 60px 0 20px;
        }

        .footer-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 40px;
            margin-bottom: 40px;
        }

        .footer-column h3 {
            font-size: 1.2rem;
            margin-bottom: 20px;
            color: var(--secondary);
            position: relative;
            padding-bottom: 10px;
        }

        .footer-column h3::after {
            content: '';
            position: absolute;
            width: 40px;
            height: 2px;
            background: var(--secondary);
            bottom: 0;
            left: 0;
        }

        .footer-column ul li {
            margin-bottom: 10px;
        }

        .footer-column ul li a {
            transition: var(--transition);
            opacity: 0.8;
        }

        .footer-column ul li a:hover {
            opacity: 1;
            color: var(--secondary);
            padding-left: 5px;
        }

        .social-links {
            display: flex;
            margin-top: 20px;
        }

        .social-links a {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 36px;
            height: 36px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            margin-right: 10px;
            transition: var(--transition);
        }

        .social-links a:hover {
            background: var(--secondary);
            color: var(--dark);
        }

        .footer-bottom {
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            font-size: 0.9rem;
            opacity: 0.7;
        }

        /* Responsive Styles */
        @media (max-width: 992px) {
            .hero h2 {
                font-size: 2.5rem;
            }
            
            .search-container {
                grid-template-columns: repeat(2, 1fr);
            }
        }

        @media (max-width: 768px) {
            nav {
                display: none;
            }
            
            .mobile-menu {
                display: block;
            }
            
            .hero h2 {
                font-size: 2rem;
            }
            
            .hero-buttons {
                flex-direction: column;
                gap: 10px;
            }
            
            .search-container {
                grid-template-columns: 1fr;
            }
            
            .newsletter-form {
                flex-direction: column;
            }
            
            .newsletter-form input {
                border-radius: 4px;
                margin-bottom: 10px;
            }
            
            .newsletter-form button {
                border-radius: 4px;
                padding: 15px;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container header-container">
            <div class="logo">
                <i class="fas fa-car" style="font-size: 2rem; color: var(--secondary);"></i>
                <h1>Jixoric <span>Cars</span></h1>
            </div>
            <nav>
                <ul>
                    <li><a href="#">Home</a></li>
                    <li><a href="#">Inventory</a></li>
                    <li><a href="#">Finance</a></li>
                    <li><a href="#">Services</a></li>
                    <li><a href="#">About</a></li>
                    <li><a href="#">Contact</a></li>
                </ul>
            </nav>
            <div class="header-actions">
                <div class="search-icon"><i class="fas fa-search"></i></div>
                <div class="user-icon"><i class="fas fa-user"></i></div>
                <div class="cart-icon"><i class="fas fa-shopping-cart"></i></div>
                <div class="mobile-menu"><i class="fas fa-bars"></i></div>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <div class="container hero-content">
            <h2>Find Your Perfect Car With Ease</h2>
            <p>Discover the best selection of quality vehicles at competitive prices. Your dream car is just a click away.</p>
            <div class="hero-buttons">
                <a href="#" class="btn">Browse Inventory</a>
                <a href="#" class="btn btn-secondary">Book a Test Drive</a>
            </div>
        </div>
    </section>

    <!-- Search Section -->
    <section class="search-section">
        <div class="container">
            <div class="search-container">
                <div class="search-box">
                    <label for="make">Make</label>
                    <select id="make">
                        <option value="">Any Make</option>
                        <option value="toyota">Toyota</option>
                        <option value="honda">Honda</option>
                        <option value="ford">Ford</option>
                        <option value="bmw">BMW</option>
                        <option value="mercedes">Mercedes</option>
                    </select>
                </div>
                <div class="search-box">
                    <label for="model">Model</label>
                    <select id="model">
                        <option value="">Any Model</option>
                        <option value="camry">Camry</option>
                        <option value="civic">Civic</option>
                        <option value="mustang">Mustang</option>
                        <option value="x5">X5</option>
                        <option value="c-class">C-Class</option>
                    </select>
                </div>
                <div class="search-box">
                    <label for="price">Max Price</label>
                    <select id="price">
                        <option value="">No Max</option>
                        <option value="10000">$10,000</option>
                        <option value="20000">$20,000</option>
                        <option value="30000">$30,000</option>
                        <option value="40000">$40,000</option>
                        <option value="50000">$50,000</option>
                    </select>
                </div>
                <div class="search-box">
                    <label for="year">Year</label>
                    <select id="year">
                        <option value="">Any Year</option>
                        <option value="2023">2023</option>
                        <option value="2022">2022</option>
                        <option value="2021">2021</option>
                        <option value="2020">2020</option>
                        <option value="2019">2019</option>
                    </select>
                </div>
                <div class="search-box search-button">
                    <button class="btn">Search Vehicles</button>
                </div>
            </div>
        </div>
    </section>

    <!-- Featured Cars -->
    <section class="featured-cars">
        <div class="container">
            <div class="section-title">
                <h2>Featured Vehicles</h2>
                <p>Check out our most popular cars</p>
            </div>
            <div class="cars-grid">
                <!-- Car 1 -->
                <div class="car-card">
                    <div class="car-image">
                        <img src="https://images.unsplash.com/photo-1549317661-bd32c8ce0db2?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80" alt="BMW X5">
                    </div>
                    <div class="car-details">
                        <div class="car-title">
                            <h3>BMW X5</h3>
                            <div class="car-price">$62,500</div>
                        </div>
                        <div class="car-specs">
                            <span><i class="fas fa-calendar-alt"></i> 2022</span>
                            <span><i class="fas fa-tachometer-alt"></i> 18K mi</span>
                            <span><i class="fas fa-gas-pump"></i> Hybrid</span>
                        </div>
                        <div class="car-actions">
                            <a href="#" class="btn">View Details</a>
                            <a href="#" class="btn btn-secondary">Compare</a>
                        </div>
                    </div>
                </div>
                
                <!-- Car 2 -->
                <div class="car-card">
                    <div class="car-image">
                        <img src="https://images.unsplash.com/photo-1555215695-3004980ad54e?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80" alt="Mercedes C-Class">
                    </div>
                    <div class="car-details">
                        <div class="car-title">
                            <h3>Mercedes C-Class</h3>
                            <div class="car-price">$45,800</div>
                        </div>
                        <div class="car-specs">
                            <span><i class="fas fa-calendar-alt"></i> 2023</span>
                            <span><i class="fas fa-tachometer-alt"></i> 8K mi</span>
                            <span><i class="fas fa-gas-pump"></i> Gasoline</span>
                        </div>
                        <div class="car-actions">
                            <a href="#" class="btn">View Details</a>
                            <a href="#" class="btn btn-secondary">Compare</a>
                        </div>
                    </div>
                </div>
                
                <!-- Car 3 -->
                <div class="car-card">
                    <div class="car-image">
                        <img src="https://images.unsplash.com/photo-1603584173870-7f23fdae1b7a?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2069&q=80" alt="Audi Q7">
                    </div>
                    <div class="car-details">
                        <div class="car-title">
                            <h3>Audi Q7</h3>
                            <div class="car-price">$58,900</div>
                        </div>
                        <div class="car-specs">
                            <span><i class="fas fa-calendar-alt"></i> 2021</span>
                            <span><i class="fas fa-tachometer-alt"></i> 22K mi</span>
                            <span><i class="fas fa-gas-pump"></i> Diesel</span>
                        </div>
                        <div class="car-actions">
                            <a href="#" class="btn">View Details</a>
                            <a href="#" class="btn btn-secondary">Compare</a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Why Choose Us -->
    <section class="why-choose">
        <div class="container">
            <div class="section-title">
                <h2>Why Choose Jixoric Cars</h2>
                <p>We provide the best car buying experience</p>
            </div>
            <div class="features-grid">
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-shield-alt"></i>
                    </div>
                    <h3>Quality Assurance</h3>
                    <p>All our vehicles undergo rigorous inspection and come with a comprehensive warranty.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-hand-holding-usd"></i>
                    </div>
                    <h3>Best Price Guarantee</h3>
                    <p>We offer competitive pricing and will match any verifiable competitor's offer.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-user-clock"></i>
                    </div>
                    <h3>Personalized Service</h3>
                    <p>Our experts provide tailored advice to help you find the perfect vehicle.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-tools"></i>
                    </div>
                    <h3>After-Sales Support</h3>
                    <p>Comprehensive maintenance and support services for your peace of mind.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Testimonials -->
    <section class="testimonials">
        <div class="container">
            <div class="section-title">
                <h2>What Our Customers Say</h2>
                <p>Real experiences from real customers</p>
            </div>
            <div class="testimonials-container">
                <div class="testimonial-slider">
                    <div class="testimonial-slide active">
                        <div class="testimonial-content">
                            <p>"I had an amazing experience buying my car from Jixoric. The process was smooth, and the staff was incredibly helpful. I got exactly what I was looking for at a great price!"</p>
                        </div>
                        <div class="client-info">
                            <div class="client-avatar">
                                <img src="https://randomuser.me/api/portraits/women/44.jpg" alt="Sarah Johnson">
                            </div>
                            <div>
                                <h4>Sarah Johnson</h4>
                                <p>Purchased a BMW X3</p>
                            </div>
                        </div>
                    </div>
                    <div class="testimonial-slide">
                        <div class="testimonial-content">
                            <p>"The financing options at Jixoric made it possible for me to get my dream car. The team worked with me to find a payment plan that fit my budget. Highly recommended!"</p>
                        </div>
                        <div class="client-info">
                            <div class="client-avatar">
                                <img src="https://randomuser.me/api/portraits/men/32.jpg" alt="Michael Chen">
                            </div>
                            <div>
                                <h4>Michael Chen</h4>
                                <p>Purchased an Audi A4</p>
                            </div>
                        </div>
                    </div>
                    <div class="testimonial-slide">
                        <div class="testimonial-content">
                            <p>"I was hesitant about buying a car online, but Jixoric made it so easy. The detailed vehicle history and virtual tour gave me confidence in my purchase. Great service!"</p>
                        </div>
                        <div class="client-info">
                            <div class="client-avatar">
                                <img src="https://randomuser.me/api/portraits/women/68.jpg" alt="Emily Rodriguez">
                            </div>
                            <div>
                                <h4>Emily Rodriguez</h4>
                                <p>Purchased a Toyota RAV4</p>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="slider-controls">
                    <div class="slider-dot active" data-slide="0"></div>
                    <div class="slider-dot" data-slide="1"></div>
                    <div class="slider-dot" data-slide="2"></div>
                </div>
            </div>
        </div>
    </section>

    <!-- Newsletter -->
    <section class="newsletter">
        <div class="container">
            <div class="newsletter-content">
                <h2>Stay Updated With Our Latest Offers</h2>
                <p>Subscribe to our newsletter and be the first to know about new arrivals and exclusive deals.</p>
                <form class="newsletter-form">
                    <input type="email" placeholder="Enter your email address" required>
                    <button type="submit">Subscribe</button>
                </form>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-container">
                <div class="footer-column">
                    <h3>Jixoric Cars</h3>
                    <p>Your trusted partner for quality vehicles. We're committed to providing the best car buying experience with transparency and integrity.</p>
                    <div class="social-links">
                        <a href="#"><i class="fab fa-facebook-f"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-linkedin-in"></i></a>
                    </div>
                </div>
                <div class="footer-column">
                    <h3>Quick Links</h3>
                    <ul>
                        <li><a href="#">Home</a></li>
                        <li><a href="#">Inventory</a></li>
                        <li><a href="#">Finance Options</a></li>
                        <li><a href="#">Services</a></li>
                        <li><a href="#">About Us</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Contact Us</h3>
                    <ul>
                        <li><i class="fas fa-map-marker-alt"></i> 123 Auto Avenue, Car City</li>
                        <li><i class="fas fa-phone"></i> +1 (555) 123-4567</li>
                        <li><i class="fas fa-envelope"></i> info@jixoriccars.com</li>
                        <li><i class="fas fa-clock"></i> Mon-Sat: 9AM - 7PM</li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Our Services</h3>
                    <ul>
                        <li><a href="#">Car Buying</a></li>
                        <li><a href="#">Car Selling</a></li>
                        <li><a href="#">Financing</a></li>
                        <li><a href="#">Vehicle Inspection</a></li>
                        <li><a href="#">Maintenance</a></li>
                    </ul>
                </div>
            </div>
            <div class="footer-bottom">
                <p>&copy; 2023 Jixoric Cars. All rights reserved.</p>
            </div>
        </div>
    </footer>

    <script>
        // Testimonial Slider
        document.addEventListener('DOMContentLoaded', function() {
            const slides = document.querySelectorAll('.testimonial-slide');
            const dots = document.querySelectorAll('.slider-dot');
            let currentSlide = 0;
            
            // Function to show a specific slide
            function showSlide(n) {
                slides.forEach(slide => slide.classList.remove('active'));
                dots.forEach(dot => dot.classList.remove('active'));
                
                slides[n].classList.add('active');
                dots[n].classList.add('active');
                currentSlide = n;
            }
            
            // Add click event to dots
            dots.forEach((dot, index) => {
                dot.addEventListener('click', () => {
                    showSlide(index);
                });
            });
            
            // Auto slide change
            setInterval(() => {
                currentSlide = (currentSlide + 1) % slides.length;
                showSlide(currentSlide);
            }, 5000);
            
            // Mobile menu toggle
            const mobileMenu = document.querySelector('.mobile-menu');
            const nav = document.querySelector('nav');
            
            mobileMenu.addEventListener('click', () => {
                nav.style.display = nav.style.display === 'block' ? 'none' : 'block';
            });
            
            // Search functionality (basic)
            const searchBtn = document.querySelector('.search-button .btn');
            searchBtn.addEventListener('click', function(e) {
                e.preventDefault();
                alert('Search functionality would be implemented here with real data.');
            });
            
            // Newsletter form submission
            const newsletterForm = document.querySelector('.newsletter-form');
            newsletterForm.addEventListener('submit', function(e) {
                e.preventDefault();
                const email = this.querySelector('input').value;
                alert(`Thank you for subscribing with ${email}! You'll receive our latest offers soon.`);
                this.reset();
            });
        });
    </script>
</body>
</html>
