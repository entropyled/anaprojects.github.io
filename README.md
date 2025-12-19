<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>My Projects | CS & EE</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
    }

    body {
      background: #0f172a;
      color: #e5e7eb;
      min-height: 100vh;
      display: flex;
      flex-direction: column;
    }

    header {
      padding: 1rem 2rem;
      border-bottom: 1px solid #1f2937;
      display: flex;
      justify-content: space-between;
      align-items: center;
      background: #020617;
      position: sticky;
      top: 0;
      z-index: 10;
    }

    .logo {
      font-weight: 700;
      letter-spacing: 0.08em;
      text-transform: uppercase;
      font-size: 0.9rem;
      color: #38bdf8;
    }

    nav {
      display: flex;
      gap: 0.75rem;
      background: #020617;
      padding: 0.4rem;
      border-radius: 999px;
      border: 1px solid #1f2937;
    }

    .nav-btn {
      border: none;
      background: transparent;
      color: #9ca3af;
      padding: 0.45rem 0.9rem;
      border-radius: 999px;
      font-size: 0.85rem;
      cursor: pointer;
      transition: all 0.15s ease;
    }

    .nav-btn.active {
      background: linear-gradient(135deg, #22c55e, #38bdf8);
      color: #020617;
      font-weight: 600;
    }

    main {
      max-width: 960px;
      margin: 0 auto;
      padding: 1.5rem 1.25rem 3rem;
      width: 100%;
      flex: 1;
    }

    .intro {
      margin-bottom: 1.75rem;
    }

    .intro h1 {
      font-size: 1.8rem;
      margin-bottom: 0.4rem;
    }

    .intro p {
      color: #9ca3af;
      font-size: 0.95rem;
    }

    .tagline {
      color: #6b7280;
      font-size: 0.85rem;
      margin-top: 0.25rem;
    }

    .pill-row {
      display: flex;
      flex-wrap: wrap;
      gap: 0.5rem;
      margin-top: 0.75rem;
    }

    .pill {
      font-size: 0.75rem;
      padding: 0.1rem 0.6rem;
      border-radius: 999px;
      border: 1px solid #1f2937;
      color: #9ca3af;
    }

    .sections {
      background: radial-gradient(circle at top left, #0f172a, #020617);
      border-radius: 1rem;
      border: 1px solid #1f2937;
      padding: 1.25rem;
      box-shadow: 0 18px 45px rgba(0, 0, 0, 0.55);
    }

    .section {
      display: none;
      animation: fadeIn 0.2s ease-out;
    }

    .section.active {
      display: block;
    }

    .section h2 {
      font-size: 1.2rem;
      margin-bottom: 0.75rem;
      display: flex;
      align-items: center;
      gap: 0.5rem;
    }

    .badge {
      font-size: 0.7rem;
      padding: 0.1rem 0.5rem;
      border-radius: 999px;
      text-transform: uppercase;
      letter-spacing: 0.08em;
      border: 1px solid #1f2937;
    }

    .badge.cs {
      color: #38bdf8;
      border-color: #0ea5e9;
    }

    .badge.ee {
      color: #22c55e;
      border-color: #22c55e;
    }

    .projects-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(230px, 1fr));
      gap: 0.9rem;
      margin-top: 0.75rem;
    }

    .project-card {
      padding: 0.9rem;
      border-radius: 0.75rem;
      border: 1px solid #1f2937;
      background: rgba(15, 23, 42, 0.9);
      transition: transform 0.12s ease, box-shadow 0.12s ease, border-color 0.12s ease;
    }

    .project-card:hover {
      transform: translateY(-2px);
      box-shadow: 0 10px 25px rgba(0, 0, 0, 0.6);
      border-color: #38bdf8;
    }

    .project-title {
      font-size: 0.95rem;
      font-weight: 600;
      margin-bottom: 0.25rem;
    }

    .project-meta {
      font-size: 0.75rem;
      color: #6b7280;
      margin-bottom: 0.4rem;
    }

    .project-desc {
      font-size: 0.8rem;
      color: #9ca3af;
      margin-bottom: 0.4rem;
    }

    .project-tags {
      display: flex;
      flex-wrap: wrap;
      gap: 0.3rem;
    }

    .tag {
      font-size: 0.7rem;
      padding: 0.05rem 0.45rem;
      border-radius: 999px;
      border: 1px solid #1f2937;
      color: #9ca3af;
    }

    .links-row {
      margin-top: 0.65rem;
      display: flex;
      gap: 0.6rem;
      align-items: center;
      font-size: 0.75rem;
    }

    .link {
      color: #38bdf8;
      text-decoration: none;
    }

    .link:hover {
      text-decoration: underline;
    }

    footer {
      text-align: center;
      padding: 1rem 0;
      font-size: 0.75rem;
      color: #6b7280;
    }

    @keyframes fadeIn {
      from {
        opacity: 0;
        transform: translateY(3px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    @media (max-width: 640px) {
      header {
        flex-direction: column;
        align-items: flex-start;
        gap: 0.75rem;
      }

      nav {
        align-self: stretch;
        justify-content: space-between;
      }
    }
  </style>
</head>
<body>
  <header>
    <div class="logo">ANA · PROJECTS</div>
    <nav>
      <button class="nav-btn active" data-target="cs-section">Computer Science</button>
      <button class="nav-btn" data-target="ee-section">Electrical Engineering</button>
    </nav>
  </header>

  <main>
    <section class="intro">
      <h1>Projects in Computer Science & Electrical Engineering</h1>
      <p>
        A curated collection of my technical work, split into software-focused and hardware-focused paths.
      </p>
      <p class="tagline">
        Exploring algorithms, code, circuits, and systems—one project at a time.
      </p>

      <div class="pill-row">
        <span class="pill">Portfolio-ready</span>
        <span class="pill">Student projects</span>
        <span class="pill">Self-directed experiments</span>
      </div>
    </section>

    <section class="sections">
      <!-- CS SECTION -->
      <div id="cs-section" class="section active">
        <h2>
          Computer Science projects
          <span class="badge cs">software & algorithms</span>
        </h2>
        <div class="projects-grid">
          <!-- Project 1 -->
          <article class="project-card">
            <div class="project-title">Pathfinding Visualizer</div>
            <div class="project-meta">Python · Pygame · Algorithms</div>
            <p class="project-desc">
              Interactive tool that visualizes algorithms like A*, Dijkstra, and BFS on a grid,
              showing how each explores the search space.
            </p>
            <div class="project-tags">
              <span class="tag">A*</span>
              <span class="tag">Dijkstra</span>
              <span class="tag">Graphs</span>
            </div>
            <div class="links-row">
              <a class="link" href="#" target="_blank">View code</a>
              <a class="link" href="#" target="_blank">Project write-up</a>
            </div>
          </article>

          <!-- Project 2 -->
          <article class="project-card">
            <div class="project-title">Task Manager Web App</div>
            <div class="project-meta">JavaScript · HTML/CSS · LocalStorage</div>
            <p class="project-desc">
              A minimal web app that lets users create, edit, and filter tasks locally in the browser,
              with persistent storage and responsive UI.
            </p>
            <div class="project-tags">
              <span class="tag">Frontend</span>
              <span class="tag">State management</span>
              <span class="tag">UX</span>
            </div>
            <div class="links-row">
              <a class="link" href="#" target="_blank">Live demo</a>
              <a class="link" href="#" target="_blank">GitHub repo</a>
            </div>
          </article>

          <!-- Add more CS projects here -->
        </div>
      </div>

      <!-- EE SECTION -->
      <div id="ee-section" class="section">
        <h2>
          Electrical Engineering projects
          <span class="badge ee">hardware & systems</span>
        </h2>
        <div class="projects-grid">
          <!-- Project 1 -->
          <article class="project-card">
            <div class="project-title">Temperature Logger with Microcontroller</div>
            <div class="project-meta">Arduino · Sensors · Data Logging</div>
            <p class="project-desc">
              Embedded system that reads temperature from a digital sensor and logs data to an SD card,
              with serial monitoring and basic error handling.
            </p>
            <div class="project-tags">
              <span class="tag">Embedded</span>
              <span class="tag">C/C++</span>
              <span class="tag">Signal acquisition</span>
            </div>
            <div class="links-row">
              <a class="link" href="#" target="_blank">Schematic</a>
              <a class="link" href="#" target="_blank">Firmware code</a>
            </div>
          </article>

          <!-- Project 2 -->
          <article class="project-card">
            <div class="project-title">Audio Amplifier Prototype</div>
            <div class="project-meta">Analog circuits · SPICE · PCB</div>
            <p class="project-desc">
              Low-noise audio amplifier designed in SPICE, then implemented on a PCB,
              with gain, bandwidth, and noise performance characterized.
            </p>
            <div class="project-tags">
              <span class="tag">Analog</span>
              <span class="tag">Op-amps</span>
              <span class="tag">PCB design</span>
            </div>
            <div class="links-row">
              <a class="link" href="#" target="_blank">Design files</a>
              <a class="link" href="#" target="_blank">Lab report</a>
            </div>
          </article>

          <!-- Add more EE projects here -->
        </div>
      </div>
    </section>
  </main>

  <footer>
    &copy; <span id="year"></span> Ana · CS & EE Projects
  </footer>

  <script>
    // Tab switching logic
    const navButtons = document.querySelectorAll(".nav-btn");
    const sections = document.querySelectorAll(".section");

    navButtons.forEach((btn) => {
      btn.addEventListener("click", () => {
        const targetId = btn.getAttribute("data-target");

        navButtons.forEach((b) => b.classList.remove("active"));
        sections.forEach((section) => section.classList.remove("active"));

        btn.classList.add("active");
        document.getElementById(targetId).classList.add("active");
      });
    });

    // Auto year in footer
    document.getElementById("year").textContent = new Date().getFullYear();
  </script>
</body>
</html>
