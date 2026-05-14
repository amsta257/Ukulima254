# Ukulima254
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=yes, viewport-fit=cover">
  <title>Golden Nest • Premium Poultry Farm</title>
  <!-- Google Fonts & Font Awesome for modern icons -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,400;14..32,500;14..32,600;14..32,700&family=Playfair+Display:ital,wght@0,500;0,600;0,700;1,500&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Inter', sans-serif;
      background: #f5f3e9;
      color: #2d3a1f;
      line-height: 1.5;
      scroll-behavior: smooth;
    }

    h1, h2, h3, .serif {
      font-family: 'Playfair Display', serif;
    }

    /* Color palette: dark green #1e3b2f, gold #c7a44d, soft cream */
    :root {
      --deep-green: #1e3b2f;
      --green-dark: #0f2a1f;
      --gold: #c7a44d;
      --gold-light: #e1c97b;
      --cream: #fdfaf3;
      --soft-white: #ffffff;
      --glass-bg: rgba(255, 255, 255, 0.25);
      --glass-border: rgba(255, 255, 255, 0.4);
      --shadow: 0 20px 35px rgba(0, 0, 0, 0.08);
    }

    /* Smooth animations */
    @keyframes fadeUp {
      0% { opacity: 0; transform: translateY(30px); }
      100% { opacity: 1; transform: translateY(0); }
    }

    .animate-on-scroll {
      animation: fadeUp 0.8s ease-out forwards;
    }

    /* Navigation */
    .navbar {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 1rem 5%;
      background: rgba(30, 59, 47, 0.9);
      backdrop-filter: blur(12px);
      -webkit-backdrop-filter: blur(12px);
      position: fixed;
      width: 100%;
      top: 0;
      z-index: 1000;
      border-bottom: 1px solid rgba(199, 164, 77, 0.3);
      flex-wrap: wrap;
    }

    .logo {
      font-size: 1.8rem;
      font-weight: 700;
      color: var(--gold);
      letter-spacing: 1px;
      display: flex;
      align-items: center;
      gap: 0.5rem;
    }
    .logo i {
      font-size: 2rem;
      color: var(--gold-light);
    }

    .nav-links {
      display: flex;
      gap: 2.2rem;
      align-items: center;
    }
    .nav-links a {
      color: #f0ead0;
      text-decoration: none;
      font-weight: 500;
      transition: 0.3s;
      position: relative;
      font-size: 1rem;
    }
    .nav-links a::after {
      content: '';
      position: absolute;
      bottom: -5px;
      left: 0;
      width: 0%;
      height: 2px;
      background: var(--gold);
      transition: 0.3s;
    }
    .nav-links a:hover {
      color: var(--gold-light);
    }
    .nav-links a:hover::after {
      width: 100%;
    }

    .menu-toggle {
      display: none;
      font-size: 1.8rem;
      color: var(--gold);
      cursor: pointer;
    }

    /* Hero section */
    .hero {
      min-height: 90vh;
      background: linear-gradient(rgba(15, 42, 31, 0.7), rgba(30, 59, 47, 0.75)), 
                  url('https://images.unsplash.com/photo-1586348943529-beaae6c28db9?q=80&w=2070&auto=format&fit=crop');
      background-size: cover;
      background-position: center 30%;
      display: flex;
      align-items: center;
      justify-content: center;
      text-align: center;
      padding: 0 2rem;
      margin-top: 70px;
      color: white;
    }
    .hero-content {
      max-width: 800px;
      background: rgba(255, 255, 255, 0.08);
      backdrop-filter: blur(10px);
      -webkit-backdrop-filter: blur(10px);
      border-radius: 30px;
      padding: 2.5rem;
      border: 1px solid rgba(199, 164, 77, 0.35);
      box-shadow: 0 25px 45px rgba(0,0,0,0.2);
    }
    .hero h1 {
      font-size: 3.5rem;
      font-weight: 700;
      color: #fff;
      text-shadow: 2px 2px 10px rgba(0,0,0,0.5);
      margin-bottom: 1rem;
    }
    .hero p {
      font-size: 1.3rem;
      margin-bottom: 2rem;
      color: #f3efd9;
    }
    .btn {
      background: var(--gold);
      color: var(--deep-green);
      padding: 0.85rem 2.2rem;
      border-radius: 50px;
      font-weight: 700;
      text-decoration: none;
      display: inline-block;
      transition: 0.3s;
      border: none;
      cursor: pointer;
      letter-spacing: 0.5px;
      box-shadow: 0 8px 18px rgba(199, 164, 77, 0.4);
    }
    .btn:hover {
      background: #e1c97b;
      transform: translateY(-3px);
      box-shadow: 0 14px 22px rgba(199, 164, 77, 0.6);
    }

    /* Section styling */
    section {
      padding: 5rem 5%;
    }
    .section-title {
      text-align: center;
      margin-bottom: 3rem;
    }
    .section-title h2 {
      font-size: 2.7rem;
      color: var(--deep-green);
      position: relative;
      display: inline-block;
    }
    .section-title h2::after {
      content: '';
      width: 70px;
      height: 4px;
      background: var(--gold);
      position: absolute;
      bottom: -12px;
      left: 50%;
      transform: translateX(-50%);
    }

    /* Glass cards */
    .glass-card {
      background: var(--glass-bg);
      backdrop-filter: blur(14px);
      -webkit-backdrop-filter: blur(14px);
      border-radius: 24px;
      border: 1px solid var(--glass-border);
      box-shadow: var(--shadow);
      transition: transform 0.3s ease, box-shadow 0.3s;
    }
    .glass-card:hover {
      transform: translateY(-8px);
      box-shadow: 0 28px 40px rgba(0, 0, 0, 0.15);
    }

    /* About + Services grid */
    .about-grid {
      display: flex;
      flex-wrap: wrap;
      gap: 3rem;
      align-items: center;
    }
    .about-text {
      flex: 1 1 400px;
    }
    .about-image {
      flex: 1 1 400px;
      border-radius: 28px;
      overflow: hidden;
    }
    .about-image img {
      width: 100%;
      height: auto;
      display: block;
      border-radius: 28px;
    }

    .services-grid, .products-grid, .pricing-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 2rem;
      margin-top: 2rem;
    }
    .service-card, .product-card, .pricing-card {
      padding: 2rem 1.5rem;
      text-align: center;
      background: rgba(255, 255, 255, 0.7);
      backdrop-filter: blur(10px);
      border-radius: 28px;
      border: 1px solid rgba(199, 164, 77, 0.4);
    }
    .service-card i, .product-card i {
      font-size: 2.8rem;
      color: var(--gold);
      margin-bottom: 1rem;
    }
    .price {
      font-size: 2.5rem;
      font-weight: 700;
      color: var(--deep-green);
      margin: 1rem 0;
    }
    .pricing-card ul {
      list-style: none;
      margin: 1.2rem 0;
    }
    .pricing-card li {
      margin: 0.5rem 0;
    }

    /* Testimonials */
    .testimonial-card {
      background: rgba(255,255,240,0.8);
      backdrop-filter: blur(12px);
      padding: 2rem;
      border-radius: 30px;
      text-align: center;
    }
    .testimonial-card img {
      width: 70px;
      height: 70px;
      border-radius: 50%;
      object-fit: cover;
      border: 3px solid var(--gold);
      margin-bottom: 1rem;
    }

    /* Contact form */
    .contact-form {
      max-width: 650px;
      margin: 0 auto;
      background: rgba(255, 255, 250, 0.75);
      backdrop-filter: blur(16px);
      padding: 2.5rem;
      border-radius: 32px;
      border: 1px solid rgba(199,164,77,0.5);
    }
    .contact-form input, .contact-form textarea {
      width: 100%;
      padding: 0.9rem;
      margin: 0.8rem 0;
      border-radius: 20px;
      border: 1px solid #ccc;
      background: rgba(255,255,255,0.8);
      font-family: 'Inter', sans-serif;
    }

    footer {
      background: var(--deep-green);
      color: #e9e2c7;
      padding: 2.5rem 5%;
      text-align: center;
    }
    .social-links a {
      color: var(--gold-light);
      margin: 0 0.8rem;
      font-size: 1.6rem;
      transition: 0.3s;
    }
    .social-links a:hover {
      color: white;
      transform: scale(1.2);
    }

    @media (max-width: 768px) {
      .nav-links {
        display: none;
        flex-direction: column;
        width: 100%;
        background: rgba(30, 59, 47, 0.95);
        margin-top: 1rem;
        padding: 1rem 0;
        border-radius: 16px;
      }
      .nav-links.active {
        display: flex;
      }
      .menu-toggle {
        display: block;
      }
      .hero h1 {
        font-size: 2.5rem;
      }
    }
  </style>
</head>
<body>
  <nav class="navbar">
    <div class="logo">
      <i class="fas fa-feather-alt"></i> GoldenNest
    </div>
    <div class="menu-toggle" id="menuToggle">
      <i class="fas fa-bars"></i>
    </div>
    <div class="nav-links" id="navLinks">
      <a href="#home">Home</a>
      <a href="#about">About</a>
      <a href="#services">Services</a>
      <a href="#products">Products</a>
      <a href="#pricing">Pricing</a>
      <a href="#testimonials">Reviews</a>
      <a href="#contact">Contact</a>
    </div>
  </nav>

  <!-- Hero -->
  <section id="home" class="hero">
    <div class="hero-content">
      <h1>Fresh From The Farm</h1>
      <p>Organic eggs, healthy broilers & day-old chicks raised with care.</p>
      <a href="#products" class="btn">Explore Products</a>
    </div>
  </section>

  <!-- About Us -->
  <section id="about">
    <div class="section-title"><h2>About Golden Nest</h2></div>
    <div class="about-grid">
      <div class="about-text">
        <p style="font-size: 1.2rem; margin-bottom: 1.5rem;">Nestled in rolling green pastures, we combine traditional farming with modern sustainability. Our free-range hens enjoy sunlight and space, producing rich golden yolks.</p>
        <p>With over 15 years of experience, we deliver premium poultry while protecting the land. Every chick, egg, and broiler reflects our passion for quality.</p>
      </div>
      <div class="about-image">
        <img src="https://images.unsplash.com/photo-1548550023-2bdb3c5beed7?q=80&w=1974&auto=format&fit=crop" alt="Free range chickens on green farm">
      </div>
    </div>
  </section>

  <!-- Services -->
  <section id="services" style="background: #eef3e0;">
    <div class="section-title"><h2>Our Services</h2></div>
    <div class="services-grid">
      <div class="service-card glass-card">
        <i class="fas fa-tractor"></i>
        <h3>Farm Consulting</h3>
        <p>Expert advice on poultry setup, biosecurity & feed management.</p>
      </div>
      <div class="service-card glass-card">
        <i class="fas fa-egg"></i>
        <h3>Egg Supply</h3>
        <p>Daily fresh organic eggs for households & businesses.</p>
      </div>
      <div class="service-card glass-card">
        <i class="fas fa-drumstick-bite"></i>
        <h3>Broiler Processing</h3>
        <p>Healthy, antibiotic-free broilers dressed to order.</p>
      </div>
    </div>
  </section>

  <!-- Products -->
  <section id="products">
    <div class="section-title"><h2>Poultry Products</h2></div>
    <div class="products-grid">
      <div class="product-card glass-card">
        <i class="fas fa-egg"></i>
        <h3>Organic Eggs</h3>
        <p>Free-range, rich in omega-3. Available by crate or tray.</p>
      </div>
      <div class="product-card glass-card">
        <i class="fas fa-drumstick-bite"></i>
        <h3>Broilers</h3>
        <p>Corn-fed broilers (2-3kg), vacuum packed fresh.</p>
      </div>
      <div class="product-card glass-card">
        <i class="fas fa-kiwi-bird"></i>
        <h3>Day-Old Chicks</h3>
        <p>Vaccinated layers & broilers, perfect for starting your flock.</p>
      </div>
    </div>
  </section>

  <!-- Pricing Cards -->
  <section id="pricing" style="background: #faf7ed;">
    <div class="section-title"><h2>Transparent Pricing</h2></div>
    <div class="pricing-grid">
      <div class="pricing-card glass-card">
        <h3>Egg Basket</h3>
        <div class="price">$8<span>/tray</span></div>
        <ul>
          <li>30 fresh eggs</li>
          <li>Free-range certified</li>
          <li>Weekly delivery</li>
        </ul>
        <a href="#" class="btn">Order</a>
      </div>
      <div class="pricing-card glass-card">
        <h3>Broiler Pack</h3>
        <div class="price">$14<span>/bird</span></div>
        <ul>
          <li>2.5 kg average</li>
          <li>Dressed & clean</li>
          <li>5 birds minimum</li>
        </ul>
        <a href="#" class="btn">Order</a>
      </div>
      <div class="pricing-card glass-card">
        <h3>Chick Starter</h3>
        <div class="price">$3<span>/chick</span></div>
        <ul>
          <li>Vaccinated</li>
          <li>Hybrid layers</li>
          <li>Bulk discount</li>
        </ul>
        <a href="#" class="btn">Inquire</a>
      </div>
    </div>
  </section>

  <!-- Testimonials -->
  <section id="testimonials">
    <div class="section-title"><h2>From Our Customers</h2></div>
    <div class="services-grid">
      <div class="testimonial-card glass-card">
        <img src="https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?q=80&w=1974&auto=format&fit=crop&facearea=1&h=100" alt="Customer">
        <p>"The eggs are incredibly fresh! Golden yolks every morning."</p>
        <h4>Michael Roberts</h4>
        <small>Local Chef</small>
      </div>
      <div class="testimonial-card glass-card">
        <img src="https://images.unsplash.com/photo-1494790108377-be9c29b29330?q=80&w=1974&auto=format&fit=crop&facearea=1&h=100" alt="Customer">
        <p>"Broilers taste like real chicken, not factory farmed. Highly recommend."</p>
        <h4>Sarah Lin</h4>
        <small>Homesteader</small>
      </div>
      <div class="testimonial-card glass-card">
        <img src="https://images.unsplash.com/photo-1500648767791-00dcc994a43e?q=80&w=1974&auto=format&fit=crop&facearea=1&h=100" alt="Customer">
        <p>"Day-old chicks are healthy and strong. Great support from the farm."</p>
        <h4>David Okafor</h4>
        <small>Poultry Farmer</small>
      </div>
    </div>
  </section>

  <!-- Contact Form -->
  <section id="contact">
    <div class="section-title"><h2>Get In Touch</h2></div>
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
      <a href="#"><i class="fab fa-facebook-f"></i></a>
      <a href="#"><i class="fab fa-instagram"></i></a>
      <a href="#"><i class="fab fa-twitter"></i></a>
      <a href="#"><i class="fab fa-youtube"></i></a>
    </div>
    <p style="margin-top: 1.2rem;">© 2025 Golden Nest Poultry Farm • Freshness Delivered Daily</p>
  </footer>

  <script>
    // Mobile menu toggle
    const menuToggle = document.getElementById('menuToggle');
    const navLinks = document.getElementById('navLinks');
    menuToggle.addEventListener('click', () => {
      navLinks.classList.toggle('active');
    });

    // Smooth scroll for anchor links & close mobile menu
    document.querySelectorAll('.nav-links a').forEach(link => {
      link.addEventListener('click', (e) => {
        e.preventDefault();
        const targetId = link.getAttribute('href').substring(1);
        const targetSection = document.getElementById(targetId);
        if (targetSection) {
          targetSection.scrollIntoView({ behavior: 'smooth' });
          navLinks.classList.remove('active');
        }
      });
    });

    // Simple form submission prevention & feedback
    const form = document.getElementById('contactForm');
    form.addEventListener('submit', function(e) {
      e.preventDefault();
      alert('Thank you for your message! We will get back to you soon.');
      form.reset();
    });

    // Add subtle animation on scroll (basic intersection observer)
    const animatedElements = document.querySelectorAll('.glass-card, .about-image, .hero-content');
    const observer = new IntersectionObserver((entries) => {
      entries.forEach(entry => {
        if (entry.isIntersecting) {
          entry.target.style.animation = 'fadeUp 0.7s ease forwards';
        }
      });
    }, { threshold: 0.2 });

    animatedElements.forEach(el => observer.observe(el));
  </script>
</body>
</html>
