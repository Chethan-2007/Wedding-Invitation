# Wedding-Invitation
<html lang="en"><head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pavan &amp; Roopa - Sacred Union</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin="">
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;500;600;700&amp;family=Montserrat:wght@300;400;500;600&amp;family=Sacramento&amp;family=Noto+Sans+Devanagari:wght@400;500&amp;display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --deep-purple: #2D033B;
            --royal-purple: #6A0DAD;
            --amethyst: #9B59B6;
            --lavender: #E6E6FA;
            --gold: #FFD700;
            --light-gold: #FFF8DC;
            --dark-bg: #0A0014;
            --eco-green: #2E8B57;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Montserrat', sans-serif;
            line-height: 1.7;
            color: var(--lavender);
            background-color: var(--dark-bg);
            background-image: 
                radial-gradient(circle at 20% 30%, rgba(106, 13, 173, 0.1) 0%, transparent 50%),
                radial-gradient(circle at 80% 70%, rgba(45, 3, 59, 0.15) 0%, transparent 50%);
            position: relative;
            overflow-x: hidden;
        }
        
        /* Animated background elements */
        .floating-element {
            position: fixed;
            background: radial-gradient(circle, var(--royal-purple) 0%, transparent 70%);
            border-radius: 50%;
            opacity: 0.1;
            z-index: -1;
            animation: float 20s infinite ease-in-out;
        }
        
        .floating-element:nth-child(1) {
            width: 300px;
            height: 300px;
            top: 10%;
            left: 5%;
            animation-delay: 0s;
        }
        
        .floating-element:nth-child(2) {
            width: 200px;
            height: 200px;
            bottom: 20%;
            right: 10%;
            animation-delay: 5s;
        }
        
        @keyframes float {
            0%, 100% { transform: translateY(0) rotate(0deg); }
            50% { transform: translateY(-20px) rotate(180deg); }
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Header Styles */
        header {
            background: linear-gradient(135deg, var(--deep-purple) 0%, #1A001F 100%);
            padding: 40px 0 30px;
            text-align: center;
            position: relative;
            border-bottom: 3px solid var(--gold);
            box-shadow: 0 10px 30px rgba(0,0,0,0.5);
            overflow: hidden;
        }
        
        header::before {
            content: '🪷';
            position: absolute;
            top: 20px;
            left: 30px;
            font-size: 28px;
            color: var(--gold);
            opacity: 0.7;
        }
        
        header::after {
            content: '🌸';
            position: absolute;
            bottom: 20px;
            right: 30px;
            font-size: 28px;
            color: var(--amethyst);
            opacity: 0.7;
        }
        
        .header-content {
            position: relative;
            z-index: 2;
        }
        
        h1 {
            font-family: 'Playfair Display', serif;
            font-size: 4rem;
            margin-bottom: 15px;
            background: linear-gradient(45deg, var(--lavender), var(--gold));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            text-shadow: 0 5px 15px rgba(0,0,0,0.3);
        }
        
        .sanskrit-title {
            font-family: 'Noto Sans Devanagari', sans-serif;
            font-size: 1.8rem;
            color: var(--amethyst);
            margin-bottom: 25px;
            letter-spacing: 2px;
        }
        
        .subtitle {
            font-size: 1.3rem;
            font-weight: 300;
            letter-spacing: 3px;
            margin-bottom: 25px;
            color: var(--lavender);
        }
        
        .hashtags {
            display: flex;
            justify-content: center;
            gap: 25px;
            margin-top: 20px;
            flex-wrap: wrap;
        }
        
        .hashtag {
            background: linear-gradient(45deg, var(--royal-purple), var(--amethyst));
            padding: 10px 20px;
            border-radius: 30px;
            font-weight: 600;
            box-shadow: 0 4px 15px rgba(155, 89, 182, 0.3);
            transition: transform 0.3s ease;
        }
        
        .hashtag:hover {
            transform: translateY(-3px);
        }
        
        /* Couple Section */
        .couple-section {
            padding: 100px 0 80px;
            text-align: center;
            position: relative;
        }
        
        .couple-section::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('https://images.unsplash.com/photo-1596461404969-9ae70f2830c1?q=80&w=2070&auto=format&fit=crop') center/cover;
            opacity: 0.07;
            z-index: -1;
        }
        
        .couple-names {
            display: flex;
            justify-content: center;
            align-items: center;
            margin-bottom: 80px;
            flex-wrap: wrap;
            gap: 50px;
        }
        
        .bride, .groom {
            flex: 1;
            min-width: 300px;
            padding: 40px 30px;
            position: relative;
            background: rgba(45, 3, 59, 0.6);
            border-radius: 20px;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(155, 89, 182, 0.3);
            box-shadow: 0 15px 35px rgba(0,0,0,0.5);
            transition: transform 0.5s ease;
        }
        
        .bride:hover, .groom:hover {
            transform: translateY(-10px);
            border-color: var(--gold);
        }
        
        .bride {
            border-left: 5px solid var(--gold);
        }
        
        .groom {
            border-right: 5px solid var(--gold);
        }
        
        .name {
            font-family: 'Playfair Display', serif;
            font-size: 3rem;
            background: linear-gradient(to right, var(--gold), var(--lavender));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            margin-bottom: 15px;
        }
        
        .groom .name {
            background: linear-gradient(to right, var(--gold), var(--lavender));
            -webkit-background-clip: text;
            background-clip: text;
        }
        
        .ampersand {
            font-family: 'Sacramento', cursive;
            font-size: 5rem;
            color: var(--gold);
            margin: 0 20px;
            text-shadow: 0 0 20px rgba(255, 215, 0, 0.5);
        }
        
        .parents {
            margin-top: 20px;
            font-size: 1.2rem;
            color: #C9B6E4;
            line-height: 1.8;
        }
        
        /* Quote Section */
        .scripture-quote {
            background: rgba(45, 3, 59, 0.8);
            padding: 50px;
            border-radius: 15px;
            margin: 50px auto;
            max-width: 900px;
            border-left: 5px solid var(--gold);
            position: relative;
            overflow: hidden;
        }
        
        .scripture-quote::before {
            content: '"';
            position: absolute;
            top: -30px;
            left: 20px;
            font-size: 120px;
            font-family: 'Playfair Display', serif;
            color: var(--royal-purple);
            opacity: 0.3;
        }
        
        .quote-text {
            font-size: 1.8rem;
            font-style: italic;
            text-align: center;
            margin-bottom: 20px;
            color: var(--light-gold);
            line-height: 1.6;
        }
        
        .quote-source {
            text-align: right;
            color: var(--amethyst);
            font-size: 1.1rem;
        }
        
        /* Events Section */
        .events-section {
            padding: 80px 0;
            position: relative;
        }
        
        .section-title {
            font-family: 'Playfair Display', serif;
            font-size: 3rem;
            text-align: center;
            color: var(--lavender);
            margin-bottom: 70px;
            position: relative;
            display: inline-block;
            left: 50%;
            transform: translateX(-50%);
        }
        
        .section-title::after {
            content: '';
            display: block;
            width: 150px;
            height: 4px;
            background: linear-gradient(to right, var(--amethyst), var(--gold));
            margin: 15px auto 0;
            border-radius: 2px;
        }
        
        .events-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 40px;
            margin-top: 50px;
        }
        
        .event-card {
            background: linear-gradient(145deg, rgba(45, 3, 59, 0.8), rgba(26, 0, 31, 0.9));
            border-radius: 20px;
            padding: 40px;
            box-shadow: 0 20px 40px rgba(0,0,0,0.4);
            transition: all 0.4s ease;
            border: 1px solid rgba(155, 89, 182, 0.2);
            position: relative;
            overflow: hidden;
        }
        
        .event-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 5px;
            height: 100%;
            background: linear-gradient(to bottom, var(--amethyst), var(--gold));
        }
        
        .event-card:hover {
            transform: translateY(-15px);
            box-shadow: 0 30px 50px rgba(0,0,0,0.5);
            border-color: var(--gold);
        }
        
        .event-title {
            font-family: 'Playfair Display', serif;
            font-size: 2.2rem;
            background: linear-gradient(45deg, var(--lavender), var(--gold));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            margin-bottom: 20px;
        }
        
        .event-subtitle {
            font-style: italic;
            color: #C9B6E4;
            margin-bottom: 30px;
            font-size: 1.1rem;
        }
        
        .event-details {
            margin-bottom: 20px;
        }
        
        .detail-item {
            display: flex;
            margin-bottom: 15px;
            align-items: center;
        }
        
        .detail-icon {
            color: var(--gold);
            margin-right: 15px;
            width: 25px;
            font-size: 1.2rem;
        }
        
        .muhurtha-highlight {
            background: linear-gradient(45deg, var(--royal-purple), transparent);
            padding: 15px;
            border-radius: 10px;
            margin-top: 20px;
            border: 1px solid var(--gold);
        }
        
        /* Sustainable Wedding Section */
        .sustainable-section {
            padding: 80px 0;
            background: rgba(26, 0, 31, 0.7);
            margin: 60px 0;
            position: relative;
            border-top: 2px solid var(--eco-green);
            border-bottom: 2px solid var(--eco-green);
        }
        
        .sustainable-section::before {
            content: '🌿';
            position: absolute;
            top: 30px;
            left: 30px;
            font-size: 40px;
            opacity: 0.5;
        }
        
        .sustainable-section::after {
            content: '🌍';
            position: absolute;
            bottom: 30px;
            right: 30px;
            font-size: 40px;
            opacity: 0.5;
        }
        
        .sustainable-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-top: 50px;
        }
        
        .sustainable-item {
            background: rgba(45, 3, 59, 0.6);
            padding: 30px;
            border-radius: 15px;
            text-align: center;
            border: 1px solid var(--eco-green);
            transition: transform 0.3s ease;
        }
        
        .sustainable-item:hover {
            transform: translateY(-10px);
            border-color: var(--gold);
        }
        
        .sustainable-icon {
            font-size: 2.5rem;
            margin-bottom: 20px;
            color: var(--eco-green);
        }
        
        /* Venue Section */
        .venue-section {
            padding: 80px 0;
            background: rgba(45, 3, 59, 0.3);
            border-radius: 20px;
            margin: 60px 0;
        }
        
        .venue-details {
            max-width: 800px;
            margin: 50px auto 0;
            background: rgba(26, 0, 31, 0.8);
            padding: 50px;
            border-radius: 20px;
            border: 2px solid var(--royal-purple);
            box-shadow: 0 20px 40px rgba(0,0,0,0.4);
        }
        
        /* RSVP Section */
        .rsvp-section {
            padding: 80px 0;
            text-align: center;
        }
        
        .rsvp-details {
            background: linear-gradient(145deg, rgba(45, 3, 59, 0.9), rgba(26, 0, 31, 0.9));
            padding: 60px;
            border-radius: 20px;
            max-width: 900px;
            margin: 50px auto 0;
            border: 2px solid var(--amethyst);
            box-shadow: 0 25px 50px rgba(0,0,0,0.5);
            position: relative;
            overflow: hidden;
        }
        
        .rsvp-details::before {
            content: '💌';
            position: absolute;
            top: 20px;
            right: 20px;
            font-size: 40px;
            opacity: 0.3;
        }
        
        .contact-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
            margin-top: 40px;
        }
        
        .contact-card {
            background: rgba(155, 89, 182, 0.2);
            padding: 30px;
            border-radius: 15px;
            border: 1px solid var(--amethyst);
            transition: all 0.3s ease;
        }
        
        .contact-card:hover {
            background: rgba(155, 89, 182, 0.3);
            transform: translateY(-5px);
            border-color: var(--gold);
        }
        
        /* Footer */
        footer {
            background: linear-gradient(135deg, var(--deep-purple) 0%, #0A0014 100%);
            color: var(--lavender);
            text-align: center;
            padding: 60px 0 40px;
            margin-top: 80px;
            border-top: 3px solid var(--gold);
            position: relative;
        }
        
        .footer-quote {
            font-family: 'Sacramento', cursive;
            font-size: 2.5rem;
            color: var(--light-gold);
            margin: 30px 0;
            max-width: 800px;
            margin: 30px auto;
            line-height: 1.4;
        }
        
        /* Responsive */
        @media (max-width: 992px) {
            h1 { font-size: 3rem; }
            .name { font-size: 2.5rem; }
            .ampersand { font-size: 4rem; margin: 30px 0; }
            .couple-names { flex-direction: column; }
            .bride, .groom { min-width: 100%; }
        }
        
        @media (max-width: 768px) {
            h1 { font-size: 2.5rem; }
            .sanskrit-title { font-size: 1.4rem; }
            .section-title { font-size: 2.5rem; }
            .quote-text { font-size: 1.5rem; }
            .event-card, .rsvp-details { padding: 30px; }
        }
        
        /* Decorative Elements */
        .decoration {
            text-align: center;
            color: var(--gold);
            font-size: 2rem;
            letter-spacing: 15px;
            margin: 40px 0;
            opacity: 0.8;
        }
        
        .mandala {
            display: flex;
            justify-content: center;
            margin: 40px 0;
        }
        
        .mandala i {
            color: var(--amethyst);
            margin: 0 10px;
            font-size: 1.5rem;
            animation: spin 10s linear infinite;
        }
        
        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }
        
        /* Countdown */
        .countdown {
            background: linear-gradient(135deg, var(--deep-purple), var(--royal-purple));
            padding: 30px;
            border-radius: 20px;
            text-align: center;
            margin: 60px auto;
            max-width: 800px;
            border: 2px solid var(--gold);
            box-shadow: 0 15px 35px rgba(106, 13, 173, 0.3);
        }
        
        .countdown-title {
            font-size: 1.8rem;
            margin-bottom: 30px;
            color: var(--light-gold);
        }
        
        .countdown-timer {
            display: flex;
            justify-content: center;
            gap: 25px;
            flex-wrap: wrap;
        }
        
        .countdown-item {
            background: rgba(255, 255, 255, 0.1);
            padding: 20px 15px;
            border-radius: 15px;
            min-width: 100px;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 215, 0, 0.3);
        }
        
        .countdown-number {
            font-size: 3rem;
            font-weight: bold;
            display: block;
            color: var(--gold);
            text-shadow: 0 0 10px rgba(255, 215, 0, 0.5);
        }
        
        .countdown-label {
            font-size: 0.9rem;
            text-transform: uppercase;
            letter-spacing: 2px;
            color: var(--lavender);
            margin-top: 10px;
        }
    </style>
</head>
<body>
    <!-- Animated Background Elements -->
    <div class="floating-element"></div>
    <div class="floating-element"></div>
    
    <!-- Header -->
    <header>
        <div class="container header-content">
            <h1>Pavan &amp; Roopa</h1>
            <div class="sanskrit-title">सहधर्मचारिणी भव</div>
            <div class="subtitle">Invite you to their Sacred Union</div>
            <div class="mandala">
                <i class="fas fa-om"></i>
                <i class="fas fa-star-of-david"></i>
                <i class="fas fa-infinity"></i>
                <i class="fas fa-heart"></i>
                <i class="fas fa-om"></i>
            </div>
            <div class="hashtags">
                <span class="hashtag">#PaRo</span>
                <span class="hashtag">#TeamPaRo</span>
                <span class="hashtag">#SustainableWedding</span>
            </div>
        </div>
    </header>

    <!-- Countdown Timer -->
    <div class="container">
        <div class="countdown">
            <div class="countdown-title">Countdown to Our Sacred Union</div>
            <div class="countdown-timer">
                <div class="countdown-item">
                    <span class="countdown-number" id="days">003</span>
                    <span class="countdown-label">Days</span>
                </div>
                <div class="countdown-item">
                    <span class="countdown-number" id="hours">12</span>
                    <span class="countdown-label">Hours</span>
                </div>
                <div class="countdown-item">
                    <span class="countdown-number" id="minutes">59</span>
                    <span class="countdown-label">Minutes</span>
                </div>
                <div class="countdown-item">
                    <span class="countdown-number" id="seconds">02</span>
                    <span class="countdown-label">Seconds</span>
                </div>
            </div>
        </div>
    </div>

    <!-- Couple Section -->
    <section class="couple-section">
        <div class="container">
            <div class="couple-names">
                <div class="groom">
                    <div class="name">Pavan Kumar U</div>
                    <div class="parents">Son of<br>Mr. Umeshappa &amp; Mrs. Lakkamma<br>Burudekatte, Hosadurga Taluk</div>
                    <div class="decoration" style="margin-top: 20px;">🌸 🌸 🌸</div>
                </div>
                
                <div class="ampersand">&amp;</div>
                
                <div class="bride">
                    <div class="name">Roopa M H</div>
                    <div class="parents">Daughter of<br>Mr. Halappa M B &amp; Mrs. Yashodha<br>M. Hosahalli, Ajjampura Taluk</div>
                    <div class="decoration" style="margin-top: 20px;">🌸 🌸 🌸</div>
                </div>
            </div>
            
            <!-- Hindu Scripture Quote -->
            <div class="scripture-quote">
                <div class="quote-text">
                    "Where the wife is happy, the household will be happy. Where the household is happy, all worldly and spiritual acts will be successful."
                </div>
                <div class="quote-source">— Manusmriti 3.60</div>
            </div>
            
            <p style="font-size: 1.3rem; max-width: 900px; margin: 50px auto; line-height: 1.9; text-align: center; color: #C9B6E4;">
                With the divine blessings of the Almighty and our beloved elders, we joyfully invite you to witness our sacred union as we embark on the eternal journey of marriage according to Hindu Vedic traditions. Your presence will sanctify our bond and fill our hearts with divine joy.
            </p>
        </div>
    </section>

    <!-- Events Section -->
    <section class="events-section">
        <div class="container">
            <h2 class="section-title">Vivaah Mahotsav</h2>
            
            <div class="events-grid">
                <div class="event-card">
                    <h3 class="event-title">Reception &amp; Swagat</h3>
                    <div class="event-subtitle">A divine evening of blessings and celebrations</div>
                    
                    <div class="event-details">
                        <div class="detail-item">
                            <i class="fas fa-calendar-alt detail-icon"></i>
                            <div>
                                <strong style="color: var(--gold);">Date:</strong> 
                                <span style="font-size: 1.1rem;">Wednesday, 18th February 2026</span>
                            </div>
                        </div>
                        
                        <div class="detail-item">
                            <i class="fas fa-clock detail-icon"></i>
                            <div>
                                <strong style="color: var(--gold);">Time:</strong> 
                                <span style="font-size: 1.1rem;">7:00 PM Onwards</span>
                            </div>
                        </div>
                    </div>
                    
                    <div class="scripture-quote" style="padding: 20px; margin: 25px 0; background: rgba(155, 89, 182, 0.1);">
                        <div class="quote-text" style="font-size: 1.1rem;">
                            "Let there be harmony between husband and wife for the welfare of the family and society."
                        </div>
                        <div class="quote-source" style="font-size: 0.9rem;">— Atharva Veda</div>
                    </div>
                </div>
                
                <div class="event-card">
                    <h3 class="event-title">Sacred Wedding Ceremony</h3>
                    <div class="event-subtitle">The Auspicious Muhurtha - Seven Steps to Eternal Union</div>
                    
                    <div class="event-details">
                        <div class="detail-item">
                            <i class="fas fa-calendar-alt detail-icon"></i>
                            <div>
                                <strong style="color: var(--gold);">Date:</strong> 
                                <span style="font-size: 1.1rem;">Thursday, 19th February 2026</span>
                            </div>
                        </div>
                        
                        <div class="muhurtha-highlight">
                            <div class="detail-item">
                                <i class="fas fa-clock detail-icon"></i>
                                <div>
                                    <strong style="color: var(--gold); font-size: 1.2rem;">Auspicious Muhurtha:</strong> 
                                    <span style="font-size: 1.2rem; color: var(--light-gold);">05:00 AM to 06:00 AM</span>
                                </div>
                            </div>
                        </div>
                    </div>
                    
                    <p style="margin-top: 25px; font-size: 0.95rem; color: #C9B6E4; background: rgba(255, 215, 0, 0.1); padding: 15px; border-radius: 10px;">
                        <i class="fas fa-info-circle" style="color: var(--gold);"></i> 
                        Please join us for the pre-wedding Vedic rituals starting from 4:30 AM onwards.
                    </p>
                </div>
            </div>
        </div>
    </section>

    <!-- Venue Section -->
    <section class="venue-section">
        <div class="container">
            <h2 class="section-title">Sacred Venue</h2>
            
            <div class="venue-details">
                <h3 style="color: var(--lavender); margin-bottom: 25px; font-size: 2.2rem; text-align: center;">
                    Sri Siddarameshwara Kalyana Mantapa
                </h3>
                
                <div class="detail-item" style="justify-content: center; margin-bottom: 30px;">
                    <i class="fas fa-map-marker-alt" style="color: var(--gold); font-size: 2rem; margin-right: 15px;"></i>
                    <div style="font-size: 1.3rem; text-align: center;">
                        Ajjampura, Chitradurga District,<br>
                        Karnataka - 577527
                    </div>
                </div>
                
                <!-- Map Link -->
                <div style="text-align: center; margin: 40px 0;">
                    <a href="https://maps.app.goo.gl/vUFsnhiLQxkAsvim6" target="_blank" style="display: inline-block; background: linear-gradient(45deg, var(--royal-purple), var(--amethyst)); 
                              color: white; padding: 15px 30px; border-radius: 50px; text-decoration: none; 
                              font-weight: 600; font-size: 1.1rem; box-shadow: 0 5px 15px rgba(155, 89, 182, 0.3);
                              transition: transform 0.3s ease;">
                        <i class="fas fa-map-marker-alt" style="margin-right: 10px;"></i>
                        View on Google Maps
                    </a>
                </div>
                
                <div class="scripture-quote" style="padding: 25px; margin-top: 40px; background: rgba(155, 89, 182, 0.1);">
                    <div class="quote-text" style="font-size: 1.3rem;">
                        "May our gathering be blessed with divine presence and our union be witnessed by the heavens."
                    </div>
                    <div class="quote-source">— Rig Veda</div>
                </div>
            </div>
        </div>
    </section>

    <!-- RSVP Section -->
    <section class="rsvp-section">
        <div class="container">
            <h2 class="section-title">RSVP &amp; Blessings</h2>
            
            <div class="scripture-quote" style="max-width: 800px; margin: 0 auto 40px;">
                <div class="quote-text">
                    "May you both be blessed with a long life, may you both serve the society through your offspring, may you both be blessed with bright, healthy, intelligent, and obedient children."
                </div>
                <div class="quote-source">— Hindu Wedding Blessings</div>
            </div>
            
            <div class="rsvp-details">
                <p style="font-size: 1.3rem; margin-bottom: 30px; line-height: 1.8;">
                    Your presence is the most precious blessing we could ask for as we begin this sacred journey together. Please confirm your attendance by contacting our family members:
                </p>
                
                <div class="contact-grid">
                    <div class="contact-card">
                        <h3 style="color: var(--gold); margin-bottom: 15px; font-size: 1.8rem;">
                            <i class="fas fa-phone-alt"></i> Umeshappa
                        </h3>
                        <div class="contact-person">
                            <a href="tel:9945711452" style="color: var(--lavender); text-decoration: none; font-size: 1.4rem; font-weight: 600;">
                                9945711452
                            </a>
                        </div>
                        <p style="margin-top: 15px; color: #C9B6E4; font-size: 0.95rem;">
                            For reception and general inquiries
                        </p>
                    </div>
                    
                    <div class="contact-card">
                        <h3 style="color: var(--gold); margin-bottom: 15px; font-size: 1.8rem;">
                            <i class="fas fa-phone-alt"></i> Punith
                        </h3>
                        <div class="contact-person">
                            <a href="tel:7259484249" style="color: var(--lavender); text-decoration: none; font-size: 1.4rem; font-weight: 600;">
                                7259484249
                            </a>
                        </div>
                        <p style="margin-top: 15px; color: #C9B6E4; font-size: 0.95rem;">
                            For wedding ceremony and venue details
                        </p>
                    </div>
                </div>
                
                <div class="scripture-quote" style="padding: 20px; margin-top: 40px; background: rgba(255, 215, 0, 0.1);">
                    <div class="quote-text" style="font-size: 1.1rem;">
                        Please RSVP by 16th February 2026 to help us make necessary arrangements for our sustainable celebration.
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="decoration" style="color: var(--light-gold);">🌸 🌸 🌸 🌸 🌸</div>
            
            <div class="footer-quote">
                "May our union be filled with eternal love, understanding, and divine blessings."
            </div>
            
            <div class="scripture-quote" style="max-width: 700px; margin: 30px auto; padding: 30px; background: rgba(155, 89, 182, 0.2);">
                <div class="quote-text" style="font-size: 1.4rem;">
                    "You have become mine forever. Yes, we have become partners. I have become yours. Hereafter, I cannot live without you. Do not live without me."
                </div>
                <div class="quote-source">— Saptapadi Mantra (Seven Steps Vows)</div>
            </div>
            
            <p style="margin: 30px 0; font-size: 1.3rem; line-height: 1.8;">
                With heartfelt gratitude and divine blessings,<br>
                <strong style="color: var(--gold); font-size: 1.5rem;">Pavan &amp; Roopa</strong><br>
                Along with Our Families
            </p>
            
            <div class="hashtags" style="margin-top: 40px;">
                <span class="hashtag" style="border-color: var(--light-gold);">#PaRo</span>
                <span class="hashtag" style="border-color: var(--light-gold);">#TeamPaRo</span>
                <span class="hashtag" style="border-color: var(--light-gold);">#SustainableWedding</span>
                <span class="hashtag" style="border-color: var(--light-gold);">#SacredUnion2026</span>
            </div>
            
            <div class="mandala" style="margin: 40px 0;">
                <i class="fas fa-om" style="color: var(--gold);"></i>
                <i class="fas fa-heart" style="color: var(--amethyst);"></i>
                <i class="fas fa-infinity" style="color: var(--lavender);"></i>
                <i class="fas fa-leaf" style="color: var(--eco-green);"></i>
                <i class="fas fa-om" style="color: var(--gold);"></i>
            </div>
            
            <p style="margin-top: 30px; color: rgba(255,255,255,0.7); font-size: 1rem;">
                18th &amp; 19th February 2026 | Sri Siddarameshwara Kalyana Mantapa, Ajjampura, B.H.Road, Chikkamagaluru Dist, Karnataka<br>
                A Sustainable Celebration of Love &amp; Tradition
            </p>
        </div>
    </footer>

    <!-- JavaScript -->
    <script>
        // Set the wedding date (February 15, 2026)
        const weddingDate = new Date('February 19, 2026 05:00:00').getTime();
        
        // Update the countdown every second
        const countdownTimer = setInterval(function() {
            const now = new Date().getTime();
            const timeRemaining = weddingDate - now;
            
            // Calculate days, hours, minutes, seconds
            const days = Math.floor(timeRemaining / (1000 * 60 * 60 * 24));
            const hours = Math.floor((timeRemaining % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
            const minutes = Math.floor((timeRemaining % (1000 * 60 * 60)) / (1000 * 60));
            const seconds = Math.floor((timeRemaining % (1000 * 60)) / 1000);
            
            // Display the results
            document.getElementById('days').innerHTML = days.toString().padStart(3, '0');
            document.getElementById('hours').innerHTML = hours.toString().padStart(2, '0');
            document.getElementById('minutes').innerHTML = minutes.toString().padStart(2, '0');
            document.getElementById('seconds').innerHTML = seconds.toString().padStart(2, '0');
            
            // If the countdown is over
            if (timeRemaining < 0) {
                clearInterval(countdownTimer);
                document.querySelector('.countdown-timer').innerHTML = 
                    '<div style="font-size: 1.8rem; padding: 20px; color: var(--gold);">The wedding has begun! Thank you for celebrating with us!</div>';
            }
        }, 1000);
        
        // Add smooth scrolling for navigation
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const targetId = this.getAttribute('href');
                if(targetId === '#') return;
                
                const targetElement = document.querySelector(targetId);
                if(targetElement) {
                    window.scrollTo({
                        top: targetElement.offsetTop - 80,
                        behavior: 'smooth'
                    });
                }
            });
        });
    </script>

<script>'undefined'=== typeof _trfq || (window._trfq = []);'undefined'=== typeof _trfd && (window._trfd=[]),_trfd.push({'tccl.baseHost':'secureserver.net'},{'ap':'cpsh-oh'},{'server':'sg2plzcpnl508747'},{'dcenter':'sg2'},{'cp_id':'10855977'},{'cp_cl':'8'}) // Monitoring performance to make your website faster. If you want to opt-out, please contact web hosting support.</script><script src="https://img1.wsimg.com/traffic-assets/js/tccl.min.js"></script></body></html>
