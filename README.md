<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Fatimah Al-Najjar | Portfolio</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Arial', sans-serif;
      line-height: 1.6;
      color: #333;
      background-color: #f8f9fa;
      padding-top: 80px;
    }

    /* Navigation */
    .nav {
      background: rgba(255,255,255,0.95);
      backdrop-filter: blur(10px);
      position: fixed;
      top: 0;
      width: 100%;
      z-index: 1000;
      padding: 15px 0;
      box-shadow: 0 2px 10px rgba(0,0,0,0.1);
    }

    .nav-container {
      max-width: 1200px;
      margin: 0 auto;
      display: flex;
      justify-content: center;
      padding: 0 20px;
    }

    .nav-links {
      display: flex;
      gap: 30px;
    }

    .nav-link {
      color: #333;
      text-decoration: none;
      font-weight: 500;
      padding: 10px 20px;
      border-radius: 25px;
      transition: all 0.3s ease;
      cursor: pointer;
    }

    .nav-link:hover,
    .nav-link.active {
      background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
      color: white;
      transform: translateY(-2px);
    }

    .page {
      display: none;
    }

    .page.active {
      display: block;
    }

    .container {
      max-width: 1200px;
      margin: 0 auto;
      padding: 0 20px;
    }

    .header {
      background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
      color: white;
      padding: 60px 0;
      text-align: center;
    }

    .header h1 {
      font-size: 2.5rem;
      margin-bottom: 10px;
      font-weight: 300;
    }

    .header .tagline {
      font-size: 1.2rem;
      opacity: 0.9;
      margin-bottom: 30px;
    }

    .profile-img {
      width: 120px;
      height: 140px;
      border-radius: 10px;
      margin: 0 auto 30px;
      display: block;
      border: 4px solid rgba(255,255,255,0.3);
    }

    .main-content {
      background: white;
      margin: -30px auto 0;
      border-radius: 15px;
      box-shadow: 0 10px 30px rgba(0,0,0,0.1);
      overflow: hidden;
      position: relative;
      z-index: 1;
    }

    .projects-section {
      padding: 50px 40px;
    }

    .projects-section h2 {
      font-size: 1.8rem;
      color: #2c3e50;
      margin-bottom: 40px;
      text-align: center;
    }

    .projects-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
      gap: 30px;
      margin-top: 30px;
    }

    .project-card {
      background: white;
      border-radius: 15px;
      overflow: hidden;
      box-shadow: 0 10px 30px rgba(0,0,0,0.1);
      transition: all 0.3s ease;
      position: relative;
    }

    .project-card:hover {
      transform: translateY(-10px);
      box-shadow: 0 20px 40px rgba(0,0,0,0.15);
    }

    .project-header {
      background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
      color: white;
      padding: 25px;
    }

    .project-title {
      font-size: 1.3rem;
      font-weight: 600;
      margin-bottom: 10px;
    }

    .project-type {
      font-size: 0.9rem;
      opacity: 0.8;
    }

    .project-content {
      padding: 25px;
    }

    .project-description {
      color: #666;
      line-height: 1.6;
      margin-bottom: 20px;
    }

    .project-tech {
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
      margin-bottom: 20px;
    }

    .tech-tag {
      background: #f0f0f0;
      color: #666;
      padding: 5px 12px;
      border-radius: 20px;
      font-size: 0.85rem;
      border: 1px solid #e0e0e0;
      transition: all 0.3s ease;
    }

    .tech-tag:hover {
      background: #667eea;
      color: white;
      border-color: #667eea;
    }

    .project-highlights {
      list-style: none;
      margin-top: 15px;
      padding-left: 20px;
    }

    .project-highlights li {
      color: #555;
      padding: 5px 0;
      position: relative;
    }

    .project-highlights li::before {
      content: "✓";
      color: #667eea;
      position: absolute;
      left: -20px;
      font-weight: bold;
    }

    @media (max-width: 768px) {
      .projects-grid {
        grid-template-columns: 1fr;
      }

      .nav-links {
        gap: 15px;
      }

      .nav-link {
        padding: 8px 15px;
        font-size: 0.9rem;
      }

      .header h1 {
        font-size: 2rem;
      }
    }
  </style>
</head>
<body>

  <!-- Navigation -->
  <nav class="nav">
    <div class="nav-container">
      <div class="nav-links">
        <a href="#" class="nav-link active" onclick="showPage(event, 'home')">Home</a>
        <a href="#" class="nav-link" onclick="showPage(event, 'projects')">Projects</a>
      </div>
    </div>
  </nav>

  <!-- Home Page -->
  <div id="home" class="page active">
    <div class="header">
      <div class="container">
        <img src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='120' height='140' viewBox='0 0 120 140'%3E%3Crect width='120' height='140' fill='%23f0f0f0' rx='10'/%3E%3Ctext x='60' y='75' text-anchor='middle' font-family='Arial' font-size='14' fill='%23666'%3EProfile Photo%3C/text%3E%3C/svg%3E" alt="Fatimah Al-Najjar" class="profile-img">
        <h1>From Classroom to Real-World Impact. Take a Look at My Work!</h1>
        <div class="tagline">Fatimah Al-Najjar</div>
      </div>
    </div>
    <div class="container">
      <div class="main-content">
        <div class="projects-section">
          <h2>Welcome</h2>
          <p style="padding: 30px; text-align: center; font-size: 1.1rem; color: #444;">
            I'm a Northwestern Engineering graduate who loves turning data into impact. Whether it’s building medical devices, developing simulations, or writing clean code, I combine technical expertise with creative problem-solving.
          </p>
        </div>
      </div>
    </div>
  </div>

  <!-- Projects Page -->
  <div id="projects" class="page">
    <div class="header">
      <div class="container">
        <img src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='120' height='140' viewBox='0 0 120 140'%3E%3Crect width='120' height='140' fill='%23f0f0f0' rx='10'/%3E%3Ctext x='60' y='75' text-anchor='middle' font-family='Arial' font-size='14' fill='%23666'%3EProfile Photo%3C/text%3E%3C/svg%3E" alt="Fatimah Al-Najjar" class="profile-img">
        <h1>My Projects & Technical Work</h1>
        <div class="tagline">Engineering Solutions & Research</div>
      </div>
    </div>

    <div class="container">
      <div class="main-content">
        <div class="projects-section">
          <h2>Projects Portfolio</h2>
          <div class="projects-grid">

            <div class="project-card">
              <div class="project-header">
                <div class="project-title">OpenSim Moco in Python</div>
                <div class="project-type">Optimal Control Simulation</div>
              </div>
              <div class="project-content">
                <div class="project-description">
                  Implementation of optimal control problems using OpenSim Moco framework for musculoskeletal movement prediction and analysis.
                </div>
                <div class="project-tech">
                  <span class="tech-tag">Python</span>
                  <span class="tech-tag">OpenSim Moco</span>
                  <span class="tech-tag">Optimal Control</span>
                  <span class="tech-tag">Simulation</span>
                </div>
                <ul class="project-highlights">
                  <li>Solved optimal control problems</li>
                  <li>Automated simulation pipelines</li>
                  <li>Reduced computational time significantly</li>
                </ul>
              </div>
            </div>

            <div class="project-card">
              <div class="project-header">
                <div class="project-title">Flappy Bird in Python</div>
                <div class="project-type">Game Development</div>
              </div>
              <div class="project-content">
                <div class="project-description">
                  Custom-built Flappy Bird using Python and sensor integration. Used real-time analog data to control game mechanics.
                </div>
                <div class="project-tech">
                  <span class="tech-tag">Python</span>
                  <span class="tech-tag">Pygame</span>
                  <span class="tech-tag">Sensor Input</span>
                  <span class="tech-tag">Game Dev</span>
                </div>
                <ul class="project-highlights">
                  <li>Signal-to-software integration</li>
                  <li>Hardware and software design</li>
                  <li>Custom sensor mechanics</li>
                </ul>
              </div>
            </div>

            <!-- Add more project cards here as needed -->

          </div>
        </div>
      </div>
    </div>
  </div>

  <script>
    function showPage(event, pageId) {
      event.preventDefault();
      document.querySelectorAll('.page').forEach(page => page.classList.remove('active'));
      document.getElementById(pageId).classList.add('active');
      document.querySelectorAll('.nav-link').forEach(link => link.classList.remove('active'));
      event.target.classList.add('active');
      window.scrollTo(0, 0);
    }
  </script>

</body>
</html>
