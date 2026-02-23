<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ceejay's Car Hire | Luxury & Daily Car Rentals in Nairobi</title>
    <style>
        /* CSS Styles */
        :root {
            --primary-color: #aa0000; /* Deep Red */
            --dark-bg: #111111;
            --card-bg: #1e1e1e;
            --text-light: #ffffff;
            --text-muted: #aaaaaa;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background-color: var(--dark-bg);
            color: var(--text-light);
            line-height: 1.6;
        }

        /* Navigation */
        header {
            background-color: #000;
            padding: 1rem 5%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: sticky;
            top: 0;
            z-index: 1000;
            border-bottom: 2px solid var(--primary-color);
        }

        .logo {
            font-size: 1.5rem;
            font-weight: bold;
            color: var(--text-light);
            text-decoration: none;
            letter-spacing: 1px;
        }

        .logo span {
            color: var(--primary-color);
        }

        nav ul {
            list-style: none;
            display: flex;
            gap: 20px;
        }

        nav a {
            color: var(--text-light);
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
        }

        nav a:hover {
            color: var(--primary-color);
        }

        /* Hero Section */
        .hero {
            text-align: center;
            padding: 100px 20px;
            background: linear-gradient(rgba(0,0,0,0.8), rgba(0,0,0,0.8)), url('https://images.unsplash.com/photo-1549317661-bd32c8ce0db2?auto=format&fit=crop&q=80') center/cover;
        }

        .hero h1 {
            font-size: 3rem;
            margin-bottom: 20px;
        }

        .hero p {
            font-size: 1.2rem;
            color: var(--text-muted);
            margin-bottom: 30px;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
        }

        .btn {
            background-color: var(--primary-color);
            color: white;
            padding: 12px 30px;
            text-decoration: none;
            border-radius: 5px;
            font-size: 1.1rem;
            font-weight: bold;
            transition: background 0.3s;
            display: inline-block;
        }

        .btn:hover {
            background-color: #cc0000;
        }

        /* Section Titles */
        .section-title {
            text-align: center;
            font-size: 2.5rem;
            margin: 60px 0 40px;
            color: var(--text-light);
        }

        .section-title span {
            color: var(--primary-color);
        }

        /* Fleet Grid */
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        .fleet-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 20px;
        }

        .car-card {
            background-color: var(--card-bg);
            border-radius: 8px;
            padding: 20px;
            text-align: center;
            border: 1px solid #333;
            transition: transform 0.3s, border-color 0.3s;
        }

        .car-card:hover {
            transform: translateY(-5px);
            border-color: var(--primary-color);
        }

        .car-class {
            font-size: 0.9rem;
            color: var(--primary-color);
            text-transform: uppercase;
            letter-spacing: 1px;
            margin-bottom: 10px;
            display: block;
        }

        .car-title {
            font-size: 1.4rem;
            margin-bottom: 15px;
        }

        .car-price {
            font-size: 1.2rem;
            font-weight: bold;
            color: #ddd;
            margin-bottom: 20px;
        }

        .car-price span {
            font-size: 0.9rem;
            color: var(--text-muted);
            font-weight: normal;
        }

        .book-btn {
            display: block;
            width: 100%;
            background-color: #25D366; /* WhatsApp Green */
            color: white;
            padding: 10px;
            text-decoration: none;
            border-radius: 4px;
            font-weight: bold;
            transition: opacity 0.3s;
        }

        .book-btn:hover {
            opacity: 0.8;
        }

        /* Reviews Section */
        .reviews-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-bottom: 60px;
        }

        .review-card {
            background-color: var(--card-bg);
            padding: 30px;
            border-radius: 8px;
            border-left: 4px solid var(--primary-color);
        }

        .stars {
            color: #FFD700; /* Gold */
            margin-bottom: 15px;
            font-size: 1.2rem;
        }

        .review-text {
            font-style: italic;
            color: #ccc;
            margin-bottom: 15px;
        }

        .reviewer-name {
            font-weight: bold;
            color: var(--text-light);
        }

        /* Footer */
        footer {
            background-color: #000;
            text-align: center;
            padding: 40px 20px;
            margin-top: 50px;
            border-top: 1px solid #333;
        }

        .footer-info p {
            margin: 10px 0;
            color: var(--text-muted);
        }

        /* Floating WhatsApp Button */
        .float-wa {
            position: fixed;
            width: 60px;
            height: 60px;
            bottom: 40px;
            right: 40px;
            background-color: #25d366;
            color: #FFF;
            border-radius: 50px;
            text-align: center;
            font-size: 30px;
            box-shadow: 2px 2px 3px #999;
            z-index: 100;
            display: flex;
            align-items: center;
            justify-content: center;
            text-decoration: none;
        }
        
        .float-wa:hover {
            background-color: #128C7E;
        }

        /* Mobile Adjustments */
        @media (max-width: 768px) {
            nav ul {
                display: none; /* Hide standard nav on mobile for simplicity in this template */
            }
            .hero h1 {
                font-size: 2.2rem;
            }
        }
    </style>
</head>
<body>

    <header>
        <a href="#" class="logo">CEEJAY'S <span>CAR HIRE</span></a>
        <nav>
            <ul>
                <li><a href="#home">Home</a></li>
                <li><a href="#fleet">Our Fleet</a></li>
                <li><a href="#reviews">Reviews</a></li>
            </ul>
        </nav>
        <a href="https://wa.me/254748007024" class="btn" style="padding: 8px 15px; font-size: 0.9rem;">Contact Us</a>
    </header>

    <section class="hero" id="home">
        <h1>Drive the Best in Nairobi</h1>
        <p>Premium luxury vehicles, rugged 4x4s, and reliable daily rentals. Experience unmatched comfort with self-drive and chauffeur services.</p>
        <a href="#fleet" class="btn">View Our Fleet</a>
    </section>

    <div class="container" id="fleet">
        <h2 class="section-title">Our <span>Fleet & Pricing</span></h2>
        
        <div class="fleet-grid">
            
            <div class="car-card">
                <span class="car-class">Ultra Luxury</span>
                <h3 class="car-title">Range Rover Vogue</h3>
                <p class="car-price">Ksh 60,000 <span>/ day</span></p>
                <a href="https://wa.me/254748007024?text=Hi, I'm interested in booking the Range Rover Vogue." class="book-btn">Book via WhatsApp</a>
            </div>

            <div class="car-card">
                <span class="car-class">Luxury SUV</span>
                <h3 class="car-title">Lexus LX 570</h3>
                <p class="car-price">Ksh 45,000 <span>/ day</span></p>
                <a href="https://wa.me/254748007024?text=Hi, I'm interested in booking the Lexus LX 570." class="book-btn">Book via WhatsApp</a>
            </div>

            <div class="car-card">
                <span class="car-class">Executive Sedan</span>
                <h3 class="car-title">Mercedes S-Class</h3>
                <p class="car-price">Ksh 45,000 <span>/ day</span></p>
                <a href="https://wa.me/254748007024?text=Hi, I'm interested in booking the Mercedes S-Class." class="book-btn">Book via WhatsApp</a>
            </div>

            <div class="car-card">
                <span class="car-class">Luxury SUV</span>
                <h3 class="car-title">Mercedes GLE 43</h3>
                <p class="car-price">Ksh 35,000 <span>/ day</span></p>
                <a href="https://wa.me/254748007024?text=Hi, I'm interested in booking the Mercedes GLE 43." class="book-btn">Book via WhatsApp</a>
            </div>

            <div class="car-card">
                <span class="car-class">Premium SUV</span>
                <h3 class="car-title">Land Cruiser V8</h3>
                <p class="car-price">Ksh 25,000 <span>/ day</span></p>
                <a href="https://wa.me/254748007024?text=Hi, I'm interested in booking the Land Cruiser V8." class="book-btn">Book via WhatsApp</a>
            </div>

            <div class="car-card">
                <span class="car-class">Premium SUV</span>
                <h3 class="car-title">Mercedes GLC 200</h3>
                <p class="car-price">Ksh 25,000 <span>/ day</span></p>
                <a href="https://wa.me/254748007024?text=Hi, I'm interested in booking the Mercedes GLC 200." class="book-btn">Book via WhatsApp</a>
            </div>

            <div class="car-card">
                <span class="car-class">Executive Sedan</span>
                <h3 class="car-title">Mercedes E240 / E200</h3>
                <p class="car-price">Ksh 22,000 <span>/ day</span></p>
                <a href="https://wa.me/254748007024?text=Hi, I'm interested in booking the Mercedes E-Class." class="book-btn">Book via WhatsApp</a>
            </div>

            <div class="car-card">
                <span class="car-class">Executive SUV</span>
                <h3 class="car-title">Toyota Prado J150</h3>
                <p class="car-price">Ksh 15,000 <span>/ day</span></p>
                <a href="https://wa.me/254748007024?text=Hi, I'm interested in booking the Toyota Prado J150." class="book-btn">Book via WhatsApp</a>
            </div>

            <div class="car-card">
                <span class="car-class">Executive Sedan</span>
                <h3 class="car-title">Mercedes C200</h3>
                <p class="car-price">Ksh 15,000 <span>/ day</span></p>
                <a href="https://wa.me/254748007024?text=Hi, I'm interested in booking the Mercedes C200." class="book-btn">Book via WhatsApp</a>
            </div>

            <div class="car-card">
                <span class="car-class">Mid-Size SUV</span>
                <h3 class="car-title">Toyota Harrier</h3>
                <p class="car-price">Ksh 9,000 <span>/ day</span></p>
                <a href="https://wa.me/254748007024?text=Hi, I'm interested in booking the Toyota Harrier." class="book-btn">Book via WhatsApp</a>
            </div>

            <div class="car-card">
                <span class="car-class">Mid-Size SUV</span>
                <h3 class="car-title">Mazda CX-5</h3>
                <p class="car-price">Ksh 7,000 <span>/ day</span></p>
                <a href="https://wa.me/254748007024?text=Hi, I'm interested in booking the Mazda CX-5." class="book-btn">Book via WhatsApp</a>
            </div>

            <div class="car-card">
                <span class="car-class">Mid-Size SUV</span>
                <h3 class="car-title">Nissan X-Trail</h3>
                <p class="car-price">Ksh 7,000 <span>/ day</span></p>
                <a href="https://wa.me/254748007024?text=Hi, I'm interested in booking the Nissan X-Trail." class="book-btn">Book via WhatsApp</a>
            </div>

            <div class="car-card">
                <span class="car-class">Mid-Size SUV</span>
                <h3 class="car-title">Mitsubishi Outlander</h3>
                <p class="car-price">Ksh 7,000 <span>/ day</span></p>
                <a href="https://wa.me/254748007024?text=Hi, I'm interested in booking the Mitsubishi Outlander." class="book-btn">Book via WhatsApp</a>
            </div>

            <div class="car-card">
                <span class="car-class">Premium Sedan</span>
                <h3 class="car-title">Toyota Crown</h3>
                <p class="car-price">Ksh 7,000 <span>/ day</span></p>
                <a href="https://wa.me/254748007024?text=Hi, I'm interested in booking the Toyota Crown." class="book-btn">Book via WhatsApp</a>
            </div>

            <div class="car-card">
                <span class="car-class">Premium Sedan</span>
                <h3 class="car-title">Toyota Mark X</h3>
                <p class="car-price">Ksh 6,000 <span>/ day</span></p>
                <a href="https://wa.me/254748007024?text=Hi, I'm interested in booking the Toyota Mark X." class="book-btn">Book via WhatsApp</a>
            </div>

            <div class="car-card">
                <span class="car-class">Standard Sedan</span>
                <h3 class="car-title">Toyota Premio / Allion</h3>
                <p class="car-price">Ksh 5,000 <span>/ day</span></p>
                <a href="https://wa.me/254748007024?text=Hi, I'm interested in booking the Premio/Allion." class="book-btn">Book via WhatsApp</a>
            </div>

            <div class="car-card">
                <span class="car-class">Economy Station Wagon</span>
                <h3 class="car-title">Toyota Axio / Fielder</h3>
                <p class="car-price">Ksh 4,500 <span>/ day</span></p>
                <a href="https://wa.me/254748007024?text=Hi, I'm interested in booking the Axio/Fielder." class="book-btn">Book via WhatsApp</a>
            </div>

            <div class="car-card">
                <span class="car-class">Compact / Hatchback</span>
                <h3 class="car-title">Demio / Note / Vitz</h3>
                <p class="car-price">Ksh 3,500 <span>/ day</span></p>
                <a href="https://wa.me/254748007024?text=Hi, I'm interested in booking a compact car (Demio/Note/Vitz)." class="book-btn">Book via WhatsApp</a>
            </div>

        </div>
    </div>

    <div class="container" id="reviews">
        <h2 class="section-title">Client <span>Reviews</span></h2>
        <div class="reviews-grid">
            <div class="review-card">
                <div class="stars">★★★★★</div>
                <p class="review-text">"Hired the Mercedes E-Class for my wedding weekend. The car was spotless, fueled up, and the service was incredibly professional. Highly recommend Ceejay's Car Hire!"</p>
                <p class="reviewer-name">- David M.</p>
            </div>
            <div class="review-card">
                <div class="stars">★★★★★</div>
                <p class="review-text">"Got the Prado J150 for a business trip to Naivasha. It handled the roads perfectly. Seamless booking process via WhatsApp and great customer support."</p>
                <p class="reviewer-name">- Sarah W.</p>
            </div>
            <div class="review-card">
                <div class="stars">★★★★★</div>
                <p class="review-text">"The most reliable car rental in Nairobi. I regularly rent the Mazda CX-5 for weekend errands. The cars are always well-maintained and delivered on time."</p>
                <p class="reviewer-name">- James K.</p>
            </div>
        </div>
    </div>

    <a href="https://wa.me/254748007024" class="float-wa" target="_blank" title="Chat with us on WhatsApp">
        <svg width="35" height="35" viewBox="0 0 24 24" fill="white" xmlns="http://www.w3.org/2000/svg">
            <path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 00-3.48-8.413Z"/>
        </svg>
    </a>

    <footer>
        <div class="footer-info">
            <h2 style="color: white; margin-bottom: 15px;">Ceejay's Car Hire</h2>
            <p>📍 Nairobi, Kenya</p>
            <p>📞 0748007024</p>
            <p>✉️ info@ceejayscarhire.co.ke</p>
            <p style="margin-top: 20px; font-size: 0.8rem;">&copy; 2026 Ceejay's Car Hire. All rights reserved.</p>
        </div>
    </footer>

</body>
</html>

