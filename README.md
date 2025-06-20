<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Fatimah Al-Najjar - Full Portfolio</title>
  <link rel="stylesheet" href="styles.css">
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
    <!-- Your existing home content -->
  </div>

  <!-- Projects Page -->
  <div id="projects" class="page">
    <div class="header">
      <div class="container">
        <h1>Projects Portfolio</h1>
        <div class="tagline">A showcase of technical and engineering work</div>
      </div>
    </div>
    <div class="container">
      <div class="main-content">
        <div class="projects-section">
          <div class="projects-grid">

            <div class="project-card">
              <div class="project-header">
                <div class="project-title">C-Section Baby Glove</div>
              </div>
              <div class="project-content">
                <p>Strategic Project Leadership: Led a team of four in the design and development of a glove-based device to assist with impacted fetal head deliveries in low- and middle-income countries. Structured the project and spearheaded the strategy by defining clinical needs, setting design milestones, and coordinating simulation-based testing.</p>
                <p>Clinical Collaboration and Validation: Directed collaboration with a retired OBGYN client and a practicing physician at NorthShore to ensure clinical relevance and usability. Oversaw prototype validation using SimMom and a custom-built uterine model.</p>
                <p>Cross-Functional Execution: Managed cross-functional efforts from concept through testing, resulting in a provisional patent application for a low-cost, single-user obstetric solution.</p>
              </div>
            </div>

            <div class="project-card">
              <div class="project-header">
                <div class="project-title">Fluid Dynamic Algorithms in MATLAB</div>
              </div>
              <div class="project-content">
                <p>Completed a series of advanced computational modeling projects by applying MATLAB to develop numerical algorithms for simulating physical systems and validating engineering models.</p>
                <p>Algorithm Implementation: Designed and implemented solvers for steady and unsteady 1D/2D/3D heat transfer and convection-diffusion problems using discretization techniques such as finite difference and finite volume methods.</p>
                <p>Code Optimization: Executed structured projects involving pressure-based algorithms (SIMPLE, SIMPLER), fluid flow simulations, and equation linearization methods, to emphasize mathematical accuracy and code efficiency.</p>
                <p>Technical Documentation: Produced detailed reports in LaTeX, integrating simulation results, error analyses, and visualizations to communicate technical findings clearly and effectively and mirror best practices in business reporting and model validation.</p>
              </div>
            </div>

            <div class="project-card">
              <div class="project-header">
                <div class="project-title">Flappy Bird in Python</div>
              </div>
              <div class="project-content">
                <p>Software Development: Wrote a Python script to continuously read analog voltage data, apply real-time mapping logic, and control game mechanics using Pygame Zero, demonstrating signal-to-software integration and data-driven control</p>
                <p>System Architecture: Demonstrated end-to-end system design, from analog signal acquisition to digital response, highlighting practical experience in embedded systems, data interpretation, and Python-based automation</p>
                <p>Sensor Integration: Designed and implemented a Python-controlled version of Flappy Bird using a custom-built bending sensor to convert mechanical deformation into game input</p>
                <p>Hardware Design: Developed a hardware system incorporating a voltage divider, buffer amplifier, and high/low-pass filters to process analog signals, with a level shifter for Raspberry Pi Pico compatibility</p>
              </div>
            </div>

            <div class="project-card">
              <div class="project-header">
                <div class="project-title">Robotic Manipulation in Python</div>
              </div>
              <div class="project-content">
                <p>Python Scripting: Completed a final project in ME 449: Robotic Manipulation, using Python and CoppeliaSim to automate a robotic arm for dynamic object manipulation tasks involving position detection, grasp planning, and trajectory execution.</p>
                <p>Time Series Data Analysis: Developed and tested multiple control strategies with varying damping and feedback parameters to capture real-time movement and error data through scripted logging into CSV files for comparative analysis.</p>
                <p>Data-Driven Decision Making: Visualized positional error convergence across control methods using Python plotting libraries to enable data-driven evaluation of optimization performance and the decision-making process.</p>
              </div>
            </div>

            <div class="project-card">
              <div class="project-header">
                <div class="project-title">Data Visualization in R</div>
              </div>
              <div class="project-content">
                <p>R Scripting: Completed a series of data visualization projects using R and ggplot2 to transform raw datasets into clear, insight-driven graphics for both structured and exploratory analysis.</p>
                <p>Data Visualization: Applied best practices in visual encoding, dashboard design, and storytelling to develop custom visualizations and communicate patterns, trends, and outliers across various data types and business contexts.</p>
              </div>
            </div>

            <div class="project-card">
              <div class="project-header">
                <div class="project-title">Research Grant: AI-Driven Anatomic Fingerprinting of Coronary Arteries</div>
              </div>
              <div class="project-content">
                <p>Machine Learning: Led a proposal for an independent project to develop a predictive framework for ischemic heart disease using machine learning, computational fluid dynamics (CFD), and AI-driven risk modeling.</p>
                <p>Problem Identification: Identified key limitations in existing diagnostic workflows that rely solely on static anatomical metrics, and proposed a data-driven alternative leveraging patient-specific hemodynamic profiles.</p>
                <p>Pipeline Development: Designed a pipeline integrating AI and CFD simulations to generate personalized risk signatures, to enable more accurate stratification of cardiovascular event risk. First, I propose a 3D U-Net CNN model with uncertainty estimation (Monte Carlo dropout) to automate segmentation. Nest, 3D coronary geometries from Aim 1 are refined with Poisson surface reconstruction and anisotropic smoothing. Patient-specific inflow data are derived from Doppler echocardiography or 4D flow MRI. Outflow conditions are modeled using Windkessel circuits. Laslty, algorithms will integrate geometric and CFD-derived features to generate individual “risk fingerprints.” Cross-validation will assess the performance of these signatures in distinguishing MACE vs. non-MACE patients, compared to conventional metrics like percent stenosis.</p>
                <p>Strategic Insight: Demonstrated strategic thinking by bridging domain-specific insights with advanced analytics.</p>
              </div>
            </div>

            <div class="project-card">
              <div class="project-header">
                <div class="project-title">OpenSim Moco in Python</div>
              </div>
              <div class="project-content">
                <p>Developed an object-oriented Python framework on top of OpenSim Moco to simulate, optimize, and analyze neuromuscular control and hand kinematics for prosthetics and rehabilitation applications.</p>
                <p>System Architecture: Designed modular Python classes to structure core functionality, including model building, simulation setup, data integration, and results visualization</p>
                <p>Object-Oriented Design: Implemented key classes such as</p>
                <ul>
                  <li>MocoHandModelBuilder to configure musculoskeletal models with adjustable muscles, constraints, and joint parameters</li>
                  <li>MocoHandSimulation to define and solve optimal control problems with cost terms, bounds, and solver settings</li>
                  <li>DataHandler to load, preprocess, and format experimental data for simulation input</li>
                  <li>Visualizer to generate diagnostic plots of muscle activation, kinematics, and solver performance</li>
                </ul>
                <p>Data Integration & Automation: Enabled batch simulation runs, parameter sweeps, and reproducible experiments through configurable class-based workflows</p>
                <p>Scalability: Engineered the framework for extensibility to allow users to add muscles, redefine objective functions, or modify model architecture without disrupting core logic</p>
              </div>
            </div>

            <div class="project-card">
              <div class="project-header">
                <div class="project-title">Hand and Wrist Musculoskeletal Model in Python and C++</div>
              </div>
              <div class="project-content">
                <p>Engineered enhancements to an OpenSim-based biomechanical model by integrating new muscles and synergy controllers to improve simulation fidelity of the extensor hood mechanism in the human hand.</p>
                <p>Analytical Evaluation: Processed simulation results to assess joint performance and muscle activation, summarizing key insights in a user-friendly format suitable for review by both technical and non-technical stakeholders</p>
                <p>Workflow Automation: Designed a lightweight automation pipeline to execute Computed Muscle Control (CMC) simulations and extract relevant outputs across 12 multi-joint, multi-subject motion trials</p>
                <p>Strategic Proposal: Identified limitations in existing CMC objective functions and proposed a migration to the Moco simulation platform to enable better optimization and analytical flexibility (see MocoHand project)</p>
                <p>Data Quality & Selection: Cleaned and evaluated time-series joint angle data collected via CyberGlove; selected optimal trials based on cross-subject consistency and signal reliability to ensure robust input for simulation</p>
                <p>Simulation Modeling: Added new muscles and coordination strategies to the existing OpenSim Hand and Wrist model using both GUI and C++ API; configured the model to more accurately reflect real-world anatomical structures</p>
              </div>
            </div>

          </div>
        </div>
      </div>
    </div>
  </div>
</body>
</html>
