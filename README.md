<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Fatimah Al-Najjar - Portfolio</title>
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

        .nav-link:hover, .nav-link.active {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            transform: translateY(-2px);
        }

        /* Page sections */
        .page {
            display: none;
        }

        .page.active {
            display: block;
        }

        body {
            padding-top: 80px;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Header Section */
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

        /* Main Content */
        .main-content {
            background: white;
            margin: -30px auto 0;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            overflow: hidden;
            position: relative;
            z-index: 1;
        }

        .intro {
            padding: 50px 40px;
            text-align: center;
            border-bottom: 1px solid #eee;
        }

        .intro h2 {
            font-size: 1.8rem;
            color: #2c3e50;
            margin-bottom: 20px;
        }

        .intro p {
            font-size: 1.1rem;
            line-height: 1.8;
            color: #666;
            max-width: 900px;
            margin: 0 auto;
        }

        /* Skills Section */
        .skills-section {
            padding: 50px 40px;
            background: #f8f9fa;
        }

        .skills-section h2 {
            font-size: 1.8rem;
            color: #2c3e50;
            margin-bottom: 30px;
            text-align: center;
        }

        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
            margin-top: 30px;
        }

        .skill-category {
            background: white;
            padding: 25px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.08);
            transition: transform 0.3s ease;
        }

        .skill-category:hover {
            transform: translateY(-5px);
        }

        .skill-category h3 {
            color: #667eea;
            margin-bottom: 15px;
            font-size: 1.2rem;
        }

        .skill-category ul {
            list-style: none;
        }

        .skill-category li {
            padding: 5px 0;
            color: #666;
            border-bottom: 1px solid #eee;
        }

        .skill-category li:last-child {
            border-bottom: none;
        }

        /* Experience Section */
        .experience-section {
            padding: 50px 40px;
        }

        .experience-section h2 {
            font-size: 1.8rem;
            color: #2c3e50;
            margin-bottom: 40px;
            text-align: center;
        }

        .job {
            background: white;
            margin-bottom: 40px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.08);
            overflow: hidden;
            transition: transform 0.3s ease;
        }

        .job:hover {
            transform: translateY(-3px);
        }

        .job-header {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 25px 30px;
        }

        .job-title {
            font-size: 1.4rem;
            font-weight: 600;
            margin-bottom: 5px;
        }

        .company {
            font-size: 1.2rem;
            opacity: 0.9;
            margin-bottom: 5px;
        }

        .job-period {
            font-size: 0.9rem;
            opacity: 0.8;
        }

        .job-content {
            padding: 30px;
        }

        .tech-skills {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 30px;
            margin-bottom: 30px;
        }

        .tech-section h4 {
            color: #667eea;
            margin-bottom: 10px;
            font-size: 1rem;
        }

        .tech-section ul {
            list-style: none;
        }

        .tech-section li {
            color: #666;
            padding: 3px 0;
            position: relative;
            padding-left: 15px;
        }

        .tech-section li:before {
            content: "•";
            color: #667eea;
            position: absolute;
            left: 0;
        }

        .achievements {
            margin-top: 20px;
        }

        .achievements ul {
            list-style: none;
        }

        .achievements li {
            color: #555;
            padding: 8px 0;
            padding-left: 20px;
            position: relative;
            line-height: 1.6;
        }

        .achievements li:before {
            content: "▸";
            color: #667eea;
            position: absolute;
            left: 0;
            font-weight: bold;
        }

        /* Projects Section */
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
            position: relative;
            overflow: hidden;
        }

        .project-header::before {
            content: '';
            position: absolute;
            top: -50%;
            right: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(255,255,255,0.1) 0%, transparent 70%);
            animation: float 6s ease-in-out infinite;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-20px); }
        }

        .project-title {
            font-size: 1.3rem;
            font-weight: 600;
            margin-bottom: 10px;
            position: relative;
            z-index: 1;
        }

        .project-type {
            font-size: 0.9rem;
            opacity: 0.8;
            position: relative;
            z-index: 1;
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
        }

        .project-highlights li {
            color: #555;
            padding: 5px 0;
            padding-left: 20px;
            position: relative;
            line-height: 1.5;
        }

        .project-highlights li:before {
            content: "✓";
            color: #667eea;
            position: absolute;
            left: 0;
            font-weight: bold;
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .container {
                padding: 0 15px;
            }

            .header h1 {
                font-size: 2rem;
            }

            .intro, .skills-section, .experience-section, .projects-section {
                padding: 30px 20px;
            }

            .tech-skills {
                grid-template-columns: 1fr;
                gap: 20px;
            }

            .job-content {
                padding: 20px;
            }

            .nav-links {
                gap: 15px;
            }

            .nav-link {
                padding: 8px 15px;
                font-size: 0.9rem;
            }

            .projects-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <!-- Navigation -->
    <nav class="nav">
        <div class="nav-container">
            <div class="nav-links">
                <a class="nav-link active" onclick="showPage('home', this)">Home</a>
                <a class="nav-link" onclick="showPage('projects')">Projects</a>
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
            <div class="intro">
                <h2>Engineer Who Loves Data, Devices, and Discovery</h2>
                <p>I'm a Northwestern graduate (BS/MS in Biomedical and Mechanical Engineering with a focus on Advanced Data Analytics) who loves using Python and data to solve real-world problems. At Novo Surgical, I built automated workflows, designed data-driven process improvements, and worked hands-on with production teams to optimize operations. I've also done research in three engineering labs, tutored Economics, and helped lead campus programs. Whether it's building visual dashboards, analyzing trends, or streamlining systems, I enjoy applying my engineering background to make processes smarter and more efficient, especially in fast-paced, high-impact environments.</p>
            </div>
            <div class="projects-section">
    <h2>Projects Portfolio</h2>
    <div class="projects-grid">

        <div class="project-card">
            <div class="project-header">
                <div class="project-title">C-Section Baby Glove</div>
                <div class="project-type">Medical Device Design</div>
            </div>
            <div class="project-content">
                <div class="project-description">
                    Strategic Project Leadership: Led a team of four in the design and development of a glove-based device to assist with impacted fetal head deliveries in low- and middle-income countries. Structured the project and spearheaded the strategy by defining clinical needs, setting design milestones, and coordinating simulation-based testing.<br><br>
                    Clinical Collaboration and Validation: Directed collaboration with a retired OBGYN client and a practicing physician at NorthShore to ensure clinical relevance and usability. Oversaw prototype validation using SimMom and a custom-built uterine model.<br><br>
                    Cross-Functional Execution: Managed cross-functional efforts from concept through testing, resulting in a provisional patent application for a low-cost, single-user obstetric solution.
                </div>
            </div>
        </div>

        <div class="project-card">
            <div class="project-header">
                <div class="project-title">Fluid Dynamic Algorithms in MATLAB</div>
                <div class="project-type">Computational Engineering</div>
            </div>
            <div class="project-content">
                <div class="project-description">
                    Completed a series of advanced computational modeling projects by applying MATLAB to develop numerical algorithms for simulating physical systems and validating engineering models.<br><br>
                    Algorithm Implementation: Designed and implemented solvers for steady and unsteady 1D/2D/3D heat transfer and convection-diffusion problems using discretization techniques such as finite difference and finite volume methods.<br><br>
                    Code Optimization: Executed structured projects involving pressure-based algorithms (SIMPLE, SIMPLER), fluid flow simulations, and equation linearization methods, to emphasize mathematical accuracy and code efficiency.<br><br>
                    Technical Documentation: Produced detailed reports in LaTeX, integrating simulation results, error analyses, and visualizations to communicate technical findings clearly and effectively and mirror best practices in business reporting and model validation.
                </div>
            </div>
        </div>

        <div class="project-card">
            <div class="project-header">
                <div class="project-title">Flappy Bird in Python</div>
                <div class="project-type">Sensor-Driven Software</div>
            </div>
            <div class="project-content">
                <div class="project-description">
                    Software Development: Wrote a Python script to continuously read analog voltage data, apply real-time mapping logic, and control game mechanics using Pygame Zero, demonstrating signal-to-software integration and data-driven control.<br><br>
                    System Architecture: Demonstrated end-to-end system design, from analog signal acquisition to digital response, highlighting practical experience in embedded systems, data interpretation, and Python-based automation.<br><br>
                    Sensor Integration: Designed and implemented a Python-controlled version of Flappy Bird using a custom-built bending sensor to convert mechanical deformation into game input.<br><br>
                    Hardware Design: Developed a hardware system incorporating a voltage divider, buffer amplifier, and high/low-pass filters to process analog signals, with a level shifter for Raspberry Pi Pico compatibility.
                </div>
            </div>
        </div>

        <div class="project-card">
            <div class="project-header">
                <div class="project-title">Robotic Manipulation in Python</div>
                <div class="project-type">Robotics</div>
            </div>
            <div class="project-content">
                <div class="project-description">
                    Python Scripting: Completed a final project in ME 449: Robotic Manipulation, using Python and CoppeliaSim to automate a robotic arm for dynamic object manipulation tasks involving position detection, grasp planning, and trajectory execution.<br><br>
                    Time Series Data Analysis: Developed and tested multiple control strategies with varying damping and feedback parameters to capture real-time movement and error data through scripted logging into CSV files for comparative analysis.<br><br>
                    Data-Driven Decision Making: Visualized positional error convergence across control methods using Python plotting libraries to enable data-driven evaluation of optimization performance and the decision-making process.
                </div>
            </div>
        </div>

        <div class="project-card">
            <div class="project-header">
                <div class="project-title">Data Visualization in R</div>
                <div class="project-type">Data Analytics</div>
            </div>
            <div class="project-content">
                <div class="project-description">
                    R Scripting: Completed a series of data visualization projects using R and ggplot2 to transform raw datasets into clear, insight-driven graphics for both structured and exploratory analysis.<br><br>
                    Data Visualization: Applied best practices in visual encoding, dashboard design, and storytelling to develop custom visualizations and communicate patterns, trends, and outliers across various data types and business contexts.
                </div>
            </div>
        </div>

        <div class="project-card">
            <div class="project-header">
                <div class="project-title">Research Grant: AI-Driven Anatomic Fingerprinting</div>
                <div class="project-type">AI & Cardiovascular Modeling</div>
            </div>
            <div class="project-content">
                <div class="project-description">
                    Machine Learning: Led a proposal for an independent project to develop a predictive framework for ischemic heart disease using machine learning, computational fluid dynamics (CFD), and AI-driven risk modeling.<br><br>
                    Problem Identification: Identified key limitations in existing diagnostic workflows that rely solely on static anatomical metrics, and proposed a data-driven alternative leveraging patient-specific hemodynamic profiles.<br><br>
                    Pipeline Development: Designed a pipeline integrating AI and CFD simulations to generate personalized risk signatures, to enable more accurate stratification of cardiovascular event risk. First, I propose a 3D U-Net CNN model with uncertainty estimation (Monte Carlo dropout) to automate segmentation. Nest, 3D coronary geometries from Aim 1 are refined with Poisson surface reconstruction and anisotropic smoothing. Patient-specific inflow data are derived from Doppler echocardiography or 4D flow MRI. Outflow conditions are modeled using Windkessel circuits. Laslty, algorithms will integrate geometric and CFD-derived features to generate individual “risk fingerprints.” Cross-validation will assess the performance of these signatures in distinguishing MACE vs. non-MACE patients, compared to conventional metrics like percent stenosis.<br><br>
                    Strategic Insight: Demonstrated strategic thinking by bridging domain-specific insights with advanced analytics.
                </div>
            </div>
        </div>

        <div class="project-card">
            <div class="project-header">
                <div class="project-title">OpenSim Moco in Python</div>
                <div class="project-type">Biomechanical Simulation</div>
            </div>
            <div class="project-content">
                <div class="project-description">
                    Developed an object-oriented Python framework on top of OpenSim Moco to simulate, optimize, and analyze neuromuscular control and hand kinematics for prosthetics and rehabilitation applications.<br><br>
                    System Architecture: Designed modular Python classes to structure core functionality, including model building, simulation setup, data integration, and results visualization.<br><br>
                    Object-Oriented Design: Implemented key classes such as<br>
                    MocoHandModelBuilder to configure musculoskeletal models with adjustable muscles, constraints, and joint parameters<br>
                    MocoHandSimulation to define and solve optimal control problems with cost terms, bounds, and solver settings<br>
                    DataHandler to load, preprocess, and format experimental data for simulation input<br>
                    Visualizer to generate diagnostic plots of muscle activation, kinematics, and solver performance<br><br>
                    Data Integration & Automation: Enabled batch simulation runs, parameter sweeps, and reproducible experiments through configurable class-based workflows<br><br>
                    Scalability: Engineered the framework for extensibility to allow users to add muscles, redefine objective functions, or modify model architecture without disrupting core logic
                </div>
            </div>
        </div>

        <div class="project-card">
            <div class="project-header">
                <div class="project-title">Hand and Wrist Musculoskeletal Model</div>
                <div class="project-type">Biomechanics & Modeling</div>
            </div>
            <div class="project-content">
                <div class="project-description">
                    Engineered enhancements to an OpenSim-based biomechanical model by integrating new muscles and synergy controllers to improve simulation fidelity of the extensor hood mechanism in the human hand.<br><br>
                    Analytical Evaluation: Processed simulation results to assess joint performance and muscle activation, summarizing key insights in a user-friendly format suitable for review by both technical and non-technical stakeholders<br><br>
                    Workflow Automation: Designed a lightweight automation pipeline to execute Computed Muscle Control (CMC) simulations and extract relevant outputs across 12 multi-joint, multi-subject motion trials<br><br>
                    Strategic Proposal: Identified limitations in existing CMC objective functions and proposed a migration to the Moco simulation platform to enable better optimization and analytical flexibility (see MocoHand project)<br><br>
                    Data Quality & Selection: Cleaned and evaluated time-series joint angle data collected via CyberGlove; selected optimal trials based on cross-subject consistency and signal reliability to ensure robust input for simulation<br><br>
                    Simulation Modeling: Added new muscles and coordination strategies to the existing OpenSim Hand and Wrist model using both GUI and C++ API; configured the model to more accurately reflect real-world anatomical structures
                </div>
            </div>
        </div>

    </div>
</div>

            <div class="experience-section">
                <h2>Professional Experience</h2>

                <div class="job">
                    <div class="job-header">
                        <div class="job-title">Data Science Research Assistant</div>
                        <div class="company">Shirley Ryan AbilityLab</div>
                        <div class="job-period">Nov 2023 – Present | Chicago, IL</div>
                    </div>
                    <div class="job-content">
                        <div class="tech-skills">
                            <div class="tech-section">
                                <h4>Technology Used:</h4>
                                <ul>
                                    <li>Python, OpenSim API, R Shiny, ggplot2, Pandas</li>
                                    <li>Motion capture data, EMG signals, Git</li>
                                </ul>
                            </div>
                            <div class="tech-section">
                                <h4>Skills Gained:</h4>
                                <ul>
                                    <li>Simulation pipeline automation</li>
                                    <li>Time-series data cleaning</li>
                                    <li>Joint/EMG error analysis (RMSE, activation mismatch)</li>
                                    <li>Biomechanical data visualization</li>
                                    <li>Iterative model refinement and validation</li>
                                </ul>
                            </div>
                        </div>
                        <div class="achievements">
                            <ul>
                                <li>Automated a simulation pipeline in Python (OpenSim API), reducing processing time by ~70% and enabling scalable analysis of 12+ ASL hand gesture trials with over 1.5m+ unique data points</li>
                                <li>Designed a scalable data pipeline to process and clean high-frequency kinematic time-series data (100Hz+), enabling error-free simulation input preparation and reducing preprocessing time by 60%</li>
                                <li>Evaluated simulation accuracy using kinematic RMSE, EMG activation mismatch, and actuator load metrics—driving a 40% reduction in joint tracking error through iterative model refinement</li>
                                <li>Delivered insight-driven dashboards in R Shiny to visualize trends in joint torque and muscle forces, supporting data-driven decisions across biomechanical research projects and reducing manual analysis time by 50%</li>
                                <li>Enhanced simulation fidelity by integrating anatomical features (e.g., extensor hood) and synergy-based muscle controllers, reducing kinematic RMSE across joints by up to 40%</li>
                            </ul>
                        </div>
                    </div>
                </div>

                <div class="job">
                    <div class="job-header">
                        <div class="job-title">Data Analyst Research Assistant</div>
                        <div class="company">Shirley Ryan AbilityLab</div>
                        <div class="job-period">Nov 2023 – Present | Chicago, IL</div>
                    </div>
                    <div class="job-content">
                        <div class="tech-skills">
                            <div class="tech-section">
                                <h4>Technology Used:</h4>
                                <ul>
                                    <li>Python, C++, OpenSim Moco, Git</li>
                                    <li>Object-oriented frameworks, LaTeX, CSV logging</li>
                                </ul>
                            </div>
                            <div class="tech-section">
                                <h4>Skills Gained:</h4>
                                <ul>
                                    <li>OOP-based simulation architecture</li>
                                    <li>Batch simulations and parameter sweeps</li>
                                    <li>Solver configuration and constraint modeling</li>
                                    <li>Automation of analysis/reporting pipelines</li>
                                    <li>Technical documentation and code modularity</li>
                                </ul>
                            </div>
                        </div>
                        <div class="achievements">
                            <ul>
                                <li>Worked cross-functionally to identify and resolve modeling errors in musculoskeletal simulations, resulting in more stable parameter configurations and higher confidence in output accuracy</li>
                                <li>Designed and built an object-oriented simulation framework in Python and C++ to streamline model loading, solver setup, and result interpretation, improving reusability and enabling scalable batch simulations</li>
                                <li>Engineered a configurable Moco simulation framework using modular class definitions for constraints, cost terms, and solvers—automating setup and supporting rapid prototyping of new movement cases</li>
                                <li>Created parameterized class methods to support batch simulations, parameter sweeps, and post-run statistical analyses</li>
                                <li>Built an automated data pipeline with class-based logging, result serialization, and visual reporting—boosting reproducibility and cutting debugging time by 50%</li>
                                <li>Built extensible simulation modules using clean, object-oriented principles—supporting future expansion and reducing code duplication across gesture-specific models</li>
                                <li>Authored clear, comprehensive documentation—including usage guides, architecture overviews, and class diagrams—to support onboarding, collaboration, and long-term maintainability</li>
                            </ul>
                        </div>
                    </div>
                </div>

                <div class="job">
                    <div class="job-header">
                        <div class="job-title">Engineering Management Intern</div>
                        <div class="company">Novo Surgical Inc.</div>
                        <div class="job-period">Jun 2024 – Dec 2024 | Westmont, IL</div>
                    </div>
                    <div class="job-content">
                        <div class="tech-skills">
                            <div class="tech-section">
                                <h4>Technology Used:</h4>
                                <ul>
                                    <li>SolidWorks, CorelDraw, TruTops, Microsoft Office</li>
                                    <li>FDA/ISO standards, QA protocols, GanttPro</li>
                                </ul>
                            </div>
                            <div class="tech-section">
                                <h4>Skills Gained:</h4>
                                <ul>
                                    <li>Laser marking workflow automation</li>
                                    <li>FDA/ISO-compliant protocol writing</li>
                                    <li>Cross-functional team leadership</li>
                                    <li>Manufacturing process optimization</li>
                                    <li>Training documentation and SOP design</li>
                                </ul>
                            </div>
                        </div>
                        <div class="achievements">
                            <ul>
                                <li>Automated the laser marking process for 120 top-selling surgical instruments by designing custom fixtures and integrating Trumpf TruTops software—reducing setup time by 60% and minimizing operator errors</li>
                                <li>Authored FDA- and ISO-compliant inspection protocols for a 15,000-instrument portfolio, enhancing traceability and improving audit readiness across manufacturing and quality teams</li>
                                <li>Led a cross-functional team of 7 to identify bottlenecks in manufacturing and QA workflows, implementing process improvements that increased throughput by 25% and reduced rework incidents</li>
                                <li>Created clear instructional guides and visual references that improved training effectiveness and standardized QA procedures across production teams, reducing onboarding time and errors</li>
                                <li>Balanced competing project timelines by coordinating across teams, resolving bottlenecks through root-cause analysis, and adjusting execution plans to meet aggressive delivery targets</li>
                            </ul>
                        </div>
                    </div>
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
                                <div class="project-title">Hand and Wrist Musculoskeletal Model</div>
                                <div class="project-type">Biomechanical Simulation</div>
                            </div>
                            <div class="project-content">
                                <div class="project-description">
                                    Advanced musculoskeletal modeling project focused on hand and wrist biomechanics using computational simulation frameworks.
                                </div>
                                <div class="project-tech">
                                    <span class="tech-tag">Python</span>
                                    <span class="tech-tag">C++</span>
                                    <span class="tech-tag">OpenSim</span>
                                    <span class="tech-tag">Biomechanics</span>
                                </div>
                                <ul class="project-highlights">
                                    <li>Developed comprehensive musculoskeletal model</li>
                                    <li>Implemented simulation algorithms</li>
                                    <li>Validated against experimental data</li>
                                </ul>
                            </div>
                        </div>

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
                                <div class="project-title">Research Grant: AI-Driven Anatomic Fingerprinting</div>
                                <div class="project-type">Medical AI Research</div>
                            </div>
                            <div class="project-content">
                                <div class="project-description">
                                    Cutting-edge research project applying artificial intelligence to coronary artery analysis for anatomic fingerprinting and medical diagnosis.
                                </div>
                                <div class="project-tech">
                                    <span class="tech-tag">AI/ML</span>
                                    <span class="tech-tag">Medical Imaging</span>
                                    <span class="tech-tag">Research</span>
                                    <span class="tech-tag">Grant Funded</span>
                                </div>
                                <ul class="project-highlights">
                                    <li>Secured research funding</li>
                                    <li>Applied AI to medical imaging</li>
                                    <li>Developed novel fingerprinting methods</li>
                                </ul>
                            </div>
                        </div>

                        <div class="project-card">
                            <div class="project-header">
                                <div class="project-title">Data Visualization in R</div>
                                <div class="project-type">Statistical Analysis</div>
                            </div>
                            <div class="project-content">
                                <div class="project-description">
                                    Comprehensive data visualization project utilizing R for statistical analysis and interactive dashboard development.
                                </div>
                                <div class="project-tech">
                                    <span class="tech-tag">R</span>
                                    <span class="tech-tag">R Shiny</span>
                                    <span class="tech-tag">ggplot2</span>
                                    <span class="tech-tag">Data Viz</span>
                                </div>
                                <ul class="project-highlights">
                                    <li>Created interactive dashboards</li>
                                    <li>Advanced statistical visualization</li>
                                    <li>User-friendly interface design</li>
                                </ul>
                            </div>
                        </div>

                        <div class="project-card">
                            <div class="project-header">
                                <div class="project-title">Robotic Manipulation in Python</div>
                                <div class="project-type">Robotics & Control</div>
                            </div>
                            <div class="project-content">
                                <div class="project-description">
                                    Advanced robotics project focusing on manipulation algorithms and control systems implemented in Python.
                                </div>
                                <div class="project-tech">
                                    <span class="tech-tag">Python</span>
                                    <span class="tech-tag">Robotics</span>
                                    <span class="tech-tag">Control Systems</span>
                                    <span class="tech-tag">Manipulation</span>
                                </div>
                                <ul class="project-highlights">
                                    <li>Developed manipulation algorithms</li>
                                    <li>Implemented control systems</li>
                                    <li>Real-world robotics applications</li>
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
                                    Recreation of the popular Flappy Bird game using Python, demonstrating programming fundamentals and game development skills.
                                </div>
                                <div class="project-tech">
                                    <span class="tech-tag">Python</span>
                                    <span class="tech-tag">Game Development</span>
                                    <span class="tech-tag">Graphics</span>
                                    <span class="tech-tag">UI/UX</span>
                                </div>
                                <ul class="project-highlights">
                                    <li>Complete game implementation</li>
                                    <li>User interface design</li>
                                    <li>Game physics and logic</li>
                                </ul>
                            </div>
                        </div>

                        <div class="project-card">
                            <div class="project-header">
                                <div class="project-title">Fluid Dynamic Algorithms in MATLAB</div>
                                <div class="project-type">Computational Engineering</div>
                            </div>
                            <div class="project-content">
                                <div class="project-description">
                                    Implementation of advanced fluid dynamics algorithms using MATLAB for computational fluid dynamics analysis and simulation.
                                </div>
                                <div class="project-tech">
                                    <span class="tech-tag">MATLAB</span>
                                    <span class="tech-tag">CFD</span>
                                    <span class="tech-tag">Algorithms</span>
                                    <span class="tech-tag">Simulation</span>
                                </div>
                                <ul class="project-highlights">
                                    <li>Advanced algorithm development</li>
                                    <li>Computational fluid dynamics</li>
                                    <li>Mathematical modeling</li>
                                </ul>
                            </div>
                        </div>

                        <div class="project-card">
                            <div class="project-header">
                                <div class="project-title">C-Section Baby Glove</div>
                                <div class="project-type">Medical Device Design</div>
                            </div>
                            <div class="project-content">
                                <div class="project-description">
                                    Innovative medical device design project focused on developing a specialized glove for C-section procedures to improve safety and outcomes.
                                </div>
                                <div class="project-tech">
                                    <span class="tech-tag">Medical Design</span>
                                    <span class="tech-tag">Product Development</span>
                                    <span class="tech-tag">Healthcare</span>
                                    <span class="tech-tag">Innovation</span>
                                </div>
                                <ul class="project-highlights">
                                    <li>Medical device innovation</li>
                                    <li>Safety-focused design</li>
                                    <li>Clinical application</li>
                                </ul>
                            </div>
                        </div>

                    </div>
                </div>
            </div>
        </div>
    </div>

    <script>
        function showPage(pageId) {
            // Hide all pages
            const pages = document.querySelectorAll('.page');
            pages.forEach(page => page.classList.remove('active'));
            
            // Show selected page
            document.getElementById(pageId).classList.add('active');
            
            // Update navigation
            const navLinks = document.querySelectorAll('.nav-link');
            navLinks.forEach(link => link.classList.remove('active'));
            function showPage(pageId, el) {
                // Hide all pages
                const pages = document.querySelectorAll('.page');
                pages.forEach(page => page.classList.remove('active'));
                
                // Show selected page
                document.getElementById(pageId).classList.add('active');
                
                // Update navigation
                const navLinks = document.querySelectorAll('.nav-link');
                navLinks.forEach(link => link.classList.remove('active'));
                el.classList.add('active');
            
                // Scroll to top
                window.scrollTo(0, 0);
            }


            
            // Scroll to top
            window.scrollTo(0, 0);
        }
    </script>
</body>
</html>
