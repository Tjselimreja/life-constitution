<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Selim Reja - Deep Learning & Entrepreneur</title>
    <meta name="description" content="Selim Reja - Deep Learning Enthusiast, Entrepreneur & CEO at Codarithm">
    
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --bg-primary: #0a0a0a;
            --bg-secondary: #1a1a1a;
            --text-primary: #ffffff;
            --text-secondary: #a0a0a0;
            --accent: #3b82f6;
            --accent-hover: #2563eb;
            --border: #2a2a2a;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
            background: var(--bg-primary);
            color: var(--text-primary);
            line-height: 1.6;
            overflow-x: hidden;
        }

        /* Navigation */
        nav {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(10, 10, 10, 0.95);
            backdrop-filter: blur(10px);
            padding: 1.5rem 0;
            z-index: 1000;
            border-bottom: 1px solid var(--border);
        }

        nav .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        nav .logo {
            font-size: 1.5rem;
            font-weight: 700;
            color: var(--text-primary);
            text-decoration: none;
        }

        nav ul {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        nav a {
            color: var(--text-secondary);
            text-decoration: none;
            transition: color 0.3s;
            font-weight: 500;
        }

        nav a:hover {
            color: var(--accent);
        }

        /* Hero Section */
        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 6rem 2rem 2rem;
            position: relative;
        }

        .hero-content {
            max-width: 1200px;
            text-align: center;
        }

        .hero h1 {
            font-size: clamp(2.5rem, 8vw, 5rem);
            font-weight: 800;
            margin-bottom: 1rem;
            background: linear-gradient(135deg, #fff 0%, #a0a0a0 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .hero .subtitle {
            font-size: clamp(1.2rem, 3vw, 1.8rem);
            color: var(--accent);
            margin-bottom: 1.5rem;
            font-weight: 600;
        }

        .hero p {
            font-size: 1.2rem;
            color: var(--text-secondary);
            max-width: 700px;
            margin: 0 auto 2rem;
        }

        .social-links {
            display: flex;
            gap: 1.5rem;
            justify-content: center;
            margin: 2rem 0;
        }

        .social-links a {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background: var(--bg-secondary);
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--text-primary);
            text-decoration: none;
            font-size: 1.5rem;
            transition: all 0.3s;
            border: 1px solid var(--border);
        }

        .social-links a:hover {
            background: var(--accent);
            transform: translateY(-5px);
            box-shadow: 0 10px 30px rgba(59, 130, 246, 0.3);
        }

        .cta-btn {
            display: inline-block;
            padding: 1rem 2.5rem;
            background: var(--accent);
            color: white;
            text-decoration: none;
            border-radius: 8px;
            font-weight: 600;
            transition: all 0.3s;
            margin-top: 1rem;
        }

        .cta-btn:hover {
            background: var(--accent-hover);
            transform: translateY(-2px);
            box-shadow: 0 10px 30px rgba(59, 130, 246, 0.4);
        }

        /* Section Styles */
        section {
            padding: 6rem 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .section-title {
            font-size: 2.5rem;
            font-weight: 700;
            margin-bottom: 3rem;
            text-align: center;
        }

        /* About Section */
        .about-content {
            display: grid;
            grid-template-columns: 1fr 2fr;
            gap: 4rem;
            align-items: start;
        }

        .profile-img {
            width: 100%;
            border-radius: 16px;
            border: 3px solid var(--border);
        }

        .about-text {
            font-size: 1.1rem;
            color: var(--text-secondary);
            line-height: 1.8;
        }

        .info-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 1.5rem;
            margin: 2rem 0;
        }

        .info-item {
            padding: 1rem;
            background: var(--bg-secondary);
            border-radius: 8px;
            border: 1px solid var(--border);
        }

        .info-item strong {
            color: var(--accent);
            display: block;
            margin-bottom: 0.5rem;
        }

        /* Skills Section */
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: 2rem;
            margin-top: 2rem;
        }

        .skill-card {
            background: var(--bg-secondary);
            padding: 2rem;
            border-radius: 12px;
            text-align: center;
            border: 1px solid var(--border);
            transition: all 0.3s;
        }

        .skill-card:hover {
            transform: translateY(-5px);
            border-color: var(--accent);
            box-shadow: 0 10px 30px rgba(59, 130, 246, 0.2);
        }

        .skill-card h3 {
            margin-top: 1rem;
            font-size: 1.2rem;
        }

        /* Experience Section */
        .experience-item {
            background: var(--bg-secondary);
            padding: 2rem;
            border-radius: 12px;
            margin-bottom: 2rem;
            border-left: 4px solid var(--accent);
            border: 1px solid var(--border);
        }

        .experience-item h3 {
            font-size: 1.5rem;
            margin-bottom: 0.5rem;
        }

        .experience-item .company {
            color: var(--accent);
            font-weight: 600;
            margin-bottom: 1rem;
        }

        .experience-item ul {
            margin-left: 1.5rem;
            color: var(--text-secondary);
        }

        .experience-item li {
            margin-bottom: 0.5rem;
        }

        /* Projects Section */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .project-card {
            background: var(--bg-secondary);
            border-radius: 12px;
            overflow: hidden;
            border: 1px solid var(--border);
            transition: all 0.3s;
        }

        .project-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 40px rgba(0, 0, 0, 0.5);
        }

        .project-img {
            width: 100%;
            height: 200px;
            background: linear-gradient(135deg, var(--accent) 0%, #1e40af 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 3rem;
        }

        .project-content {
            padding: 2rem;
        }

        .project-content h3 {
            font-size: 1.5rem;
            margin-bottom: 1rem;
        }

        .project-content p {
            color: var(--text-secondary);
            margin-bottom: 1.5rem;
        }

        .project-links {
            display: flex;
            gap: 1rem;
        }

        .project-links a {
            padding: 0.5rem 1.5rem;
            background: var(--accent);
            color: white;
            text-decoration: none;
            border-radius: 6px;
            font-size: 0.9rem;
            transition: all 0.3s;
        }

        .project-links a:hover {
            background: var(--accent-hover);
        }

        /* Contact Section */
        .contact-content {
            text-align: center;
            max-width: 600px;
            margin: 0 auto;
        }

        .contact-content p {
            font-size: 1.2rem;
            color: var(--text-secondary);
            margin-bottom: 2rem;
        }

        /* Footer */
        footer {
            background: var(--bg-secondary);
            padding: 3rem 2rem;
            text-align: center;
            border-top: 1px solid var(--border);
        }

        footer p {
            color: var(--text-secondary);
        }

        /* Responsive */
        @media (max-width: 768px) {
            nav ul {
                display: none;
            }

            .about-content {
                grid-template-columns: 1fr;
            }

            .info-grid {
                grid-template-columns: 1fr;
            }

            .projects-grid {
                grid-template-columns: 1fr;
            }
        }

        /* Scroll Animations */
        .fade-in {
            opacity: 0;
            transform: translateY(30px);
            animation: fadeIn 0.8s ease forwards;
        }

        @keyframes fadeIn {
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
    </style>
</head>
<body>
    <!-- Navigation -->
    <nav>
        <div class="container">
            <a href="#" class="logo">SR</a>
            <ul>
                <li><a href="#about">About</a></li>
                <li><a href="#skills">Skills</a></li>
                <li><a href="#experience">Experience</a></li>
                <li><a href="#projects">Projects</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </div>
    </nav>

    <!-- Hero Section -->
    <section class="hero">
        <div class="hero-content">
            <h1>Selim Reja</h1>
            <p class="subtitle">Deep Learning Enthusiast & Entrepreneur</p>
            <p>Bangladesh কে ভালোবাসি এবং এই দেশকে ভালো পর্যায়ে নিয়ে যেতে চাই। Building new ecosystem for Bangladesh's tech future.</p>
            
            <div class="social-links">
                <a href="https://github.com/Tjselimreja" target="_blank" title="GitHub">
                    <svg width="24" height="24" fill="currentColor" viewBox="0 0 24 24"><path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"/></svg>
                </a>
                <a href="https://www.linkedin.com/in/selim-reja-801b732a6/" target="_blank" title="LinkedIn">
                    <svg width="24" height="24" fill="currentColor" viewBox="0 0 24 24"><path d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z"/></svg>
                </a>
                <a href="https://x.com/tjselimreja" target="_blank" title="Twitter/X">
                    <svg width="24" height="24" fill="currentColor" viewBox="0 0 24 24"><path d="M18.244 2.25h3.308l-7.227 8.26 8.502 11.24H16.17l-5.214-6.817L4.99 21.75H1.68l7.73-8.835L1.254 2.25H8.08l4.713 6.231zm-1.161 17.52h1.833L7.084 4.126H5.117z"/></svg>
                </a>
                <a href="https://www.facebook.com/tjselimreja/" target="_blank" title="Facebook">
                    <svg width="24" height="24" fill="currentColor" viewBox="0 0 24 24"><path d="M9 8h-3v4h3v12h5v-12h3.642l.358-4h-4v-1.667c0-.955.192-1.333 1.115-1.333h2.885v-5h-3.808c-3.596 0-5.192 1.583-5.192 4.615v3.385z"/></svg>
                </a>
                <a href="mailto:tjselimreja@gmail.com" title="Email">
                    <svg width="24" height="24" fill="currentColor" viewBox="0 0 24 24"><path d="M0 3v18h24v-18h-24zm6.623 7.929l-4.623 5.712v-9.458l4.623 3.746zm-4.141-5.929h19.035l-9.517 7.713-9.518-7.713zm5.694 7.188l3.824 3.099 3.83-3.104 5.612 6.817h-18.779l5.513-6.812zm9.208-1.264l4.616-3.741v9.348l-4.616-5.607z"/></svg>
                </a>
            </div>

            <a href="#contact" class="cta-btn">Get In Touch</a>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="fade-in">
        <h2 class="section-title">About Me</h2>
        <div class="about-content">
            <div>
                <img src="https://via.placeholder.com/400x500/1a1a1a/3b82f6?text=Your+Photo" alt="Selim Reja" class="profile-img">
            </div>
            <div>
                <p class="about-text">
                    আমি একজন Deep Learning enthusiast এবং entrepreneur যে নতুন ecosystem তৈরি করছি Bangladesh এর জন্য। 
                    আমি Notion expert এবং business এর সাথে জড়িত। বর্তমানে Codarithm.com এর CEO হিসেবে কাজ করছি 
                    এবং নতুন technology শিখছি।
                </p>
                <div class="info-grid">
                    <div class="info-item">
                        <strong>Email</strong>
                        <span>tjselimreja@gmail.com</span>
                    </div>
                    <div class="info-item">
                        <strong>Location</strong>
                        <span>Keraniganj, Dhaka, Bangladesh</span>
                    </div>
                    <div class="info-item">
                        <strong>Role</strong>
                        <span>CEO at Codarithm</span>
                    </div>
                    <div class="info-item">
                        <strong>Focus</strong>
                        <span>Deep Learning & Business</span>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Skills Section -->
    <section id="skills" class="fade-in">
        <h2 class="section-title">Skills & Expertise</h2>
        <div class="skills-grid">
            <div class="skill-card">
                <div style="font-size: 3rem;">🧠</div>
                <h3>Deep Learning</h3>
            </div>
            <div class="skill-card">
                <div style="font-size: 3rem;">🤖</div>
                <h3>AI/ML</h3>
            </div>
            <div class="skill-card">
                <div style="font-size: 3rem;">📝</div>
                <h3>Notion Expert</h3>
            </div>
            <div class="skill-card">
                <div style="font-size: 3rem;">💼</div>
                <h3>Business</h3>
            </div>
            <div class="skill-card">
                <div style="font-size: 3rem;">🐍</div>
                <h3>Python</h3>
            </div>
            <div class="skill-card">
                <div style="font-size: 3rem;">🌐</div>
                <h3>Web Dev</h3>
            </div>
        </div>
    </section>

    <!-- Experience Section -->
    <section id="experience" class="fade-in">
        <h2 class="section-title">Experience</h2>
        <div class="experience-item">
            <h3>CEO & Founder</h3>
            <p class="company">Codarithm • Present</p>
            <ul>
                <li>Leading Codarithm.com as Chief Executive Officer</li>
                <li>Building new ecosystem for Bangladesh's tech industry</li>
                <li>Working on innovative solutions in AI and Deep Learning</li>
                <li>Managing business operations and strategic planning</li>
            </ul>
        </div>
        <div class="experience-item">
            <h3>Self-Taught Learner</h3>
            <p class="company">Independent Study • 2022 - Present</p>
            <ul>
                <li>Left traditional education to pursue entrepreneurship</li>
                <li>Focused on Deep Learning, AI, and Business</li>
                <li>Building projects and learning by doing</li>
            </ul>
        </div>
    </section>

    <!-- Projects Section -->
    <section id="projects" class="fade-in">
        <h2 class="section-title">Projects</h2>
        <div class="projects-grid">
            <div class="project-card">
                <div class="project-img">🚀</div>
                <div class="project-content">
                    <h3>Codarithm</h3>
                    <p>Building Bangladesh's tech ecosystem platform. A comprehensive solution for developers and entrepreneurs.</p>
                    <div class="project-links">
                        <a href="https://codarithm.com" target="_blank">Visit Site</a>
                    </div>
                </div>
            </div>
            <div class="project-card">
                <div class="project-img">🤖</div>
                <div class="project-content">
                    <h3>Project Orrin</h3>
                    <p>Small Language Model project exploring AI capabilities and natural language processing.</p>
                    <div class="project-links">
                        <a href="https://github.com/Tjselimreja" target="_blank">View Code</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="fade-in">
        <h2 class="section-title">Get In Touch</h2>
        <div class="contact-content">
            <p>আমি সবসময় নতুন ideas এবং collaboration এর জন্য open. Let's build something amazing together!</p>
            <a href="mailto:tjselimreja@gmail.com" class="cta-btn">Send Email</a>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="social-links">
            <a href="https://github.com/Tjselimreja" target="_blank">
                <svg width="24" height="24" fill="currentColor" viewBox="0 0 24 24"><path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"/></svg>
            </a>
            <a href="https://www.linkedin.com/in/selim-reja-801b732a6/" target="_blank">
                <svg width="24" height="24" fill="currentColor" viewBox="0 0 24 24"><path d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z"/></svg>
            </a>
        </div>
        <p style="margin-top: 2rem;">© 2024 Selim Reja. Building Bangladesh's Tech Future.</p>
    </footer>

    <script>
        // Smooth scrolling
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({ behavior: 'smooth' });
                }
            });
        });

        // Fade in animation on scroll
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = '1';
                    entry.target.style.transform = 'translateY(0)';
                }
            });
        });

        document.querySelectorAll('.fade-in').forEach(el => observer.observe(el));
    </script>
</body>
</html># life-constitution
