# Ex01 Portfolio
## Date:
   29/8/2025
## AIM
To create a Portfolio using HTML and CSS.

## ALGORITHM
### STEP 1
Create an HTML file (index.html)

### STEP 2
Create a CSS file (style.css)

### STEP 3
Include a navigation bar with links to different sections.

### STEP 4
Add structured sections for introduction, about, projects, and contact details.

### STEP 5
Define global styles for fonts, colors, and layout.

### STEP 6
Style the header, navigation bar, and sections.

### STEP 7
Use Flexbox or CSS Grid for layout design.

### STEP 8
Add hover effects and transitions for interactivity.

### STEP 9
Add Images and Media.

### STEP 10
Use optimized images for a professional look.

### STEP 11
Open the HTML file in a browser to check layout and functionality.

### STEP 12
Fix styling issues and refine content placement.

### STEP 13
Deploy the Portfolio.

### STEP 14
Upload to GitHub Pages for free hosting.

## PROGRAM
```
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Vidhyadharan R — Portfolio</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
  <style>
    :root{
      --bg:#0b0f1a; --panel:#111827; --muted:#94a3b8; --text:#e2e8f0; --brand:#22d3ee; --brand-2:#a78bfa; --ring:#334155;
    }
    *{box-sizing:border-box}
    html,body{height:100%}
    body{margin:0; font-family:Inter, system-ui, -apple-system, Segoe UI, Roboto, "Helvetica Neue", Arial, "Noto Sans", "Apple Color Emoji","Segoe UI Emoji"; color:var(--text); background:radial-gradient(1200px 600px at 10% 0%, #0f172a 0%, var(--bg) 60%), var(--bg);}
    a{color:inherit; text-decoration:none}
    .container{max-width:1100px; margin:0 auto; padding:0 20px}
    header{position:sticky; top:0; backdrop-filter:saturate(160%) blur(8px); background:rgba(11,15,26,0.6); border-bottom:1px solid var(--ring); z-index:10}
    nav{display:flex; align-items:center; justify-content:space-between; height:64px}
    .logo{display:flex; align-items:center; gap:10px; font-weight:800; letter-spacing:.2px}
    .logo .dot{width:10px; height:10px; border-radius:999px; background:linear-gradient(135deg,var(--brand),var(--brand-2)); box-shadow:0 0 18px rgba(34,211,238,.7)}
    .nav-links{display:flex; gap:18px; font-weight:600}
    .nav-links a{padding:8px 12px; border-radius:10px; color:var(--muted)}
    .nav-links a:hover{color:var(--text); background:rgba(148,163,184,.08)}

    .hero{padding:72px 0 32px}
    .grid{display:grid; gap:28px}
    .hero-grid{grid-template-columns:1.15fr .85fr; align-items:center}
    @media (max-width: 900px){ .hero-grid{grid-template-columns:1fr} }
    .badge{display:inline-flex; gap:8px; align-items:center; font-size:12px; font-weight:700; color:#0b1220; background:linear-gradient(135deg,var(--brand),var(--brand-2)); padding:6px 10px; border-radius:999px; letter-spacing:.2px}
    h1{font-size:40px; line-height:1.1; margin:14px 0}
    .subtitle{font-size:18px; color:var(--muted); max-width:52ch}
    .cta{margin-top:22px; display:flex; flex-wrap:wrap; gap:12px}
    .btn{display:inline-flex; gap:10px; align-items:center; padding:12px 16px; border:1px solid var(--ring); border-radius:12px; font-weight:700}
    .btn.primary{border-color:transparent; color:#08111b; background:linear-gradient(135deg,var(--brand),var(--brand-2))}
    .btn:hover{transform:translateY(-1px)}

    .card{background:linear-gradient(180deg, rgba(255,255,255,.03), rgba(255,255,255,.01)); border:1px solid var(--ring); border-radius:20px; padding:22px; display:flex; flex-direction:column; align-items:center}
    section{padding:24px 0}
    section h2{font-size:22px; letter-spacing:.3px}
    section .muted{color:var(--muted)}

    .two-col{display:grid; grid-template-columns:1fr 1fr; gap:18px}
    @media (max-width: 900px){ .two-col{grid-template-columns:1fr} }
    .chip{display:inline-flex; align-items:center; padding:6px 10px; border:1px solid var(--ring); border-radius:999px; gap:8px; color:var(--muted); font-weight:600; margin:6px 6px 0 0}
    .chip::before{content:""; width:8px; height:8px; border-radius:999px; background:linear-gradient(135deg,var(--brand),var(--brand-2))}

    ul.clean{list-style:none; padding:0; margin:0}
    .item{display:grid; grid-template-columns:auto 1fr; gap:14px; padding:14px 0; border-bottom:1px dashed var(--ring)}
    .item:last-child{border-bottom:none}
    .item time{color:var(--muted); font-weight:700; min-width:120px}
    .item h3{margin:0 0 6px; font-size:18px}
    .item p{margin:0; color:var(--muted)}
    .pill{display:inline-block; font-size:12px; font-weight:800; color:#07101a; padding:4px 10px; border-radius:999px; background:linear-gradient(135deg,var(--brand),var(--brand-2))}

    footer{padding:40px 0 60px; color:var(--muted)}
    .links{display:flex; flex-wrap:wrap; gap:10px}
    .avatar-img{width:120px; height:120px; border-radius:20px; border:1px solid var(--ring); object-fit:cover; max-width:100%}
  </style>
</head>
<body>
  <header>
    <div class="container">
      <nav>
        <div class="logo"><span class="dot"></span> <span>Vidhyadharan&nbsp;R</span></div>
        <div class="nav-links">
          <a href="#about">About</a>
          <a href="#skills">Skills</a>
          <a href="#experience">Experience</a>
          <a href="#projects">Projects</a>
          <a href="#education">Education</a>
          <a href="#achievements">Achievements</a>
          <a href="#contact">Contact</a>
        </div>
      </nav>
    </div>
  </header>

  <main>
    <section class="hero">
      <div class="container grid hero-grid">
        <div>
          <span class="badge">Backend & Java Developer</span>
          <h1>Building reliable backends and clean APIs.</h1>
          <p class="subtitle">Computer Science (IoT) student based in Chennai, focusing on Java, Spring Boot, SQL and scalable, data‑driven systems.</p>
          <div class="cta">
            <a class="btn primary" href="#contact">Contact me</a>
            <a class="btn" href="mailto:rvdharan31@gmail.com">rvdharan31@gmail.com</a>
            <a class="btn" href="https://linkedin.com/in/vidhyadharan-r" target="_blank" rel="noreferrer">LinkedIn</a>
            <a class="btn" href="https://github.com/vidhyadharan-03" target="_blank" rel="noreferrer">GitHub</a>
            <a class="btn" href="Vidhyadharan_Resume.pdf" download>Download CV</a>
          </div>
        </div>
        <div class="card">
          <img src="clg photo-min.jpg" alt="Vidhyadharan R" class="avatar-img">
          <p class="subtitle" style="margin-top:14px">Open to Backend Internships • Chennai, India</p>
        </div>
      </div>
    </section>

    <!-- About Section -->
    <section id="about">
      <div class="container">
        <div class="card">
          <h2>About</h2>
          <p class="muted">Motivated Computer Science (IoT) student with a strong foundation in backend development, OOP, and data‑driven application design. I enjoy building RESTful APIs in Java/Spring Boot and working with relational databases to deliver reliable features end‑to‑end.</p>
        </div>
      </div>
    </section>

    <!-- Skills Section -->
    <section id="skills">
      <div class="container">
        <div class="two-col">
          <div class="card">
            <h2>Skills</h2>
            <div>
              <span class="chip">Java</span>
              <span class="chip">Spring Boot</span>
              <span class="chip">Hibernate/JPA</span>
              <span class="chip">REST APIs</span>
              <span class="chip">MySQL</span>
              <span class="chip">JDBC</span>
              <span class="chip">OOP & OOD</span>
              <span class="chip">SOLID</span>
              <span class="chip">DSA</span>
              <span class="chip">Git & GitHub</span>
              <span class="chip">Postman</span>
              <span class="chip">Maven</span>
              <span class="chip">Python (basic)</span>
              <span class="chip">Streamlit</span>
              <span class="chip">Java Collections</span>
            </div>
          </div>
          <div class="card">
            <h2>What I’m focusing on</h2>
            <ul class="clean">
              <li class="item"><time>2025</time>
                <div>
                  <h3>Scalable backend patterns</h3>
                  <p>Layered architectures, LLD, and robust database design for production‑ready services.</p>
                </div>
              </li>
              <li class="item"><time>Now</time>
                <div>
                  <h3>Spring Boot + MySQL</h3>
                  <p>RESTful APIs, validation, JPA relationships, and integration testing.</p>
                </div>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </section>

    <!-- Experience Section -->
    <section id="experience">
      <div class="container">
        <div class="card">
          <h2>Experience</h2>
          <ul class="clean">
            <li class="item">
              <time>Jun–Jul 2024</time>
              <div>
                <h3>Mobile Application Developer Intern — Arjun Vision Tech Solution, Chennai</h3>
                <p>Built a Kotlin‑based Android math learning app with timed quizzes and scoring to improve engagement among primary‑school students. Followed clean architecture and user‑centric logic.</p>
              </div>
            </li>
          </ul>
        </div>
      </div>
    </section>

    <!-- Projects Section -->
    <section id="projects">
      <div class="container">
        <div class="card">
          <h2>Projects</h2>
          <ul class="clean">
            <li class="item">
              <time>Apr 2025</time>
              <div>
                <h3>FoodZone — Backend Food Ordering System <span class="pill">Spring Boot • MySQL</span></h3>
                <p>Designed RESTful APIs for menu, orders, and roles; implemented Hibernate/JPA and modular architecture for future frontend scalability.</p>
              </div>
            </li>
            <li class="item">
              <time>Mar 2025</time>
              <div>
                <h3>BookNest — Library Management System <span class="pill">Java • OOP • MVC</span></h3>
                <p>Console‑based system with SOLID principles; role‑based lending, returns, and inventory updates via layered MVC.</p>
              </div>
            </li>
            <li class="item">
              <time>Jan 2025</time>
              <div>
                <h3>Plan‑It‑Perfect — Event Management Portal <span class="pill">Java • JDBC • MySQL</span></h3>
                <p>Event booking with capacity constraints, profile management, and booking history.</p>
              </div>
            </li>
            <li class="item">
              <time>Nov 2024</time>
              <div>
                <h3>CML Prediction — Disease Detection App (ML) <span class="pill">Streamlit • ML</span></h3>
                <p>Model predicts Chronic Myelogenous Leukemia from blood test data for early, non‑invasive screening.</p>
              </div>
            </li>
          </ul>
        </div>
      </div>
    </section>

    <!-- Education & Achievements Section -->
    <section id="education">
      <div class="container">
        <div class="two-col">
          <div class="card">
            <h2>Education</h2>
            <ul class="clean">
              <li class="item">
                <time>2022–2026</time>
                <div>
                  <h3>B.E. Computer Science & Engineering (IoT) — Saveetha Engineering College</h3>
                  <p>GPA: 8.47 • Chennai, India</p>
                </div>
              </li>
              <li class="item">
                <time>2022</time>
                <div>
                  <h3>Higher Secondary — Kendriya Vidyalaya, Ashok Nagar</h3>
                </div>
              </li>
            </ul>
          </div>
          <div class="card" id="achievements">
            <h2>Achievements</h2>
            <ul class="clean">
              <li class="item">
                <time>Nov 2024</time>
                <div>
                  <h3>IBM Datathon — Global 3rd Place</h3>
                  <p>Built an ML‑powered fraud detection system under the “Technology for Good” theme; deployed on IBM LinuxOne to demonstrate enterprise‑grade scalability.</p>
                </div>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </section>

    <!-- Contact Section -->
    <section id="contact">
      <div class="container">
        <div class="card">
          <h2>Contact</h2>
          <p class="muted">I’m happy to connect for internships, backend roles, or Java/Spring collaborations.</p>
          <div class="links" style="margin-top:10px">
            <a class="btn" href="mailto:rvdharan31@gmail.com">📧&nbsp;rvdharan31@gmail.com</a>
            <a class="btn" href="tel:+919043280889">📱&nbsp;+91&nbsp;9043280889</a>
            <a class="btn" href="https://linkedin.com/in/vidhyadharan-r" target="_blank" rel="noreferrer">in/vidhyadharan-r</a>
            <a class="btn" href="https://github.com/vidhyadharan-03" target="_blank" rel="noreferrer">github.com/vidhyadharan-03</a>
          </div>
        </div>
      </div>
    </section>
  </main>

  <footer>
    <div class="container">© <span id="y"></span> Vidhyadharan R · Chennai, India</div>
  </footer>

  <script>document.getElementById('y').textContent=new Date().getFullYear()</script>
</body>
</html>
```

## OUTPUT
<img width="1883" height="977" alt="image" src="https://github.com/user-attachments/assets/5dc7cecc-aaa7-4d5d-9b47-7aaa6884b447" />
<img width="1918" height="956" alt="image" src="https://github.com/user-attachments/assets/6a60d0f8-f160-4b3a-834e-77533ba1c580" />
<img width="1911" height="969" alt="image" src="https://github.com/user-attachments/assets/c3e1a72c-c2f4-449f-b303-cf6b5a4844e1" />
<img width="1896" height="948" alt="image" src="https://github.com/user-attachments/assets/b97f67c8-df3f-4f15-b230-e706b9fbf320" />


## RESULT
The program for creating Portfolio using HTML and CSS is executed successfully.
