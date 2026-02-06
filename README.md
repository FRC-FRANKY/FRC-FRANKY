<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Frank Oliver Bentoy | Portfolio</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />

  <!-- Material Icons -->
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&display=swap" rel="stylesheet">

  <style>
    *{box-sizing:border-box;margin:0;padding:0;font-family:'Inter',sans-serif}

    body{
      background:#f8fafc;
      color:#1f2933;
      line-height:1.6;
    }

    header{
      background:white;
      padding:60px 20px;
    }

    .container{
      max-width:1100px;
      margin:auto;
    }

    .hero{
      display:grid;
      grid-template-columns:1fr 1fr;
      gap:40px;
      align-items:center;
    }

    h1{font-size:42px;margin-bottom:10px}
    h2{font-size:28px;margin-bottom:20px}
    h3{margin-bottom:10px}

    .subtitle{
      color:#64748b;
      font-weight:600;
      margin-bottom:16px;
    }

    .btns a{
      display:inline-block;
      padding:10px 16px;
      border-radius:10px;
      border:1px solid #cbd5e1;
      margin-right:10px;
      text-decoration:none;
      color:#0f172a;
      font-weight:600;
      transition:.2s;
    }

    .btns a.primary{
      background:#0f172a;
      color:white;
      border:none;
    }

    .btns a:hover{transform:translateY(-2px)}

    section{
      padding:70px 20px;
    }

    .card-grid{
      display:grid;
      grid-template-columns:repeat(auto-fit,minmax(260px,1fr));
      gap:20px;
    }

    .card{
      background:white;
      padding:22px;
      border-radius:18px;
      box-shadow:0 10px 20px rgba(0,0,0,.05);
    }

    ul{list-style:none}

    ul li{margin-bottom:6px;color:#475569}

    .projects-grid{
      display:grid;
      grid-template-columns:repeat(auto-fit,minmax(300px,1fr));
      gap:20px;
    }

    .muted{color:#64748b;font-size:14px}

    footer{
      background:#0f172a;
      color:white;
      text-align:center;
      padding:40px 20px;
    }

    @media(max-width:768px){
      .hero{grid-template-columns:1fr}
      h1{font-size:34px}
    }
  </style>
</head>
<body>

<header>
  <div class="container hero">
    <div>
      <h1>Frank Oliver Narag Bentoy</h1>
      <div class="subtitle">Web Developer</div>
      <p>
        I am a dedicated Web Developer with a strong background in programming. I specialize in building efficient and scalable
        applications using ASP.NET, Razor Pages, and database‑driven systems. I enjoy learning new technologies and creating
        solutions that make a real‑world impact.
      </p>

      <div class="btns" style="margin-top:20px">
        <a class="primary" href="mailto:frankoliverbentoy@gmail.com">Contact Me</a>
        <a href="https://github.com/FRC_FRANKY" target="_blank">GitHub</a>
        <a href="https://www.linkedin.com/in/frank-oliver-bentoy-33b116238" target="_blank">LinkedIn</a>
      </div>
    </div>
  </div>
</header>

<section>
  <div class="container">
    <h2>About Me</h2>
    <p>
      I am currently taking Bachelor of Science in Information Technology at the University of Cebu – Banilad. I have experience
      working on academic and personal projects such as web systems, games, and IoT applications. My main focus is backend and
      full‑stack web development, particularly using ASP.NET and database technologies.
    </p>
  </div>
</section>

<section>
  <div class="container">
    <h2>Technical Skills</h2>

    <div class="card-grid">
      <div class="card">
        <h3>Languages & Frameworks</h3>
        <ul id="languages"></ul>
      </div>

      <div class="card">
        <h3>Frontend & UI</h3>
        <ul id="frontend"></ul>
      </div>

      <div class="card">
        <h3>Databases, Cloud & Tools</h3>
        <ul id="tools"></ul>
      </div>
    </div>
  </div>
</section>

<section>
  <div class="container">
    <h2>Projects</h2>

    <div class="projects-grid" id="projects"></div>
  </div>
</section>

<section>
  <div class="container" style="display:grid;grid-template-columns:1fr 1fr;gap:40px">

    <div>
      <h2>Education</h2>
      <p><strong>Bachelor of Science in Information Technology</strong></p>
      <p class="muted">University of Cebu – Banilad</p>
      <p class="muted">2021 – Present</p>
    </div>

    <div>
      <h2>Experience</h2>
      <p><strong>Project Manager – School Project</strong></p>
      <p class="muted">September 2024 – December 2024</p>
      <p style="margin-top:10px">
        Worked with a development team on web-based projects using ASP.NET, SQL Server, and MySQL while helping manage tasks
        and timelines.
      </p>
    </div>

  </div>
</section>

<footer>
  <p><strong>Frank Oliver Narag Bentoy</strong></p>
  <p>Cebu, Philippines</p>
  <p>frankoliverbentoy@gmail.com | +63 956 077 2456</p>
</footer>

<script>
  const skills = {
    languages: ["Java", "JavaScript", "React", "C#", "C++", "PHP", "IoT"],
    frontend: ["HTML5", "CSS3", "Material UI"],
    tools: ["MySQL", "Firebase", "Git"]
  };

  const projects = [
    {
      title: "Enrollment System",
      date: "09/2024 – 11/2024",
      description: "A comprehensive enrollment system developed using ASP.NET with Razor Pages and SQL Server for secure and reliable data management."
    },
    {
      title: "Boy Cabbage Web Game",
      date: "01/2023 – 05/2023",
      description: "A 2D platform web game where players guide a character through levels filled with challenges, obstacles, and enemies."
    },
    {
      title: "JobFilter",
      date: "08/2025 – 12/2025",
      description: "A PHP-based job matching platform that connects job seekers with relevant job listings based on skills, experience, and preferences."
    },
    {
      title: "Cuppa: Your Coffee, Your Way",
      date: "08/2025 – 12/2025",
      description: "An IoT-enabled smart coffee brewing system with Android integration for remote brewing, scheduling, and real-time alerts."
    }
  ];

  function renderList(id, items){
    const ul = document.getElementById(id);
    items.forEach(i => {
      const li = document.createElement('li');
      li.textContent = "• " + i;
      ul.appendChild(li);
    });
  }

  renderList('languages', skills.languages);
  renderList('frontend', skills.frontend);
  renderList('tools', skills.tools);

  const projectContainer = document.getElementById('projects');

  projects.forEach(p => {
    const card = document.createElement('div');
    card.className = 'card';

    card.innerHTML = `
      <h3>${p.title}</h3>
      <p class="muted">${p.date}</p>
      <p style="margin-top:10px">${p.description}</p>
    `;

    projectContainer.appendChild(card);
  });
</script>

</body>
</html>
