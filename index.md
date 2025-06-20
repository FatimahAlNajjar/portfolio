<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Fatimah Al-Najjar - Full Portfolio</title>
  <link rel="stylesheet" href="styles.css">
  <style>
    /* Basic styles for layout */
    body { font-family: Arial, sans-serif; margin: 0; padding: 0; background: #f5f5f5; }
    .nav { background: white; box-shadow: 0 2px 4px rgba(0,0,0,0.1); position: sticky; top: 0; z-index: 10; }
    .nav-container { display: flex; justify-content: center; padding: 1rem; }
    .nav-links { display: flex; gap: 2rem; }
    .nav-link { cursor: pointer; text-decoration: none; color: #333; font-weight: bold; }
    .nav-link.active { color: #667eea; }
    .page { display: none; padding: 2rem; }
    .page.active { display: block; }
    .header { text-align: center; margin-bottom: 2rem; }
    .tagline { color: #666; font-style: italic; }
    .projects-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 1.5rem; }
    .project-card { background: white; padding: 1rem; border-radius: 8px; box-shadow: 0 2px 8px rgba(0,0,0,0.05); }
    .project-header { font-weight: bold; margin-bottom: 0.5rem; }
    ul { padding-left: 1.5rem; }
  </style>
  <script>
    function showPage(pageId) {
      document.querySelectorAll('.page').forEach(p => p.classList.remove('active'));
      document.getElementById(pageId).classList.add('active');
      document.querySelectorAll('.nav-link').forEach(link => link.classList.remove('active'));
      document.querySelectorAll('.nav-link').forEach(link => {
        if (link.getAttribute('onclick').includes(pageId)) {
          link.classList.add('active');
        }
      });
    }
  </script>
</head>
<body>
  <!-- Navigation -->
  <nav class="nav">
    <div class="nav-container">
      <div class="nav-links">
        <a class="nav-link active" onclick="showPage('home')">Home</a>
        <a class="nav-link" onclick="showPage('projects')">Projects</a>
      </div>
    </div>
  </nav>

  <!-- Home Page -->
  <div id="home" class="page active">
    <div class="header">
      <h1>Fatimah Al-Najjar</h1>
      <div class="tagline">Engineer Who Loves Data, Devices, and Discovery</div>
    </div>
    <div class="container">
      <p>I'm a Northwestern graduate (BS/MS in Biomedical and Mechanical Engineering with a focus on Advanced Data Analytics) who loves using Python and data to solve real-world problems. At Novo Surgical, I built automated workflows, designed data-driven process improvements, and worked hands-on with production teams to optimize operations. I've also done research in three engineering labs, tutored Economics, and helped lead campus programs. Whether it's building visual dashboards, analyzing trends, or streamlining systems, I enjoy applying my engineering background to make processes smarter and more efficient, especially in fast-paced, high-impact environments.</p>
    </div>
  </div>

  <!-- Projects Page -->
  <div id="projects" class="page">
    <div class="header">
      <h1>Projects Portfolio</h1>
      <div class="tagline">A showcase of technical and engineering work</div>
    </div>
    <div class="container">
      <div class="main-content">
        <div class="projects-section">
          <div class="projects-grid">
            <!-- Projects inserted here -->
            <!-- Existing project-card blocks remain unchanged -->
          </div>
        </div>
      </div>
    </div>
  </div>
</body>
</html>
