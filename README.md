<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=yes, viewport-fit=cover">
  <title>Golden Nest • Premium Poultry Farm</title>
  <!-- Google Fonts for modern typography -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,400;14..32,500;14..32,600;14..32,700&family=Playfair+Display:ital,wght@0,500;0,600;0,700;1,500&display=swap" rel="stylesheet">
  <!-- Font Awesome 6 for icons -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
  <style>
    /* ----- RESET & BASE STYLES (Mobile-First) ----- */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Inter', sans-serif;
      background: #f8f6f0;
      color: #1e2b1c;
      line-height: 1.5;
      scroll-behavior: smooth;
    }

    h1, h2, h3, .serif {
      font-family: 'Playfair Display', serif;
    }

    /* Color palette: dark green #1a2f1d, black #0f0f0f, gold #c4a44a */
    :root {
      --deep-green: #1a2f1d;
      --black: #111;
      --gold: #c4a44a;
      --gold-light: #dfc27d;
      --cream: #fefcf5;
      --glass-bg: rgba(255, 255, 255, 0.2);
      --glass-border: rgba(255, 255, 255, 0.35);
      --card-shadow: 0 10px 25px rgba(0,0,0,0.08);
      --transition: 0.3s ease;
    }

    /* Smooth scrolling */
    html {
      scroll-behavior: smooth;
    }

    /* Keyframes for fade-up animation */
    @keyframes fadeUp {
      0% { opacity: 0; transform: translateY(25px); }
      100% { opacity: 1; transform: translateY(0); }
    }

    .animate {
      animation: fadeUp 0.7s ease forwards;
    }

    /* ----- MOBILE-FIRST NAVIGATION ----- */
    .navbar {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 0.9rem 1.2rem;
      background: rgba(26, 47, 29, 0.92);
      backdrop-filter: blur(16px);
      -webkit-backdrop-filter: blur(16px);
      position: fixed;
      width: 100%;
      top: 0;
      z-index: 1000;
      border-bottom: 1px solid rgba(196, 164, 74, 0.35);
    }

    .logo {
      font-size: 1.7rem;
      font-weight: 700;
      color: var(--gold);
      display: flex;
      align-items: center;
      gap: 0.4rem;
    }
    .logo i {
      color: var(--gold-light);
      font-size: 1.9rem;
    }

    .nav-links {
      display: none;
      flex-direction: column;
      width: 100%;
      background: rgba(26, 47, 29, 0.96);
      backdrop-filter: blur(20px);
      position: absolute;
      top: 65px;
      left: 0;
      padding: 1.2rem 1.5rem;
      border-radius: 0 0 20px 20px;
      gap: 1rem;
    }

    .nav-links.active {
      display: flex;
    }

    .nav-links a {
      color: #f2e9cf;
      text-decoration: none;
      font-weight: 500;
      font-size: 1.1rem;
      transition: color 0.3s;
      position: relative;
      padding: 0.3rem 0;
    }

    .nav-links a:hover {
      color: var(--gold-light);
    }

    .menu-toggle {
      font-size: 1.8rem;
      color: var(--gold);
      cursor: pointer;
      background: none;
      border: none;
    }

    /* ----- HERO SECTION (mobile-first) ----- */
    .hero {
      min-height: 85vh;
      background: linear-gradient(rgba(15, 25, 15, 0.7), rgba(26, 47, 29, 0.8)), 
                  url('https://images.unsplash.com/photo-1586348943529-beaae6c28db9?q=80&w=2070&auto=format&fit=crop');
      background-size: cover;
      background-position: center 35%;
      display: flex;
      align-items: center;
      justify-content: center;
      text-align: center;
      padding: 5rem 1.2rem 2rem;
      margin-top: 65px;
      color: white;
    }

    .hero-content {
      background: rgba(255, 255, 255, 0.08);
      backdrop-filter: blur(12px);
      -webkit-backdrop-filter: blur(12px);
      border-radius: 28px;
      padding: 2rem 1.5rem;
      border: 1px solid rgba(196, 164, 74, 0.45);
      max-width: 500px;
      width: 100%;
    }

    .hero h1 {
      font-size: 2.4rem;
      font-weight: 700;
      text-shadow: 2px 2px 8px rgba(0,0,0,0.6);
      margin-bottom: 0.8rem;
    }

    .hero p {
      font-size: 1.1rem;
      margin-bottom: 1.8rem;
      color: #f3efd9;
    }

    .btn {
      background: var(--gold);
      color: #111;
      padding: 0.8rem 2rem;
      border-radius: 40px;
      font-weight: 700;
      text-decoration: none;
      display: inline-block;
      transition: all 0.3s;
      border: none;
      cursor: pointer;
      letter-spacing: 0.4px;
      box-shadow: 0 6px 16px rgba(196, 164, 74, 0.35);
      font-size: 0.95rem;
    }

    .btn:hover {
      background: #dbb44b;
      transform: translateY(-3px);
      box-shadow: 0 12px 22px rgba(196, 164, 74, 0.55);
    }

    /* ----- GENERAL SECTION STYLING ----- */
    section {
      padding: 3.5rem 1.2rem;
    }

    .section-title {
      text-align: center;
      margin-bottom: 2.5rem;
    }

    .section-title h2 {
      font-size: 2.2rem;
      color: var(--deep-green);
      position: relative;
      display: inline-block;
    }

    .section-title h2::after {
      content: '';
      width: 65px;
      height: 3px;
      background: var(--gold);
      position: absolute;
      bottom: -10px;
      left: 50%;
      transform: translateX(-50%);
    }

    /* Glass card base */
    .glass-card {
      background: rgba(255, 255, 250, 0.65);
      backdrop-filter: blur(14px);
      -webkit-backdrop-filter: blur(14px);
      border-radius: 26px;
      border: 1px solid rgba(196, 164, 74, 0.4);
      box-shadow: var(--card-shadow);
      transition: transform 0.3s, box-shadow 0.3s;
    }

    .glass-card:hover {
      transform: translateY(-6px);
      box-shadow: 0 22px 35px rgba(0,0,0,0.12);
    }

    /* ----- ABOUT SECTION (flex) ----- */
    .about-grid {
      display: flex;
      flex-direction: column;
      gap: 2rem;
      align-items: center;
    }

    .about-text {
      font-size: 1rem;
      text-align: center;
    }

    .about-image img {
      width: 100%;
      height: auto;
      border-radius: 28px;
      object-fit: cover;
      max-height: 350px;
    }

    /* ----- SERVICES & PRODUCTS GRID (mobile-first single column) ----- */
    .services-grid,
    .products-grid,
    .pricing-grid,
    .testimonial-grid {
      display: grid;
      grid-template-columns: 1fr;
      gap: 1.8rem;
      margin-top: 1.5rem;
    }

    .service-card,
    .product-card,
    .pricing-card,
    .testimonial-card {
      text-align: center;
      padding: 1.8rem 1.2rem;
    }

    .service-card i,
    .product-card i {
      font-size: 2.5rem;
      color: var(--gold);
      margin-bottom: 0.8rem;
    }

    .price {
      font-size: 2.2rem;
      font-weight: 700;
      color: var(--deep-green);
      margin: 0.8rem 0;
    }

    .pricing-card ul {
      list-style: none;
      margin: 1rem 0;
    }

    .testimonial-card img {
      width: 70px;
      height: 70px;
      border-radius: 50%;
      object-fit: cover;
      border: 3px solid var(--gold);
      margin-bottom: 0.8rem;
    }

    /* Gallery grid */
    .gallery-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
      gap: 1rem;
    }

    .gallery-grid img {
      width: 100%;
      height: 160px;
      object-fit: cover;
      border-radius: 20px;
      transition: transform 0.3s;
      border: 2px solid rgba(196,164,74,0.3);
    }

    .gallery-grid img:hover {
      transform: scale(1.02);
    }

    /* Contact form */
    .contact-form {
      max-width: 600px;
      margin: 0 auto;
      padding: 2rem 1.5rem;
    }

    .contact-form input,
    .contact-form textarea {
      width: 100%;
      padding: 0.85rem;
      margin: 0.7rem 0;
      border-radius: 20px;
      border: 1px solid #d4c9a8;
      background: rgba(255,255,250,0.85);
      font-family: 'Inter', sans-serif;
      font-size: 1rem;
    }

    /* Footer */
    footer {
      background: #0f1f12;
      color: #e0d7b9;
      padding: 2.5rem 1.2rem;
      text-align: center;
    }

    .social-links a {
      color: var(--gold-light);
      margin: 0 0.7rem;
      font-size: 1.6rem;
      transition: 0.3s;
    }

    .social-links a:hover {
      color: white;
      transform: scale(1.15);
    }

    /* ----- MEDIA QUERIES FOR LARGER SCREENS (Tablets & Desktops) ----- */
    @media (min-width: 640px) {
      .hero h1 {
        font-size: 3rem;
      }

      .services-grid,
      .products-grid,
      .testimonial-grid {
        grid-template-columns: repeat(2, 1fr);
      }

      .about-grid {
        flex-direction: row;
        text-align: left;
        gap: 2.5rem;
      }

      .about-text {
        text-align: left;
        flex: 1;
      }

      .about-image {
        flex: 1;
      }
    }

    @media (min-width: 768px) {
      .navbar {
        padding: 1rem 5%;
      }

      .menu-toggle {
        display: none;
      }

      .nav-links {
        display: flex;
        flex-direction: row;
        position: static;
        width: auto;
        background: transparent;
        backdrop-filter: none;
        padding: 0;
        gap: 2.2rem;
      }

      .nav-links a {
        font-size: 1rem;
      }

      .hero-content {
        padding: 2.8rem;
      }

      section {
        padding: 4.5rem 5%;
      }

      .pricing-grid {
        grid-template-columns: repeat(3, 1fr);
      }
    }

    @media (min-width: 1024px) {
      .hero h1 {
        font-size: 3.8rem;
      }

      .services-grid,
      .products-grid {
        grid-template-columns: repeat(3, 1fr);
      }

      .testimonial-grid {
        grid-template-columns: repeat(3, 1fr);
      }

      .gallery-grid {
        grid-template-columns: repeat(4, 1fr);
      }
    }

    /* Ensure no horizontal scroll */
    body, html {
      max-width: 100%;
      overflow-x: hidden;
    }
  </style>
</head>
<body>
  <!-- Navigation Bar -->
  <nav class="navbar">
    <div class="logo">
      <i class="fas fa-feather-alt"></i> GoldenNest
    </div>
    <button class="menu-toggle" id="menuToggle" aria-label="Menu">
      <i class="fas fa-bars"></i>
    </button>
    <div class="nav-links" id="navLinks">
      <a href="#home">Home</a>
      <a href="#about">About</a>
      <a href="#services">Services</a>
      <a href="#products">Products</a>
      <a href="#gallery">Gallery</a>
      <a href="#testimonials">Reviews</a>
      <a href="#contact">Contact</a>
    </div>
  </nav>

  <!-- Hero Section -->
  <section id="home" class="hero">
    <div class="hero-content animate">
      <h1>Fresh From The Farm</h1>
      <p>Organic eggs, healthy broilers & day-old chicks raised with care.</p>
      <a href="#products" class="btn">Explore Products</a>
    </div>
  </section>

  <!-- About Section -->
  <section id="about">
    <div class="section-title"><h2>About Our Farm</h2></div>
    <div class="about-grid">
      <div class="about-text">
        <p style="font-size: 1.1rem; margin-bottom: 1.2rem;">Golden Nest combines tradition with sustainability. Our free-range hens roam green pastures, producing eggs with deep golden yolks.</p>
        <p>With over 15 years of expertise, we deliver premium poultry while protecting the environment.</p>
      </div>
      <div class="about-image">
        <img src="https://images.unsplash.com/photo-1548550023-2bdb3c5beed7?q=80&w=1974&auto=format&fit=crop" alt="Free range chickens on farm" loading="lazy">
      </div>
    </div>
  </section>

  <!-- Services Section -->
  <section id="services" style="background: #f3f0e3;">
    <div class="section-title"><h2>Our Services</h2></div>
    <div class="services-grid">
      <div class="service-card glass-card">
        <i class="fas fa-tractor"></i>
        <h3>Farm Consulting</h3>
        <p>Expert advice on poultry setup & biosecurity.</p>
      </div>
      <div class="service-card glass-card">
        <i class="fas fa-egg"></i>
        <h3>Egg Supply</h3>
        <p>Daily fresh organic eggs for families & businesses.</p>
      </div>
      <div class="service-card glass-card">
        <i class="fas fa-drumstick-bite"></i>
        <h3>Broiler Processing</h3>
        <p>Healthy, antibiotic-free broilers dressed to order.</p>
      </div>
    </div>
  </section>

  <!-- Products Section -->
  <section id="products">
    <div class="section-title"><h2>Poultry Products</h2></div>
    <div class="products-grid">
      <div class="product-card glass-card">
        <i class="fas fa-egg"></i>
        <h3>Organic Eggs</h3>
        <p>Free-range, rich in omega-3. Available by tray.</p>
      </div>
      <div class="product-card glass-card">
        <i class="fas fa-drumstick-bite"></i>
        <h3>Broilers</h3>
        <p>Corn-fed broilers (2-3kg), vacuum packed.</p>
      </div>
      <div class="product-card glass-card">
        <i class="fas fa-kiwi-bird"></i>
        <h3>Day-Old Chicks</h3>
        <p>Vaccinated layers & broilers for your flock.</p>
      </div>
    </div>
  </section>

  <!-- Gallery Section -->
  <section id="gallery" style="background: #f9f7ef;">
    <div class="section-title"><h2>Farm Gallery</h2></div>
    <div class="gallery-grid">
      <img src="https://images.unsplash.com/photo-1598965675045-45c5e72c7d05?q=80&w=1974&auto=format&fit=crop" alt="Hen with eggs" loading="lazy">
      <img src="https://images.unsplash.com/photo-1560806887-1e4cd0b6cbd6?q=80&w=1974&auto=format&fit=crop" alt="Chicken coop" loading="lazy">
      <img src="https://images.unsplash.com/photo-1582722872445-44dc5f7e3c8f?q=80&w=1974&auto=format&fit=crop" alt="Free range chickens" loading="lazy">
      <img src="https://images.unsplash.com/photo-1548550023-2bdb3c5beed7?q=80&w=1974&auto=format&fit=crop" alt="Poultry farm landscape" loading="lazy">
    </div>
  </section>

  <!-- Testimonials Section -->
  <section id="testimonials">
    <div class="section-title"><h2>Happy Customers</h2></div>
    <div class="testimonial-grid">
      <div class="testimonial-card glass-card">
        <img src="https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?q=80&w=1974&auto=format&fit=crop&facearea=1&h=100" alt="Customer" loading="lazy">
        <p>"The eggs are incredibly fresh! Golden yolks every morning."</p>
        <h4>Michael Roberts</h4>
        <small>Local Chef</small>
      </div>
      <div class="testimonial-card glass-card">
        <img src="https://images.unsplash.com/photo-1494790108377-be9c29b29330?q=80&w=1974&auto=format&fit=crop&facearea=1&h=100" alt="Customer" loading="lazy">
        <p>"Broilers taste like real chicken. Highly recommend."</p>
        <h4>Sarah Lin</h4>
        <small>Homesteader</small>
      </div>
      <div class="testimonial-card glass-card">
        <img src="https://images.unsplash.com/photo-1500648767791-00dcc994a43e?q=80&w=1974&auto=format&fit=crop&facearea=1&h=100" alt="Customer" loading="lazy">
        <p>"Day-old chicks are healthy and strong. Great support."</p>
        <h4>David Okafor</h4>
        <small>Poultry Farmer</small>
      </div>
    </div>
  </section>

  <!-- Contact Form -->
  <section id="contact">
    <div class="section-title"><h2>Contact Us</h2></div>
    <div class="contact-form glass-card">
      <form id="contactForm">
        <input type="text" placeholder="Your Name" required>
        <input type="email" placeholder="Email Address" required>
        <textarea rows="4" placeholder="How can we help you?"></textarea>
        <button type="submit" class="btn" style="width:100%; margin-top:1rem;">Send Message</button>
      </form>
    </div>
  </section>

  <!-- Footer -->
  <footer>
    <div class="social-links">
      <a href="#" aria-label="Facebook"><i class="fab fa-facebook-f"></i></a>
      <a href="#" aria-label="Instagram"><i class="fab fa-instagram"></i></a>
      <a href="#" aria-label="Twitter"><i class="fab fa-twitter"></i></a>
      <a href="#" aria-label="YouTube"><i class="fab fa-youtube"></i></a>
    </div>
    <p style="margin-top: 1.2rem;">© 2025 Golden Nest Poultry Farm • Freshness Delivered Daily</p>
  </footer>

  <script>
    (function() {
      // Mobile menu toggle
      const menuToggle = document.getElementById('menuToggle');
      const navLinks = document.getElementById('navLinks');

      if (menuToggle && navLinks) {
        menuToggle.addEventListener('click', function(e) {
          e.stopPropagation();
          navLinks.classList.toggle('active');
        });

        // Close menu when clicking a nav link (mobile)
        document.querySelectorAll('.nav-links a').forEach(link => {
          link.addEventListener('click', () => {
            navLinks.classList.remove('active');
          });
        });

        // Close menu if clicking outside
        document.addEventListener('click', function(event) {
          if (!event.target.closest('.navbar')) {
            navLinks.classList.remove('active');
          }
        });
      }

      // Smooth scroll for any anchor with hash
      document.querySelectorAll('a[href^="#"]').forEach(anchor => {
        anchor.addEventListener('click', function(e) {
          const href = this.getAttribute('href');
          if (href === "#") return;
          const target = document.querySelector(href);
          if (target) {
            e.preventDefault();
            target.scrollIntoView({ behavior: 'smooth' });
          }
        });
      });

      // Contact form submission
      const form = document.getElementById('contactForm');
      if (form) {
        form.addEventListener('submit', function(e) {
          e.preventDefault();
          alert('Thank you for your message! We will get back to you soon.');
          form.reset();
        });
      }

      // Simple scroll reveal animation
      const revealElements = document.querySelectorAll('.glass-card, .about-image img, .hero-content');
      const observer = new IntersectionObserver((entries) => {
        entries.forEach(entry => {
          if (entry.isIntersecting) {
            entry.target.style.animation = 'fadeUp 0.7s ease forwards';
            observer.unobserve(entry.target);
          }
        });
      }, { threshold: 0.15 });

      revealElements.forEach(el => observer.observe(el));
    })();
  </script>
</body>
</html>
