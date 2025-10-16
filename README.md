[style.css](https://github.com/user-attachments/files/22941563/style.css)<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Brooks Yu | Portfolio</title>
  <meta name="description" content="Brooks Yu (于溪铭) — CS Student @ University of Alberta. Web Development & Cybersecurity.">
  <link rel="icon" href="assets/avatar.jpg">
  <link rel="stylesheet" href="style.css" />
</head>
<body class="dark">
  <header class="nav">
    <a href="#home" class="brand">Brooks Yu<span class="muted"> / 于溪铭</span></a>
    <nav>
      <a href="#about">About / 关于</a>
      <a href="#projects">Projects / 项目</a>
      <a href="#contact">Contact / 联系</a>
      <button id="themeToggle" aria-label="Toggle dark mode">🌙</button>
    </nav>
  </header>

  <main id="home" class="hero">
    <img src="assets/avatar.jpg" alt="Avatar" class="avatar">
    <div class="intro">
      <h1><span id="typewriter"></span></h1>
      <p class="subtitle">CS Student @ <strong>University of Alberta</strong> · Web Development · Cybersecurity<br>
      阿尔伯塔大学计算机科学本科生 · Web 前端 · 网络安全</p>
      <div class="cta">
        <a class="btn" href="#projects">View Projects 查看项目</a>
        <a class="btn ghost" href="#contact">Get in touch 联系我</a>
      </div>
    </div>
  </main>

  <section id="about" class="section">
    <h2>About Me <span class="muted">/ 关于我</span></h2>
    <p>
      I’m Brooks (于溪铭), a CS student at UAlberta. I’m building a strong foundation in Python and modern web technologies,
      and exploring cybersecurity. This site will track my learning, projects, and growth.
      <br>
      我是 Brooks（于溪铭），阿尔伯塔大学计算机科学专业在读。正在夯实 Python 和现代 Web 技术，并深入了解网络安全。
      这个网站将持续记录我的学习、项目与成长。
    </p>
    <ul class="skills">
      <li>HTML/CSS/JavaScript</li>
      <li>Python (Flask/FastAPI)</li>
      <li>Git & GitHub</li>
      <li>Linux & CLI</li>
      <li>Cybersecurity basics</li>
    </ul>
  </section>

  <section id="projects" class="section">
    <h2>Projects <span class="muted">/ 项目</span></h2>
    <p class="muted">No public repos yet — placeholders below will be replaced soon. 暂无公开仓库，下列为占位卡片。</p>
    <div class="grid">
      <article class="card">
        <h3>python-mini-labs <span class="muted">（即将上线）</span></h3>
        <p>Small Python exercises to master basics. 一组小型 Python 实验，覆盖基础语法与文件操作。</p>
        <a href="#" class="link disabled" aria-disabled="true">Coming soon</a>
      </article>
      <article class="card">
        <h3>campus-helper <span class="muted">（即将上线）</span></h3>
        <p>UAlberta student tools: GPA calc, schedules. 校园助手：GPA 计算、课程与考试信息。</p>
        <a href="#" class="link disabled" aria-disabled="true">Coming soon</a>
      </article>
      <article class="card">
        <h3>crypto-utils <span class="muted">（即将上线）</span></h3>
        <p>Security-focused utilities (hashing, password gen). 安全工具合集（哈希、密码生成等）。</p>
        <a href="#" class="link disabled" aria-disabled="true">Coming soon</a>
      </article>
    </div>
  </section>

  <section id="contact" class="section">
    <h2>Contact <span class="muted">/ 联系</span></h2>
    <div class="contact">
      <p>📫 Email: <a href="mailto:especiallymaymars@gmail.com">especiallymaymars@gmail.com</a></p>
      <p>🐙 GitHub: <a href="https://github.com/brooks-yui21" target="_blank" rel="noopener">github.com/brooks-yui21</a></p>
      <p>📸 Instagram: <a href="https://www.instagram.com/brooks_yui21/" target="_blank" rel="noopener">@brooks_yui21</a></p>
    </div>
  </section>

  <button id="backToTop" aria-label="Back to top">▲</button>

  <footer class="footer">
    <p>© <span id="year"></span> Brooks Yu · Last updated <span id="lastUpdated"></span></p>
  </footer>

  <script src="script.js"></script>
</body>
</html>

[index.html](https://github.com/user-attachments/files/22941560/index.html)
[Uploadi/* ---------- Base ---------- */
:root {
  --bg: #0b0f14;
  --surface: #121821;
  --text: #e6edf3;
  --muted: #9fb0c3;
  --accent: #4ea8de;
  --accent-2: #9b5de5;
  --shadow: rgba(0,0,0,0.35);
}

* { box-sizing: border-box; }
html, body { margin: 0; padding: 0; font-family: ui-sans-serif, system-ui, -apple-system, Segoe UI, Roboto, Arial; color: var(--text); background: var(--bg); }

/* ---------- Nav ---------- */
.nav {
  position: sticky; top: 0; z-index: 10;
  display: flex; align-items: center; justify-content: space-between;
  padding: 14px 22px; background: rgba(18,24,33,0.7); backdrop-filter: blur(8px);
  border-bottom: 1px solid rgba(255,255,255,0.05);
}
.nav .brand { color: var(--text); text-decoration: none; font-weight: 700; letter-spacing: .2px; }
.nav .brand .muted { color: var(--muted); font-weight: 400; }
.nav nav a { color: var(--muted); text-decoration: none; margin-right: 16px; }
.nav nav a:hover { color: var(--text); }
#themeToggle { background: var(--surface); color: var(--text); border: 1px solid rgba(255,255,255,0.08); padding: 6px 10px; border-radius: 10px; cursor: pointer; }

/* ---------- Hero ---------- */
.hero {
  display: grid; grid-template-columns: 140px 1fr; gap: 24px;
  align-items: center; max-width: 980px; margin: 56px auto; padding: 0 20px;
}
.avatar { width: 140px; height: 140px; object-fit: cover; border-radius: 22px; box-shadow: 0 10px 24px var(--shadow); border: 1px solid rgba(255,255,255,0.08); }
.intro h1 { font-size: 32px; margin: 0 0 6px 0; }
.subtitle { color: var(--muted); margin-top: 8px; }
.cta { margin-top: 18px; }
.btn { background: var(--accent); color: #0b0f14; padding: 10px 14px; border-radius: 12px; text-decoration: none; font-weight: 600; margin-right: 10px; display: inline-block; }
.btn.ghost { background: transparent; color: var(--text); border: 1px solid rgba(255,255,255,0.12); }

/* ---------- Sections ---------- */
.section { max-width: 980px; margin: 28px auto; padding: 24px 20px; }
.section h2 { margin-top: 0; }
.muted { color: var(--muted); }

.skills { display: flex; flex-wrap: wrap; gap: 10px; padding-left: 0; list-style: none; }
.skills li { background: var(--surface); padding: 8px 12px; border-radius: 999px; border: 1px solid rgba(255,255,255,0.08); }

.grid { display: grid; grid-template-columns: repeat(3, minmax(0,1fr)); gap: 18px; }
.card { background: var(--surface); border: 1px solid rgba(255,255,255,0.08); border-radius: 16px; padding: 16px; box-shadow: 0 10px 24px var(--shadow); }
.card h3 { margin-top: 0; }
.card .link { color: var(--accent); text-decoration: none; font-weight: 600; }
.card .link.disabled { opacity: .5; pointer-events: none; }

/* ---------- Contact ---------- */
.contact p { margin: 6px 0; }

/* ---------- Back to top ---------- */
#backToTop {
  position: fixed; right: 18px; bottom: 18px; width: 38px; height: 38px;
  border-radius: 10px; border: none; background: var(--accent-2); color: #fff;
  cursor: pointer; display: none; box-shadow: 0 10px 24px var(--shadow);
}

/* ---------- Footer ---------- */
.footer { text-align: center; color: var(--muted); padding: 28px 0 40px; border-top: 1px solid rgba(255,255,255,0.06); margin-top: 28px; }

/* ---------- Responsive ---------- */
@media (max-width: 720px) {
  .hero { grid-template-columns: 1fr; text-align: center; }
  .avatar { margin: 0 auto; }
  .grid { grid-template-columns: 1fr; }
  .nav nav a { margin-right: 10px; }
}
ng style.css…]()
[script.js](https://github.com/user-attachments/files/22941569/script.js)
// ---- Typing effect ----
const strings = [
  "Hi, I’m Brooks — Web Dev & Cybersecurity.",
  "你好，我是于溪铭 —— Web 开发 & 网络安全。"
];
const el = document.getElementById("typewriter");
let si = 0, ci = 0, deleting = false;
function type() {
  if (!el) return;
  const full = strings[si];
  if (!deleting) {
    el.textContent = full.slice(0, ++ci);
    if (ci === full.length) { deleting = true; setTimeout(type, 1500); return; }
    setTimeout(type, 28);
  } else {
    el.textContent = full.slice(0, --ci);
    if (ci === 0) { deleting = false; si = (si + 1) % strings.length; }
    setTimeout(type, 18);
  }
}
type();

// ---- Theme toggle (persist) ----
const toggle = document.getElementById("themeToggle");
const root = document.documentElement;
const stored = localStorage.getItem("theme");
if (stored) document.body.className = stored;
toggle?.addEventListener("click", () => {
  const next = document.body.classList.contains("dark") ? "light" : "dark";
  document.body.className = next;
  localStorage.setItem("theme", next);
  toggle.textContent = next === "dark" ? "🌙" : "☀️";
});

// ---- Smooth scroll ----
document.querySelectorAll('a[href^="#"]').forEach(a => {
  a.addEventListener("click", e => {
    const id = a.getAttribute("href").slice(1);
    const t = document.getElementById(id);
    if (t) { e.preventDefault(); t.scrollIntoView({ behavior: "smooth", block: "start" }); }
  });
});

// ---- Back to top ----
const backBtn = document.getElementById("backToTop");
window.addEventListener("scroll", () => {
  backBtn.style.display = window.scrollY > 400 ? "block" : "none";
});
backBtn.addEventListener("click", () => window.scrollTo({ top: 0, behavior: "smooth" }));

// ---- Footer meta ----
document.getElementById("year").textContent = new Date().getFullYear();
document.getElementById("lastUpdated").textContent = new Date(document.lastModified).toLocaleDateString();

[README.md](https://github.com/user-attachments/files/22941572/README.md)
# Brooks Portfolio

A bilingual (EN/中文) technical-style portfolio for **Brooks Yu / 于溪铭**.

## Features
- Dark/Light theme toggle (persisted to localStorage)
- Typewriter intro (EN/中文)
- Smooth anchor scrolling & back-to-top
- Responsive layout (mobile friendly)
- Placeholder project cards for easy future updates

## How to run locally
Open `index.html` in your browser.

## How to deploy to GitHub Pages
1. Create a public repo named `brooks-portfolio` (or any name).
2. Upload all files in this folder.
3. In GitHub: **Settings → Pages → Source: Deploy from a branch**, select `main` and `/ (root)`.
4. Wait for the green check, then your site will be live at:  
   `https://<your-username>.github.io/<repo-name>/`  
   (or use the special repo `brooks-yui21.github.io` to host at root domain).

## Edit content
- Text: edit `index.html`
- Styles: `style.css`
- Behaviors: `script.js`
- Avatar: replace `assets/avatar.jpg` with your image (keep the same file name).
![avatar](https://github.com/user-attachments/assets/16806393-36f8-411c-baf6-184ed072f8e7)



