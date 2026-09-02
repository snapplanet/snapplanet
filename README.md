
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Snap Planet – Explore the future</title>
    <!-- Font Awesome 6 (free) -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css" />
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Roboto, system-ui, -apple-system, sans-serif;
        }
        body {
            background: #f5f7fc;
            color: #1e1e2f;
        }
        a {
            text-decoration: none;
            color: inherit;
        }
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 24px;
        }
        /* header */
        header {
            background: #ffffff;
            box-shadow: 0 4px 12px rgba(0,0,0,0.04);
            padding: 16px 0;
            position: sticky;
            top: 0;
            z-index: 100;
            border-bottom: 1px solid #eef2f7;
        }
        .header-grid {
            display: flex;
            align-items: center;
            justify-content: space-between;
            flex-wrap: wrap;
        }
        .logo-area {
            display: flex;
            align-items: center;
            gap: 12px;
        }
        .logo-area img {
            height: 48px;
            width: auto;
            border-radius: 10px;
            object-fit: contain;
        }
        .brand {
            font-size: 1.8rem;
            font-weight: 700;
            letter-spacing: -0.5px;
            background: linear-gradient(145deg, #0b2b5c, #1f4f8a);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }
        nav {
            display: flex;
            gap: 32px;
            flex-wrap: wrap;
            font-weight: 500;
        }
        nav a {
            color: #2c3e58;
            transition: 0.2s;
            border-bottom: 2px solid transparent;
            padding-bottom: 4px;
            font-size: 1rem;
        }
        nav a:hover {
            color: #1f4f8a;
            border-bottom-color: #1f4f8a;
        }

        /* buttons */
        .btn-primary {
            background: linear-gradient(145deg, #0b2b5c, #1f4f8a);
            border: none;
            padding: 14px 38px;
            border-radius: 60px;
            font-weight: 700;
            font-size: 1rem;
            color: white;
            display: inline-block;
            transition: 0.25s;
            box-shadow: 0 8px 20px rgba(31, 79, 138, 0.25);
            cursor: pointer;
        }
        .btn-primary:hover {
            transform: scale(1.03);
            background: #1f4f8a;
            box-shadow: 0 12px 28px rgba(31, 79, 138, 0.35);
        }
        .btn-outline {
            background: transparent;
            border: 2px solid #1f4f8a;
            color: #1f4f8a;
            padding: 12px 32px;
            border-radius: 60px;
            font-weight: 600;
            transition: 0.2s;
            display: inline-block;
        }
        .btn-outline:hover {
            background: #1f4f8a;
            color: white;
        }

        section {
            padding: 64px 0;
        }
        .section-title {
            font-size: 2.4rem;
            font-weight: 700;
            margin-bottom: 20px;
            letter-spacing: -0.5px;
            color: #0b2b5c;
        }
        .section-sub {
            color: #415a77;
            max-width: 700px;
            margin-bottom: 28px;
            font-size: 1.1rem;
        }

        /* hero */
        .hero {
            background: linear-gradient(135deg, #eef4ff 0%, #ffffff 80%);
            border-radius: 40px;
            padding: 56px 48px;
            margin-top: 12px;
            border: 1px solid #dce6f2;
        }
        .hero h1 {
            font-size: 3rem;
            font-weight: 800;
            line-height: 1.2;
            color: #0b2b5c;
        }
        .hero h1 span {
            background: linear-gradient(145deg, #1f4f8a, #3b7bb7);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }
        .hero p {
            font-size: 1.2rem;
            color: #2c3e58;
            max-width: 700px;
            line-height: 1.6;
            margin-top: 12px;
        }
        .hero .cta-group {
            margin-top: 32px;
            display: flex;
            gap: 20px;
            flex-wrap: wrap;
            align-items: center;
        }

        /* two col */
        .two-col {
            display: flex;
            flex-wrap: wrap;
            gap: 48px;
            align-items: center;
        }
        .two-col .text {
            flex: 1 1 45%;
        }
        .two-col .image {
            flex: 1 1 45%;
            text-align: center;
        }
        .two-col .image img {
            max-width: 100%;
            border-radius: 28px;
            box-shadow: 0 20px 40px rgba(0,0,0,0.06);
            max-height: 340px;
            object-fit: contain;
        }
        .two-col h2 {
            font-size: 2.1rem;
            margin-bottom: 16px;
            color: #0b2b5c;
        }
        .two-col p {
            color: #2c3e58;
            line-height: 1.8;
            margin-bottom: 16px;
        }

        /* services */
        .service-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(220px, 1fr));
            gap: 28px;
            margin-top: 24px;
        }
        .service-card {
            background: #ffffff;
            padding: 28px 18px;
            border-radius: 28px;
            border: 1px solid #e2ebf6;
            transition: 0.25s;
            text-align: center;
            box-shadow: 0 4px 12px rgba(0,0,0,0.02);
        }
        .service-card:hover {
            border-color: #1f4f8a;
            transform: translateY(-6px);
            box-shadow: 0 16px 32px rgba(31,79,138,0.08);
        }
        .service-card i {
            font-size: 2.6rem;
            color: #1f4f8a;
            margin-bottom: 14px;
        }
        .service-card h4 {
            font-size: 1.1rem;
            color: #0b2b5c;
        }

        /* why choose */
        .points-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
            gap: 24px;
            margin-top: 12px;
        }
        .point-item {
            background: white;
            padding: 20px 18px;
            border-radius: 24px;
            border-left: 5px solid #1f4f8a;
            box-shadow: 0 4px 12px rgba(0,0,0,0.02);
        }
        .point-item i {
            color: #1f4f8a;
            margin-right: 10px;
        }

        /* reviews */
        .review-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(210px, 1fr));
            gap: 24px;
        }
        .review-card {
            background: white;
            padding: 22px 16px;
            border-radius: 28px;
            border: 1px solid #e2ebf6;
            display: flex;
            flex-direction: column;
            align-items: center;
            text-align: center;
        }
        .review-card img {
            width: 72px;
            height: 72px;
            border-radius: 50%;
            object-fit: cover;
            margin-bottom: 12px;
            border: 3px solid #dce6f2;
        }
        .review-card .name {
            font-weight: 600;
            color: #0b2b5c;
        }
        .review-card .quote {
            color: #415a77;
            font-style: italic;
            font-size: 0.95rem;
            margin-top: 8px;
        }

        /* areas */
        .area-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 18px;
            margin-top: 12px;
        }
        .area-tag {
            background: white;
            padding: 14px 32px;
            border-radius: 60px;
            border: 1px solid #d0ddeb;
            font-weight: 500;
            color: #0b2b5c;
            transition: 0.2s;
        }
        .area-tag:hover {
            border-color: #1f4f8a;
            background: #f0f6ff;
        }

        /* FAQ */
        .faq-list {
            display: flex;
            flex-direction: column;
            gap: 18px;
        }
        .faq-item {
            background: white;
            padding: 20px 28px;
            border-radius: 24px;
            border-left: 5px solid #1f4f8a;
            box-shadow: 0 4px 12px rgba(0,0,0,0.02);
        }
        .faq-item h4 {
            color: #0b2b5c;
            margin-bottom: 6px;
            font-size: 1.1rem;
        }
        .faq-item p {
            color: #2c3e58;
        }

        /* contact */
        .contact-wrap {
            display: flex;
            flex-wrap: wrap;
            gap: 48px;
            align-items: flex-start;
        }
        .contact-social {
            flex: 1 1 40%;
        }
        .contact-social .social-icons {
            display: flex;
            gap: 28px;
            font-size: 2.2rem;
            margin-top: 12px;
        }
        .contact-social .social-icons a {
            color: #2c3e58;
            transition: 0.2s;
        }
        .contact-social .social-icons a:hover {
            color: #1f4f8a;
            transform: scale(1.1);
        }
        .contact-map {
            flex: 1 1 40%;
            background: white;
            padding: 24px;
            border-radius: 32px;
            border: 1px solid #dce6f2;
            display: flex;
            align-items: center;
            justify-content: center;
            color: #415a77;
            gap: 12px;
        }
        .contact-map i {
            font-size: 2.8rem;
            color: #1f4f8a;
        }

        /* CTA block */
        .cta-block {
            background: linear-gradient(145deg, #eef4ff, #ffffff);
            border-radius: 48px;
            padding: 48px 40px;
            text-align: center;
            border: 1px solid #dce6f2;
        }
        .cta-block h2 {
            font-size: 2.3rem;
            color: #0b2b5c;
            margin-bottom: 12px;
        }
        .cta-block p {
            color: #2c3e58;
            max-width: 600px;
            margin: 12px auto;
            font-size: 1.1rem;
        }

        /* footer */
        footer {
            background: #ffffff;
            border-top: 1px solid #eef2f7;
            padding: 48px 0 24px;
        }
        .footer-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(180px, 1fr));
            gap: 32px;
        }
        .footer-col h5 {
            color: #0b2b5c;
            margin-bottom: 14px;
            font-size: 1.1rem;
        }
        .footer-col p, .footer-col a {
            color: #415a77;
            line-height: 1.9;
            display: block;
        }
        .footer-col a:hover {
            color: #1f4f8a;
        }
        .footer-bottom {
            text-align: center;
            padding-top: 28px;
            margin-top: 28px;
            border-top: 1px solid #eef2f7;
            color: #5b6f8c;
            font-size: 0.95rem;
        }

        @media (max-width: 700px) {
            .header-grid {
                flex-direction: column;
                gap: 16px;
            }
            nav {
                justify-content: center;
            }
            .hero h1 {
                font-size: 2.2rem;
            }
            .two-col {
                flex-direction: column;
            }
        }
    </style>
</head>
<body>

<header>
    <div class="container header-grid">
        <div class="logo-area">
        </div>
        <nav>
            <a href="#">Home</a>
            <a href="#services">Our Services</a>
            <a href="#areas">Service Areas</a>
            <a href="#about">About Us</a>
            <a href="#contact">Contact Us</a>
        </nav>
    </div>
</header>

<main class="container">
    <!-- Hero -->
    <section class="hero">
        <h1>Explore the future with <span>Snap Planet</span></h1>
        <p>Your gateway to next-gen tools and insights. <a href="https://snapplanets.app/" style="color:#1f4f8a; font-weight:600;">Snap Planet</a> delivers innovation, clarity, and performance. Start your journey today.</p>
        <div class="cta-group">
            <a href="#" class="btn-primary"><i class="fas fa-rocket"></i> Get Started</a>
            <a href="#" class="btn-outline">Learn More</a>
        </div>
    </section>

    <!-- About / first 2-col -->
    <section id="about">
        <div class="two-col">
            <div class="text">
                <h2>Snap Planet: smart solutions for modern needs</h2>
                <p>Snap Planet is built for those who value speed, simplicity, and reliability. Our platform combines intuitive design with powerful backend tools, making complex tasks feel effortless.</p>
                <p>Whether you're a creator, a business, or a curious mind, Snap Planet adapts to your workflow. We focus on delivering exceptional experiences across every touchpoint.</p>
            </div>
            <div class="image">
                <img src="https://snapplanets.app/wp-content/uploads/2026/07/ChatGPT-Image-Jul-25-2026-03_34_31-PM-e1784975819276.png" alt="Snap Planet illustration" />
            </div>
        </div>
    </section>

    <!-- second 2-col -->
    <section>
        <div class="two-col">
            <div class="image">
                <img src="https://snapplanets.app/wp-content/uploads/2026/07/ChatGPT-Image-Jul-25-2026-03_34_31-PM-e1784975819276.png" alt="Snap Planet creative" />
            </div>
            <div class="text">
                <h2>Innovation at the core of Snap Planet</h2>
                <p>We combine cutting-edge technology with a human touch. Snap Planet is designed to grow with you, offering flexible features that adapt to your evolving needs.</p>
                <p>From real-time analytics to seamless integrations, our platform is the engine behind your next big idea. Experience the difference with Snap Planet.</p>
            </div>
        </div>
    </section>

    <!-- Services -->
    <section id="services">
        <h2 class="section-title"><i class="fas fa-cogs" style="color:#1f4f8a;"></i> OUR SERVICES</h2>
        <p class="section-sub">Snap Planet offers a curated suite of digital services crafted for excellence and ease of use.</p>
        <div class="service-grid">
            <div class="service-card"><i class="fas fa-cloud-upload-alt"></i><h4>Cloud Sync</h4></div>
            <div class="service-card"><i class="fas fa-chart-line"></i><h4>Analytics Hub</h4></div>
            <div class="service-card"><i class="fas fa-shield-alt"></i><h4>Secure Access</h4></div>
            <div class="service-card"><i class="fas fa-robot"></i><h4>AI Assist</h4></div>
            <div class="service-card"><i class="fas fa-code"></i><h4>API Suite</h4></div>
            <div class="service-card"><i class="fas fa-mobile-alt"></i><h4>Mobile Ready</h4></div>
        </div>
    </section>

    <!-- CTA 1 -->
    <section>
        <div class="cta-block">
            <h2>Ready to elevate your digital journey?</h2>
            <p>Join thousands who trust Snap Planet for smarter workflows and seamless experiences. Your next step starts here.</p>
            <a href="#" class="btn-primary" style="margin-top:16px;"><i class="fas fa-arrow-right"></i> Explore Snap Planet</a>
        </div>
    </section>

    <!-- Why choose -->
    <section>
        <h2 class="section-title">Why Choose Snap Planet ?</h2>
        <div class="points-grid">
            <div class="point-item"><i class="fas fa-check-circle"></i> Intuitive & user-first design</div>
            <div class="point-item"><i class="fas fa-check-circle"></i> Real-time performance insights</div>
            <div class="point-item"><i class="fas fa-check-circle"></i> Seamless third-party integrations</div>
            <div class="point-item"><i class="fas fa-check-circle"></i> Enterprise-grade security</div>
            <div class="point-item"><i class="fas fa-check-circle"></i> 24/7 dedicated support</div>
            <div class="point-item"><i class="fas fa-check-circle"></i> Scalable for teams of any size</div>
        </div>
    </section>

    <!-- Reviews -->
    <section>
        <h2 class="section-title">What Client Says About Snap Planet</h2>
        <div class="review-grid">
            <div class="review-card"><img src="https://i.pravatar.cc/100?img=11" alt="client" /><div class="name">Amara</div><div class="quote">Snap Planet transformed our workflow</div></div>
            <div class="review-card"><img src="https://i.pravatar.cc/100?img=12" alt="client" /><div class="name">James</div><div class="quote">Incredible speed & reliability</div></div>
            <div class="review-card"><img src="https://i.pravatar.cc/100?img=13" alt="client" /><div class="name">Lin</div><div class="quote">Best platform for data insights</div></div>
            <div class="review-card"><img src="https://i.pravatar.cc/100?img=14" alt="client" /><div class="name">Carlos</div><div class="quote">The API suite is a game changer</div></div>
            <div class="review-card"><img src="https://i.pravatar.cc/100?img=15" alt="client" /><div class="name">Sophie</div><div class="quote">Support team is outstanding</div></div>
            <div class="review-card"><img src="https://i.pravatar.cc/100?img=16" alt="client" /><div class="name">Ahmed</div><div class="quote">Snap Planet keeps us ahead</div></div>
        </div>
    </section>

    <!-- Service Areas -->
    <section id="areas">
        <h2 class="section-title">Our Service Areas</h2>
        <div class="area-tags">
            <span class="area-tag"><i class="fas fa-globe-americas"></i> North America</span>
            <span class="area-tag"><i class="fas fa-globe-europe"></i> Europe</span>
            <span class="area-tag"><i class="fas fa-globe-asia"></i> Asia Pacific</span>
            <span class="area-tag"><i class="fas fa-globe"></i> Latin America</span>
            <span class="area-tag"><i class="fas fa-globe-africa"></i> Middle East & Africa</span>
            <span class="area-tag"><i class="fas fa-globe"></i> Global (Online)</span>
        </div>
    </section>

    <!-- FAQ -->
    <section>
        <h2 class="section-title">Frequently Asked Questions (FAQs)</h2>
        <div class="faq-list">
            <div class="faq-item"><h4>What is Snap Planet?</h4><p>Snap Planet is a digital platform offering tools for analytics, automation, and seamless integration.</p></div>
            <div class="faq-item"><h4>Is Snap Planet free to use?</h4><p>We offer both free and premium tiers with scalable features for individuals and teams.</p></div>
            <div class="faq-item"><h4>Can I integrate my existing tools?</h4><p>Yes, Snap Planet supports REST APIs and popular third-party services.</p></div>
            <div class="faq-item"><h4>How secure is Snap Planet?</h4><p>We use end-to-end encryption and follow enterprise-grade security protocols.</p></div>
            <div class="faq-item"><h4>Does Snap Planet offer mobile support?</h4><p>Absolutely, our platform is fully responsive and mobile-optimized.</p></div>
            <div class="faq-item"><h4>How do I get started?</h4><p>Simply sign up and explore our dashboard – no credit card required for the trial.</p></div>
        </div>
    </section>

    <!-- Contact -->
    <section id="contact">
        <h2 class="section-title">Contact Us</h2>
        <div class="contact-wrap">
            <div class="contact-social">
                <p>Connect with us on social media for updates and support.</p>
                <div class="social-icons">
                    <a href="#"><i class="fab fa-twitter"></i></a>
                    <a href="#"><i class="fab fa-linkedin-in"></i></a>
                    <a href="#"><i class="fab fa-github"></i></a>
                    <a href="#"><i class="fab fa-youtube"></i></a>
                </div>
                <div style="margin-top:20px;"><i class="fas fa-envelope" style="color:#1f4f8a;"></i> hello@snapplanets.app</div>
            </div>
            <div class="contact-map">
                <i class="fas fa-map-pin"></i> <span>San Francisco, CA (Global HQ)</span>
            </div>
        </div>
    </section>

    <!-- final CTA -->
    <section>
        <div class="cta-block">
            <h2>Join the Snap Planet community today</h2>
            <p>Experience the future of digital tools. Start your free trial and see what Snap Planet can do for you.</p>
            <a href="#" class="btn-primary"><i class="fas fa-play"></i> Get Started Free</a>
        </div>
    </section>
</main>

<!-- Footer -->
<footer>
    <div class="container">
        <div class="footer-grid">
            <div class="footer-col">
                <img src="https://snapplanets.app/wp-content/uploads/2026/07/ChatGPT-Image-Jul-25-2026-03_34_31-PM-e1784975819276.png" alt="logo" style="height:44px; border-radius:8px;" />
                <p style="margin-top:12px;">Snap Planet – innovation at your fingertips.</p>
            </div>
            <div class="footer-col">
                <h5>Quick Links</h5>
                <a href="#">Home</a>
                <a href="#services">Services</a>
                <a href="#about">About</a>
                <a href="#contact">Contact</a>
            </div>
            <div class="footer-col">
                <h5>Services</h5>
                <a href="#">Cloud Sync</a>
                <a href="#">Analytics</a>
                <a href="#">AI Assist</a>
                <a href="#">API Suite</a>
            </div>
            <div class="footer-col">
                <h5>Support</h5>
                <a href="#">Help Center</a>
                <a href="#">Community</a>
                <a href="#">Privacy</a>
            </div>
        </div>
        <div class="footer-bottom">
            Snap Planet © 2025-2026 All Rights Reserved
        </div>
    </div>
</footer>

</body>
</html>
