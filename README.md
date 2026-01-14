<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ranger Holidays | Naughty Queen Official</title>
    <link href="https://fonts.googleapis.com/css2?family=Bangers&family=Poppins:wght@300;400;600;800&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary-red: #e60000;
            --dark-grey: #333;
            --light-bg: #ffffff;
            --section-bg: #f9f9f9;
            --gold: #ffcc00;
        }

        * { box-sizing: border-box; scroll-behavior: smooth; }

        body {
            margin: 0;
            padding: 0;
            font-family: 'Poppins', sans-serif;
            background-color: var(--light-bg);
            color: #222;
            overflow-x: hidden;
        }

        /* --- Hero Section --- */
        header {
            height: 100vh;
            background: linear-gradient(rgba(255,255,255,0.2), rgba(255,255,255,0.7)), 
                        url('https://s3.amazonaws.com/polo-content/2524327/6c3d2bc0bd304ce9938952c1cb71e8ce');
            background-size: cover;
            background-position: center;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            padding: 20px;
            position: relative;
        }

        /* Logo Positioned at Top Left Side */
        .main-logo {
            position: absolute;
            top: 25px; 
            left: 30px; /* Thirich left side-lekku matti */
            width: 140px; 
            max-width: 35%;
            height: auto;
            filter: drop-shadow(0 5px 12px rgba(0,0,0,0.2));
            z-index: 100;
        }

        /* Mobile View - Logo position */
        @media (max-width: 600px) {
            .main-logo {
                left: 20px;
                top: 20px;
                width: 100px;
            }
        }

        .hero-content h1 {
            font-family: 'Bangers', cursive;
            font-size: clamp(60px, 12vw, 120px);
            color: var(--primary-red);
            margin: 0;
            text-shadow: 2px 2px 10px rgba(0,0,0,0.1);
        }

        .sub-text {
            font-size: 18px;
            font-weight: 600;
            letter-spacing: 5px;
            color: #333;
            margin-bottom: 30px;
            text-transform: uppercase;
        }

        /* --- Stats Bar --- */
        .stats-bar {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            background: #fff;
            padding: 30px 0;
            box-shadow: 0 10px 30px rgba(0,0,0,0.05);
            text-align: center;
            position: relative;
            z-index: 10;
        }
        .stat-item h3 { color: var(--primary-red); font-size: 32px; margin: 0; }
        .stat-item p { color: #888; font-size: 11px; font-weight: 700; text-transform: uppercase; }

        /* --- Content Sections --- */
        .container {
            padding: 80px 20px;
            max-width: 1200px;
            margin: auto;
        }

        .section-title {
            text-align: center;
            font-family: 'Bangers';
            font-size: 45px;
            color: #222;
            margin-bottom: 50px;
        }

        .section-title span { color: var(--primary-red); }

        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 25px;
        }

        .feature-card {
            background: var(--section-bg);
            padding: 40px;
            border-radius: 15px;
            transition: 0.3s ease;
            border: 1px solid #eee;
        }

        .feature-card:hover { transform: translateY(-5px); box-shadow: 0 15px 30px rgba(0,0,0,0.1); }
        .feature-card h3 { color: var(--primary-red); margin-top: 0; }

        /* --- Review Section --- */
        .reviews-section {
            background-color: var(--section-bg);
            padding: 80px 0;
        }

        .review-card {
            background: white;
            padding: 30px;
            border-radius: 12px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            margin-bottom: 20px;
        }

        .stars { color: var(--gold); font-size: 18px; margin-bottom: 8px; }
        .reviewer { font-weight: 700; color: #555; display: block; margin-top: 15px; font-size: 14px; }

        /* --- Buttons --- */
        .btn {
            display: inline-block;
            background: var(--primary-red);
            color: white;
            padding: 18px 45px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 700;
            transition: 0.3s;
            box-shadow: 0 5px 20px rgba(230, 0, 0, 0.3);
        }

        .btn:hover { background: #333; transform: scale(1.05); }
        .insta-btn { background: #000; margin-top: 15px; }

        /* --- Contact --- */
        .contact-box {
            background: white;
            padding: 60px 20px;
            border-radius: 20px;
            box-shadow: 0 20px 50px rgba(0,0,0,0.1);
            text-align: center;
        }

        /* --- Footer --- */
        footer {
            padding: 40px 20px;
            text-align: center;
            background: #fff;
            color: #888;
            font-size: 13px;
            border-top: 1px solid #eee;
        }

        .airdot-credits {
            margin-top: 15px;
            font-size: 11px;
            letter-spacing: 1px;
            text-transform: uppercase;
            color: #aaa;
        }

        .airdot-credits a { color: #444; text-decoration: none; font-weight: 800; }

        /* WhatsApp Floating */
        .whatsapp-float {
            position: fixed;
            bottom: 30px;
            right: 30px;
            background: #25d366;
            width: 60px;
            height: 60px;
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            z-index: 1000;
            box-shadow: 0 10px 20px rgba(0,0,0,0.2);
        }
    </style>
</head>
<body>

    <header>
        <img src="https://s3.amazonaws.com/polo-content/2524327/c582d8efad4e420a929507c2abe0a159" alt="Ranger Group Logo" class="main-logo">
        
        <div class="hero-content">
            <h1>RANGER</h1>
            <p class="sub-text">Holidays</p>
            <a href="#booking" class="btn">Book Your Trip</a>
        </div>
    </header>

    <div class="stats-bar">
        <div class="stat-item"><h3>4.9/5</h3><p>User Rating</p></div>
        <div class="stat-item"><h3>Premium</h3><p>Sound System</p></div>
        <div class="stat-item"><h3>Luxury</h3><p>Interiors</p></div>
    </div>

    <div class="container">
        <h2 class="section-title">Ultimate <span>Travel Experience</span></h2>
        <div class="features-grid">
            <div class="feature-card">
                <h3>4000W Sound</h3>
                <p>Feel the bass with our high-end DJ sound system and synchronized RGB laser lighting.</p>
            </div>
            <div class="feature-card">
                <h3>Premium Comfort</h3>
                <p>Full push-back luxury seats with extra legroom for those long midnight travels.</p>
            </div>
            <div class="feature-card">
                <h3>Expert Crew</h3>
                <p>Professional and friendly drivers and staff to ensure your journey is safe and fun.</p>
            </div>
        </div>
    </div>

    <div class="reviews-section">
        <div class="container">
            <h2 class="section-title">What <span>Our Guests</span> Say</h2>
            <div class="review-card">
                <div class="stars">★★★★★</div>
                <p>"The best experience ever! The lights and sound in Naughty Queen made our college trip unforgettable."</p>
                <span class="reviewer">— Aflah.k., College Union</span>
            </div>
            <div class="review-card">
                <div class="stars">★★★★★</div>
                <p>"Very clean and well-maintained bus. The staff was very helpful throughout the journey."</p>
                <span class="reviewer">— Shamlal</span>
            </div>
        </div>
    </div>

    <div class="container" id="booking">
        <div class="contact-box">
            <h2 class="section-title">Ready to <span>Rent?</span></h2>
            <p style="margin-bottom: 30px; color: #666;">Contact us now to get the best seasonal packages and offers.</p>
            
            <div style="display: flex; flex-direction: column; align-items: center; gap: 15px;">
                <a href="tel:9605055006" class="btn">📞 Call: 9605055006</a>
                <a href="tel:9633715469" class="btn">📞 Call: 9633715469</a>
                <a href="https://instagram.com/ranger_holidays_" target="_blank" class="btn insta-btn">Follow on Instagram</a>
            </div>
        </div>
    </div>

    <footer>
        <p>&copy; Ranger Holidays Official. <br> Experience the Naughty Queen Vibe.</p>
        <div class="airdot-credits">
            Designed by <a href="https://instagram.com/airdot_design" target="_blank">AIRDOT_DESIGN</a> | 📞 8714559096
        </div>
    </footer>

    <a href="https://wa.me/919605055006?text=Hi%20Ranger%20Holidays,%20I%20want%20to%20know%20more%20about%20booking%20bus" class="whatsapp-float" target="_blank">
        <img src="https://upload.wikimedia.org/wikipedia/commons/6/6b/WhatsApp.svg" width="35" alt="WhatsApp">
    </a>

</body>
</html>
