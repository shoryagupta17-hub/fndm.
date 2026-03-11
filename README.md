!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>FNDM - Customized Memories & Creative Gifts</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    
    <style>
        :root {
            --primary: #d4a5a5;
            --secondary: #f5f5dc;
            --accent: #ffb7b2;
            --text: #4a4a4a;
            --white: #ffffff;
            --green: #25D366;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: var(--secondary);
            color: var(--text);
            line-height: 1.6;
        }
        
        /* Header */
        header {
            background: linear-gradient(135deg, var(--primary), var(--accent));
            color: var(--white);
            padding: 60px 20px;
            text-align: center;
        }
        
        .logo {
            font-size: 3.5rem;
            font-weight: bold;
            margin-bottom: 10px;
        }
        
        .tagline {
            font-size: 1.2rem;
            margin-bottom: 20px;
            font-style: italic;
        }
        
        .owner-info {
            font-size: 0.9rem;
            opacity: 0.9;
        }
        
        /* Navigation */
        nav {
            background: #333;
            padding: 15px;
            position: sticky;
            top: 0;
            z-index: 100;
        }
        
        nav a {
            color: var(--white);
            margin: 0 15px;
            text-decoration: none;
            font-size: 16px;
            transition: color 0.3s;
        }
        
        nav a:hover {
            color: var(--primary);
        }
        
        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(212, 165, 165, 0.8), rgba(212, 165, 165, 0.8)), 
                        url('hero-bg.jpg');
            background-size: cover;
            padding: 80px 20px;
            text-align: center;
            color: var(--white);
        }
        
        .hero h2 {
            font-size: 2.5rem;
            margin-bottom: 20px;
        }
        
        .hero p {
            font-size: 1.2rem;
            margin-bottom: 30px;
        }
        
        .cta-button {
            background: var(--white);
            color: var(--primary);
            padding: 15px 40px;
            border: none;
            border-radius: 50px;
            font-size: 1.1rem;
            cursor: pointer;
            text-decoration: none;
            display: inline-block;
            font-weight: bold;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
        }
        
        /* Sections */
        section {
            padding: 60px 20px;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        h2 {
            text-align: center;
            color: var(--primary);
            font-size: 2.5rem;
            margin-bottom: 40px;
        }
        
        /* Products Grid */
        .products {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 30px;
            padding: 20px;
        }
        
        .card {
            background: var(--white);
            padding: 25px;
            border-radius: 15px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            text-align: center;
            transition: transform 0.3s;
        }
        
        .card:hover {
            transform: translateY(-10px);
        }
        
        .product-img {
            width: 100%;
            height: 200px;
            object-fit: cover;
            border-radius: 10px;
            margin-bottom: 15px;
        }
        
        .card h3 {
            color: var(--primary);
            margin-bottom: 10px;
        }
        
        .price {
            font-size: 1.3rem;
            color: var(--text);
            font-weight: bold;
            margin: 10px 0;
        }
        
        .order-btn {
            background: var(--green);
            color: white;
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            margin-top: 10px;
            text-decoration: none;
            display: inline-block;
        }
        
        /* Price List */
        .price-list {
            background: var(--white);
            padding: 30px;
            border-radius: 15px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            max-width: 800px;
            margin: 0 auto;
        }
        
        .price-item {
            display: flex;
            justify-content: space-between;
            padding: 15px 0;
            border-bottom: 1px dashed #ddd;
        }
        
        .price-item:last-child {
            border-bottom: none;
        }
        
        .price-item span:first-child {
            font-weight: 500;
        }
        
        .price-item span:last-child {
            color: var(--primary);
            font-weight: bold;
        }
        
        /* Customization Section */
        .customization {
            background: var(--white);
            padding: 40px;
            border-radius: 15px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        
        .upload-form {
            max-width: 600px;
            margin: 0 auto;
        }
        
        .upload-form input,
        .upload-form textarea {
            width: 100%;
            padding: 15px;
            margin: 10px 0;
            border: 2px solid #ddd;
            border-radius: 5px;
            font-size: 1rem;
        }
        
        .upload-form button {
            background: var(--primary);
            color: white;
            padding: 15px 40px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-size: 1.1rem;
            width: 100%;
        }
        
        /* Gallery */
        .gallery {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
        }
        
        .gallery img {
            width: 100%;
            height: 250px;
            object-fit: cover;
            border-radius: 10px;
            box-shadow: 0 3px 10px rgba(0,0,0,0.1);
            transition: transform 0.3s;
        }
        
        .gallery img:hover {
            transform: scale(1.05);
        }
        
        /* Contact Section */
        .contact-box {
            background: var(--white);
            padding: 40px;
            border-radius: 15px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            text-align: center;
        }
        
        .contact-info {
            font-size: 1.3rem;
            margin: 20px 0;
        }
        
        .whatsapp-btn {
            background: var(--green);
            color: white;
            padding: 15px 40px;
            border: none;
            border-radius: 50px;
            font-size: 1.2rem;
            cursor: pointer;
            text-decoration: none;
            display: inline-block;
            margin-top: 20px;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
        }
        
        .whatsapp-btn:hover {
            background: #128C7E;
        }
        
        /* Footer */
        footer {
            background: #333;
            color: var(--white);
            text-align: center;
            padding: 30px;
            margin-top: 50px;
        }
        
        /* Mobile Responsive */
        @media (max-width: 768px) {
            .logo { font-size: 2.5rem; }
            .hero h2 { font-size: 1.8rem; }
            nav a { display: block; margin: 10px 0; }
            .products { grid-template-columns: 1fr; }
            .price-item { flex-direction: column; text-align: center; }
        }
    </style>
</head>

<body>

<!-- Header -->
<header>
    <div class="logo">FNDM</div>
    <div class="tagline">Customized Memories & Creative Gifts</div>
    <div class="owner-info">
        <p>Owner: Pukhraj Anand</p>
        <p>📞 9012977666</p>
    </div>
</header>

<!-- Navigation -->
<nav>
    <a href="#home">Home</a>
    <a href="#products">Products</a>
    <a href="#prices">Price List</a>
    <a href="#customization">Customize</a>
    <a href="#gallery">Gallery</a>
    <a href="#contact">Contact</a>
</nav>

<!-- Hero Section -->
<section id="home" class="hero">
    <h2>Turn Your Memories Into Beautiful Gifts</h2>
    <p>Handmade, Customized & Made With Love</p>
    <a href="#products" class="cta-button">Explore Products</a>
</section>

<!-- Products Section -->
<section id="products">
    <h2>✨ Our Products</h2>
    
    <div class="products">
        
        <div class="card">
            <img src="6.jfif" alt="Snap Art" class="product-img">
            <h3>Snap Art</h3>
            <p>Custom aesthetic snap art</p>
            <div class="price">From ₹50</div>
            <a href="#contact" class="order-btn">Order Now</a>
        </div>
        
        <div class="card">
            <img src="3.jfif" alt="Photo Frames" class="product-img">
            <h3>Photo Frames</h3>
            <p>Handmade decorative frames</p>
            <div class="price">From ₹250</div>
            <a href="#contact" class="order-btn">Order Now</a>
        </div>
        
        <div class="card">
            <img src="2.jfif" alt="Wool Roses" class="product-img">
            <h3>Wool Roses</h3>
            <p>Handmade wool flowers</p>
            <div class="price">Custom Pricing</div>
            <a href="#contact" class="order-btn">Order Now</a>
        </div>
        
        <div class="card">
            <img src="4.jfif" alt="Travel Books" class="product-img">
            <h3>Travel Books</h3>
            <p>Creative travel journals</p>
            <div class="price">₹100</div>
            <a href="#contact" class="order-btn">Order Now</a>
        </div>
        
        <div class="card">
            <img src="8.jpg" alt="Decorative Tapes" class="product-img">
            <h3>Decorative Tapes</h3>
            <p>Colorful aesthetic tapes</p>
            <div class="price">₹10 each</div>
            <a href="#contact" class="order-btn">Order Now</a>
        </div>
        
        <div class="card">
            <img src="7.jfif" alt="Polaroids" class="product-img">
            <h3>Polaroids</h3>
            <p>Mini printed photo memories</p>
            <div class="price">₹100 (10 pcs)</div>
            <a href="#contact" class="order-btn">Order Now</a>
        </div>
        
    </div>
</section>

<!-- Price List Section -->
<section id="prices">
    <h2>💰 Complete Price List</h2>
    
    <div class="price-list">
        <h3 style="text-align: center; margin-bottom: 20px; color: var(--primary);">📸 Snap Arts</h3>
        <div class="price-item"><span>Small Snap Art</span> <span>₹50</span></div>
        <div class="price-item"><span>Big Snap Art</span> <span>₹75</span></div>
        <div class="price-item"><span>Stand</span> <span>₹50</span></div>
        
        <h3 style="text-align: center; margin: 30px 0 20px; color: var(--primary);">🖼️ Photo Frames</h3>
        <div class="price-item"><span>Small Frame</span> <span>₹250</span></div>
        <div class="price-item"><span>Medium Frame</span> <span>₹350</span></div>
        <div class="price-item"><span>Large Frame</span> <span>₹500</span></div>
        
        <h3 style="text-align: center; margin: 30px 0 20px; color: var(--primary);">📔 Travel Memory Books</h3>
        <div class="price-item"><span>Travel Book</span> <span>₹100</span></div>
        <div class="price-item"><span>Decorative Tape</span> <span>₹10 per tape</span></div>
        
        <h3 style="text-align: center; margin: 30px 0 20px; color: var(--primary);">📷 Polaroids</h3>
        <div class="price-item"><span>10 Polaroids</span> <span>₹100</span></div>
        <div class="price-item"><span>18 Small Polaroids</span> <span>₹100</span></div>
        
        <h3 style="text-align: center; margin: 30px 0 20px; color: var(--primary);">🌹 Other Products</h3>
        <div class="price-item"><span>Wool Rose Bouquets</span> <span>Custom Pricing</span></div>
        <div class="price-item"><span>Enamel Stickers</span> <span>Custom Pricing</span></div>
    </div>
</section>

<!-- Customization Section -->
<section id="customization">
    <h2>🎨 Customize Your Gift</h2>
    
    <div class="customization">
        <p style="text-align: center; margin-bottom: 30px;">Upload your photos for snap arts, polaroids, and frames!</p>
        
        <form class="upload-form" action="https://wa# fndm.
