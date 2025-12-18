<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>TJ Selim Reja | Portfolio</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <!-- ===== CSS (Your upgraded style) ===== -->
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
      font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI',
        Roboto, Arial, sans-serif;
      background: var(--bg-primary);
      color: var(--text-primary);
      line-height: 1.6;
    }

    /* ===== NAV ===== */
    nav {
      position: fixed;
      top: 0;
      width: 100%;
      background: rgba(10, 10, 10, 0.95);
      backdrop-filter: blur(10px);
      padding: 1rem 0;
      border-bottom: 1px solid var(--border);
      z-index: 1000;
    }

    nav .container {
      max-width: 1200px;
      margin: auto;
      padding: 0 2rem;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    nav .logo {
      font-size: 1.4rem;
      font-weight: 700;
      color: white;
      text-decoration: none;
    }

    nav ul {
      display: flex;
      list-style: none;
      gap: 1.5rem;
    }

    nav a {
      color: var(--text-secondary);
      text-decoration: none;
      font-weight: 500;
    }

    nav a:hover {
      color: var(--accent);
    }

    /* ===== HERO ===== */
    .hero {
      min-height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      padding: 6rem 2rem 2rem;
      text-align: center;
    }

    .hero h1 {
      font-size: clamp(2.5rem, 8vw, 4.5rem);
      font-weight: 800;
      background: linear-gradient(135deg, #fff, #a0a0a0);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
    }

    .hero .subtitle {
      font-size: 1.5rem;
      color: var(--accent);
      margin: 1rem 0;
      font-weight: 600;
    }

    .hero p {
      max-width: 650px;
      margin: auto;
      color: var(--text-secondary);
      font-size: 1.1rem;
    }

    .cta-btn {
      display: inline-block;
      margin-top: 2rem;
      padding: 1rem 2.5rem;
      background: var(--accent);
      color: white;
      border-radius: 8px;
      text-decoration: none;
      font-weight: 600;
    }

    .cta-btn:hover {
      background: var(--accent-hover);
    }

    /* ===== SECTIONS ===== */
    section {
      max-width: 1200px;
      margin: auto;
      padding: 6rem 2rem;
    }

    .section-title {
      text-align: center;
      font-size: 2.3rem;
      margin-bottom: 3rem;
    }

    /* ===== ABOUT ===== */
    .about-text {
      max-width: 800px;
      margin: auto;
      text-align: center;
      color: var(--text-secondary);
      font-size: 1.1rem;
    }

    /* ===== SKILLS ===== */
    .skills-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
      gap: 1.5rem;
    }

    .skill-card {
      background: var(--bg-secondary);
      padding: 1.5rem;
      text-align: center;
      border-radius: 10px;
      border: 1px solid var(--border);
    }

    /* ===== PROJECTS ===== */
    .projects-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 2rem;
    }

    .project-card {
      background: var(--bg-secondary);
      padding: 2rem;
      border-radius: 12px;
      border: 1px solid var(--border);
    }

    /* ===== FOOTER ===== */
    footer {
      text-align: center;
      padding: 3rem 2rem;
      border-top: 1px solid var(--border);
      color: var(--text-secondary);
    }

    @media (max-width: 768px) {
      nav ul {
        display: none;
      }
    }
  </style>
</head>

<body>

  <!-- NAV -->
  <nav>
    <div class="container">
      <a href="#" class="logo">TJ Selim</a>
      <ul>
        <li><a href="#about">About</a></li>
        <li><a href="#skills">Skills</a></li>
        <li><a href="#projects">Projects</a></li>
      </ul>
    </div>
  </nav>

  <!-- HERO -->
  <section class="hero">
    <div>
      <h1>TJ Selim Reja</h1>
      <div class="subtitle">Frontend Learner & Philosophy Explorer</div>
      <p>
        I build clean, modern web interfaces and love learning philosophy,
        design, and technology.
      </p>
      <a href="#projects" class="cta-btn">View My Work</a>
    </div>
  </section>

  <!-- ABOUT -->
  <section id="about">
    <h2 class="section-title">About Me</h2>
    <p class="about-text">
      I am learning web development and exploring philosophy.  
      I enjoy creating minimal, modern designs and improving my skills every day.
    </p>
  </section>

  <!-- SKILLS -->
  <section id="skills">
    <h2 class="section-title">Skills</h2>
    <div class="skills-grid">
      <div class="skill-card">HTML</div>
      <div class="skill-card">CSS</div>
      <div class="skill-card">Git & GitHub</div>
      <div class="skill-card">Responsive Design</div>
    </div>
  </section>

  <!-- PROJECTS -->
  <section id="projects">
    <h2 class="section-title">Projects</h2>
    <div class="projects-grid">
      <div class="project-card">
        <h3>Portfolio Website</h3>
        <p>A clean personal portfolio built using HTML & CSS.</p>
      </div>
      <div class="project-card">
        <h3>Practice Projects</h3>
        <p>Small UI components and layouts for learning.</p>
      </div>
    </div>
  </section>

  <!-- FOOTER -->
  <footer>
    <p>© 2025 TJ Selim Reja • All rights reserved</p>
  </footer>

</body>
</html>
