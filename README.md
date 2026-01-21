<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Shakir Sakariye | Portfolio</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&family=Raleway:wght@800&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #6C63FF;
            --primary-dark: #554fd8;
            --secondary: #FF6584;
            --dark: #1a1a2e;
            --darker: #16213e;
            --light: #f8f9fa;
            --gray: #6c757d;
            --light-gray: #e9ecef;
            --transition: all 0.3s ease;
            --shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            --border-radius: 12px;
        }

        .dark-mode {
            --dark: #f8f9fa;
            --darker: #e9ecef;
            --light: #1a1a2e;
            --light-gray: #16213e;
            --gray: #adb5bd;
            --shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: 'Poppins', sans-serif;
            background-color: var(--light);
            color: var(--dark);
            line-height: 1.6;
            transition: var(--transition);
            overflow-x: hidden;
        }

        h1, h2, h3, h4 {
            font-weight: 700;
            line-height: 1.2;
        }

        h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
        }

        h2 {
            font-size: 2.5rem;
            margin-bottom: 2rem;
            position: relative;
            display: inline-block;
        }

        h2:after {
            content: '';
            position: absolute;
            left: 0;
            bottom: -10px;
            width: 70px;
            height: 4px;
            background: var(--primary);
            border-radius: 2px;
        }

        h3 {
            font-size: 1.5rem;
            margin-bottom: 1rem;
        }

        p {
            margin-bottom: 1.5rem;
            color: var(--gray);
        }

        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        section {
            padding: 100px 0;
        }

        .btn {
            display: inline-block;
            padding: 14px 32px;
            background-color: var(--primary);
            color: white;
            border: none;
            border-radius: var(--border-radius);
            font-weight: 600;
            text-decoration: none;
            cursor: pointer;
            transition: var(--transition);
            font-size: 1rem;
            box-shadow: var(--shadow);
        }

        .btn:hover {
            background-color: var(--primary-dark);
            transform: translateY(-3px);
            box-shadow: 0 15px 30px rgba(108, 99, 255, 0.2);
        }

        .btn-secondary {
            background-color: transparent;
            border: 2px solid var(--primary);
            color: var(--primary);
        }

        .btn-secondary:hover {
            background-color: var(--primary);
            color: white;
        }

        /* Header & Navigation */
        header {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            z-index: 1000;
            padding: 20px 0;
            background-color: rgba(255, 255, 255, 0.95);
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.05);
            transition: var(--transition);
        }

        .dark-mode header {
            background-color: rgba(26, 26, 46, 0.95);
        }

        header.scrolled {
            padding: 15px 0;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
        }

        .nav-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-family: 'Raleway', sans-serif;
            font-size: 1.8rem;
            font-weight: 800;
            color: var(--primary);
            text-decoration: none;
        }

        .logo span {
            color: var(--secondary);
        }

        .nav-links {
            display: flex;
            list-style: none;
        }

        .nav-links li {
            margin-left: 30px;
        }

        .nav-links a {
            color: var(--dark);
            text-decoration: none;
            font-weight: 500;
            transition: var(--transition);
            position: relative;
        }

        .dark-mode .nav-links a {
            color: var(--light);
        }

        .nav-links a:hover {
            color: var(--primary);
        }

        .nav-links a:after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            background: var(--primary);
            left: 0;
            bottom: -5px;
            transition: var(--transition);
        }

        .nav-links a:hover:after {
            width: 100%;
        }

        .theme-toggle {
            background: none;
            border: none;
            font-size: 1.5rem;
            color: var(--dark);
            cursor: pointer;
            margin-left: 30px;
            transition: var(--transition);
        }

        .dark-mode .theme-toggle {
            color: var(--light);
        }

        .theme-toggle:hover {
            color: var(--primary);
            transform: rotate(30deg);
        }

        .mobile-toggle {
            display: none;
            font-size: 1.5rem;
            background: none;
            border: none;
            color: var(--dark);
            cursor: pointer;
        }

        .dark-mode .mobile-toggle {
            color: var(--light);
        }

        /* Hero Section */
        .hero {
            padding-top: 180px;
            min-height: 100vh;
            display: flex;
            align-items: center;
            position: relative;
            overflow: hidden;
        }

        .hero-content {
            max-width: 600px;
            z-index: 2;
            position: relative;
        }

        .hero h1 {
            animation: fadeUp 1s ease;
        }

        .hero p {
            font-size: 1.2rem;
            margin-bottom: 2rem;
            animation: fadeUp 1s ease 0.2s both;
        }

        .hero-btns {
            display: flex;
            gap: 15px;
            animation: fadeUp 1s ease 0.4s both;
        }

        .hero-image {
            position: absolute;
            right: 0;
            top: 50%;
            transform: translateY(-50%);
            width: 45%;
            height: 70%;
            border-radius: 30% 70% 70% 30% / 30% 30% 70% 70%;
            overflow: hidden;
            animation: morphing 15s infinite;
            box-shadow: var(--shadow);
            z-index: 1;
        }

        .hero-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            object-position: center;
            transition: var(--transition);
        }

        .hero-image::after {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(45deg, rgba(108, 99, 255, 0.1), rgba(255, 101, 132, 0.1));
            mix-blend-mode: multiply;
            border-radius: inherit;
        }

        .hero-image:hover img {
            transform: scale(1.05);
        }

        /* About Section */
        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 60px;
            align-items: center;
        }

        .about-text h2 {
            margin-bottom: 1.5rem;
        }

        .skills {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-top: 30px;
        }

        .skill {
            background-color: var(--light-gray);
            padding: 10px 20px;
            border-radius: 50px;
            font-weight: 500;
            transition: var(--transition);
            color: var(--dark);
        }

        .dark-mode .skill {
            background-color: var(--darker);
        }

        .skill:hover {
            background-color: var(--primary);
            color: white;
            transform: translateY(-5px);
        }

        /* Portfolio Section */
        .portfolio {
            background-color: var(--light-gray);
        }

        .dark-mode .portfolio {
            background-color: var(--darker);
        }

        .portfolio-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
            gap: 30px;
        }

        .portfolio-item {
            background-color: var(--light);
            border-radius: var(--border-radius);
            overflow: hidden;
            box-shadow: var(--shadow);
            transition: var(--transition);
        }

        .portfolio-item:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.1);
        }

        .portfolio-img {
            height: 200px;
            width: 100%;
            background-color: var(--primary);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 3rem;
        }

        .portfolio-content {
            padding: 25px;
        }

        /* Contact Section */
        .contact-container {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 60px;
        }

        .contact-info {
            display: flex;
            flex-direction: column;
            gap: 25px;
        }

        .contact-item {
            display: flex;
            align-items: center;
            gap: 15px;
        }

        .contact-icon {
            width: 50px;
            height: 50px;
            background-color: var(--primary);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 1.2rem;
        }

        .contact-form input,
        .contact-form textarea {
            width: 100%;
            padding: 15px;
            margin-bottom: 20px;
            border: 1px solid var(--light-gray);
            border-radius: var(--border-radius);
            font-family: 'Poppins', sans-serif;
            background-color: var(--light-gray);
            color: var(--dark);
            transition: var(--transition);
        }

        .dark-mode .contact-form input,
        .dark-mode .contact-form textarea {
            background-color: var(--darker);
            border-color: var(--darker);
        }

        .contact-form input:focus,
        .contact-form textarea:focus {
            outline: none;
            border-color: var(--primary);
        }

        /* Footer */
        footer {
            background-color: var(--dark);
            color: var(--light);
            padding: 60px 0 30px;
            text-align: center;
        }

        .dark-mode footer {
            background-color: var(--darker);
        }

        .footer-content {
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        .social-links {
            display: flex;
            gap: 20px;
            margin: 30px 0;
        }

        .social-links a {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 45px;
            height: 45px;
            background-color: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            color: white;
            font-size: 1.2rem;
            transition: var(--transition);
        }

        .social-links a:hover {
            background-color: var(--primary);
            transform: translateY(-5px);
        }

        .copyright {
            margin-top: 30px;
            padding-top: 20px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: var(--gray);
            font-size: 0.9rem;
        }

        /* Animations */
        @keyframes fadeUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes morphing {
            0% {
                border-radius: 30% 70% 70% 30% / 30% 30% 70% 70%;
            }
            25% {
                border-radius: 58% 42% 75% 25% / 76% 46% 54% 24%;
            }
            50% {
                border-radius: 50% 50% 33% 67% / 55% 27% 73% 45%;
            }
            75% {
                border-radius: 33% 67% 58% 42% / 63% 68% 32% 37%;
            }
            100% {
                border-radius: 30% 70% 70% 30% / 30% 30% 70% 70%;
            }
        }

        /* Responsive Design */
        @media (max-width: 992px) {
            h1 {
                font-size: 2.8rem;
            }
            
            h2 {
                font-size: 2.2rem;
            }
            
            .about-content,
            .contact-container {
                grid-template-columns: 1fr;
            }
            
            .hero-image {
                width: 50%;
                height: 50%;
                opacity: 0.8;
            }
        }

        @media (max-width: 768px) {
            .nav-links {
                position: fixed;
                top: 80px;
                left: 0;
                width: 100%;
                background-color: var(--light);
                flex-direction: column;
                align-items: center;
                padding: 20px 0;
                box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
                transform: translateY(-100%);
                opacity: 0;
                transition: var(--transition);
                z-index: 999;
            }
            
            .dark-mode .nav-links {
                background-color: var(--darker);
            }
            
            .nav-links.active {
                transform: translateY(0);
                opacity: 1;
            }
            
            .nav-links li {
                margin: 15px 0;
            }
            
            .mobile-toggle {
                display: block;
            }
            
            .theme-toggle {
                margin-left: 20px;
            }
            
            .hero {
                padding-top: 150px;
            }
            
            .hero-image {
                display: none;
            }
            
            .portfolio-grid {
                grid-template-columns: 1fr;
            }
        }

        @media (max-width: 576px) {
            h1 {
                font-size: 2.2rem;
            }
            
            h2 {
                font-size: 1.8rem;
            }
            
            section {
                padding: 70px 0;
            }
            
            .hero-btns {
                flex-direction: column;
                align-items: flex-start;
            }
        }
    </style>
</head>
<body>
    <!-- Header & Navigation -->
    <header id="header">
        <div class="container nav-container">
            <a href="#" class="logo">Shakir<span>Sakariye</span></a>
            
            <button class="mobile-toggle" id="mobileToggle">
                <i class="fas fa-bars"></i>
            </button>
            
            <ul class="nav-links" id="navLinks">
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#portfolio">Portfolio</a></li>
                <li><a href="#contact">Contact</a></li>
                <li>
                    <button class="theme-toggle" id="themeToggle">
                        <i class="fas fa-moon"></i>
                    </button>
                </li>
            </ul>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="container">
            <div class="hero-content">
                <h1>Hi, I'm <span style="color: var(--primary);">Shakir Sakariye</span></h1>
                <h2>Advanced Web Developer</h2>
                <p>I create innovative, responsive, and high-performance web applications with modern technologies. Passionate about clean code, user experience, and solving complex problems through technology.</p>
                <div class="hero-btns">
                    <a href="#portfolio" class="btn">View My Work</a>
                    <a href="#contact" class="btn btn-secondary">Contact Me</a>
                </div>
            </div>
            <div class="hero-image">
                <!-- IMPORTANT: Follow these steps for the image to work properly:
                     1. Create a folder named "images" in the same directory as this HTML file
                     2. Copy your photo into that folder
                     3. Rename the photo to something simple like "profile.jpg"
                     4. Use the path below: -->
                <img src="https://scontent.fhga1-1.fna.fbcdn.net/v/t39.30808-6/618102310_1538403388291692_9150262615773696089_n.jpg?stp=dst-jpg_s590x590_tt6&_nc_cat=104&ccb=1-7&_nc_sid=127cfc&_nc_ohc=DVyqUtHK8sYQ7kNvwEYZ3cr&_nc_oc=AdlDtCDQS158Q0Uyw45ls_OZe9uxEi5k-8dOJCxaSiWgSpe9kCMqvZPLm3tVNIumM4E&_nc_zt=23&_nc_ht=scontent.fhga1-1.fna&_nc_gid=0CQRey-g8NNXIm21DozdiA&oh=00_AfrpadA0EA1WGSMZmT9Tn_GPg5Jrdy2TfcNkCYyP1Dl0gg&oe=69767195" alt="Shakir Sakariye - Web Developer">
                
               
        </div>
    </section>

    <!-- About Section -->
    <section id="about">
        <div class="container">
            <h2>About Me</h2>
            <div class="about-content">
                <div class="about-text">
                    <p>I'm a passionate web developer with 5+ years of experience building advanced web applications. My expertise includes React, Node.js, Python, and modern frontend frameworks.</p>
                    <p>I specialize in creating responsive, accessible, and performant web solutions that deliver exceptional user experiences. I'm constantly learning and adapting to new technologies to stay at the forefront of web development.</p>
                    <div class="skills">
                        <div class="skill">HTML/CSS</div>
                        <div class="skill">JavaScript</div>
                        <div class="skill">React</div>
                        <div class="skill">Node.js</div>
                        <div class="skill">Python</div>
                        <div class="skill">MongoDB</div>
                        <div class="skill">UI/UX Design</div>
                        <div class="skill">Responsive Design</div>
                    </div>
                </div>
                <div class="about-stats">
                    <h3>My Experience</h3>
                    <p>I've worked on a variety of projects ranging from small business websites to large-scale enterprise applications. My approach combines technical expertise with creative problem-solving.</p>
                    <div style="margin-top: 30px;">
                        <a href="#" class="btn"><i class="fas fa-download"></i> Download CV</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Portfolio Section -->
    <section class="portfolio" id="portfolio">
        <div class="container">
            <h2>My Portfolio</h2>
            <div class="portfolio-grid">
                <div class="portfolio-item">
                    <div class="portfolio-img" style="background: linear-gradient(45deg, #6C63FF, #36D1DC);">
                        <i class="fas fa-shopping-cart"></i>
                    </div>
                    <div class="portfolio-content">
                        <h3>E-Commerce Platform</h3>
                        <p>Full-featured online shopping platform with payment integration, user dashboard, and admin panel.</p>
                        <a href="#" class="btn btn-secondary" style="margin-top: 10px;">View Details</a>
                    </div>
                </div>
                <div class="portfolio-item">
                    <div class="portfolio-img" style="background: linear-gradient(45deg, #FF6584, #FFB347);">
                        <i class="fas fa-chart-line"></i>
                    </div>
                    <div class="portfolio-content">
                        <h3>Data Analytics Dashboard</h3>
                        <p>Interactive dashboard for visualizing complex data with real-time updates and customizable widgets.</p>
                        <a href="#" class="btn btn-secondary" style="margin-top: 10px;">View Details</a>
                    </div>
                </div>
                <div class="portfolio-item">
                    <div class="portfolio-img" style="background: linear-gradient(45deg, #20bf55, #01baef);">
                        <i class="fas fa-mobile-alt"></i>
                    </div>
                    <div class="portfolio-content">
                        <h3>Travel Mobile App</h3>
                        <p>Cross-platform mobile application for travel planning with itinerary management and booking features.</p>
                        <a href="#" class="btn btn-secondary" style="margin-top: 10px;">View Details</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact">
        <div class="container">
            <h2>Get In Touch</h2>
            <div class="contact-container">
                <div class="contact-info">
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-envelope"></i>
                        </div>
                        <div>
                            <h3>Email</h3>
                            <p>shaakirsakariye195@gmail.com</p>
                        </div>
                    </div>
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-phone"></i>
                        </div>
                        <div>
                            <h3>Phone</h3>
                            <p>+252 634998296</p>
                        </div>
                    </div>
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-map-marker-alt"></i>
                        </div>
                        <div>
                            <h3>Location</h3>
                            <p>Hargeisa, Somaliland</p>
                        </div>
                    </div>
                </div>
                <div class="contact-form">
                    <form id="contactForm">
                        <input type="text" placeholder="Your Name" required>
                        <input type="email" placeholder="Your Email" required>
                        <input type="text" placeholder="Subject" required>
                        <textarea rows="5" placeholder="Your Message" required></textarea>
                        <button type="submit" class="btn">Send Message</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <a href="#" class="logo" style="color: white; margin-bottom: 20px;">Shakir<span>Sakariye</span></a>
                <p style="color: rgba(255,255,255,0.7); max-width: 500px;">Advanced web developer passionate about creating innovative digital solutions that make a difference.</p>
                <div class="social-links">
                    <a href="https://github.com/shaakirSakariye"><i class="fab fa-github"></i></a>
                    <a href="#"><i class="fab fa-linkedin-in"></i></a>
                    <a href="#"><i class="fab fa-twitter"></i></a>
                    <a href="#"><i class="fab fa-codepen"></i></a>
                </div>
                <div class="copyright">
                    &copy; 2026 Shakir Sakariye. All Rights Reserved.
                </div>
            </div>
        </div>
    </footer>

    <script>
        // Dark/Light Mode Toggle
        const themeToggle = document.getElementById('themeToggle');
        const themeIcon = themeToggle.querySelector('i');
        
        themeToggle.addEventListener('click', () => {
            document.body.classList.toggle('dark-mode');
            
            if (document.body.classList.contains('dark-mode')) {
                themeIcon.classList.remove('fa-moon');
                themeIcon.classList.add('fa-sun');
                localStorage.setItem('theme', 'dark');
            } else {
                themeIcon.classList.remove('fa-sun');
                themeIcon.classList.add('fa-moon');
                localStorage.setItem('theme', 'light');
            }
        });
        
        // Check for saved theme preference
        if (localStorage.getItem('theme') === 'dark') {
            document.body.classList.add('dark-mode');
            themeIcon.classList.remove('fa-moon');
            themeIcon.classList.add('fa-sun');
        }
        
        // Mobile Navigation Toggle
        const mobileToggle = document.getElementById('mobileToggle');
        const navLinks = document.getElementById('navLinks');
        
        mobileToggle.addEventListener('click', () => {
            navLinks.classList.toggle('active');
            mobileToggle.innerHTML = navLinks.classList.contains('active') 
                ? '<i class="fas fa-times"></i>' 
                : '<i class="fas fa-bars"></i>';
        });
        
        // Close mobile menu when clicking a link
        document.querySelectorAll('.nav-links a').forEach(link => {
            link.addEventListener('click', () => {
                navLinks.classList.remove('active');
                mobileToggle.innerHTML = '<i class="fas fa-bars"></i>';
            });
        });
        
        // Header scroll effect
        window.addEventListener('scroll', () => {
            const header = document.getElementById('header');
            if (window.scrollY > 50) {
                header.classList.add('scrolled');
            } else {
                header.classList.remove('scrolled');
            }
        });
        
        // Contact form submission
        const contactForm = document.getElementById('contactForm');
        contactForm.addEventListener('submit', (e) => {
            e.preventDefault();
            alert('Thank you for your message! I will get back to you soon.');
            contactForm.reset();
        });
        
        // Smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                if (targetId === '#') return;
                
                const targetElement = document.querySelector(targetId);
                if (targetElement) {
                    window.scrollTo({
                        top: targetElement.offsetTop - 80,
                        behavior: 'smooth'
                    });
                }
            });
        });
        
        // Animate elements on scroll
        const animateOnScroll = () => {
            const elements = document.querySelectorAll('.portfolio-item, .about-text, .contact-info');
            
            elements.forEach(element => {
                const elementPosition = element.getBoundingClientRect().top;
                const screenPosition = window.innerHeight / 1.2;
                
                if (elementPosition < screenPosition) {
                    element.style.opacity = '1';
                    element.style.transform = 'translateY(0)';
                }
            });
        };
        
        // Set initial state for animated elements
        document.querySelectorAll('.portfolio-item, .about-text, .contact-info').forEach(el => {
            el.style.opacity = '0';
            el.style.transform = 'translateY(30px)';
            el.style.transition = 'opacity 0.5s ease, transform 0.5s ease';
        });
        
        window.addEventListener('scroll', animateOnScroll);
        window.addEventListener('load', animateOnScroll);
    </script>
</body>
</html>
