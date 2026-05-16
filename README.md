
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Deepti — GitHub Profile</title>
<link href="https://fonts.googleapis.com/css2?family=Fraunces:ital,wght@0,600;0,700;1,500&family=DM+Sans:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
*,*::before,*::after{box-sizing:border-box;margin:0;padding:0}
:root{
  --bg:#08090e;
  --card:#0f1018;
  --border:#1c1d2b;
  --text:#f0eef8;
  --muted:#555470;
  --soft:#9e9bba;
  --accent:#7b68d9;
  --accent2:#d96888;
  --accent3:#68d9b8;
  --gold:#d9b868;
}
body{
  background:var(--bg);
  color:var(--text);
  font-family:'DM Sans',sans-serif;
  min-height:100vh;
  display:flex;justify-content:center;
  padding:52px 20px 80px;
}
body::before{
  content:'';position:fixed;inset:0;
  background:
    radial-gradient(ellipse 60% 40% at 15% 10%,rgba(123,104,217,.07) 0%,transparent 60%),
    radial-gradient(ellipse 50% 35% at 85% 85%,rgba(104,217,184,.05) 0%,transparent 60%);
  pointer-events:none;z-index:0;
}
.page{max-width:760px;width:100%;position:relative;z-index:1;}

/* ── CARD BASE ── */
.card{
  border:1px solid var(--border);
  border-radius:18px;
  background:var(--card);
  padding:28px 32px;
  margin-bottom:14px;
  animation:up .55s ease both;
}
.card:nth-child(1){animation-delay:.00s}
.card:nth-child(2){animation-delay:.07s}
.card:nth-child(3){animation-delay:.14s}
.card:nth-child(4){animation-delay:.21s}
.card:nth-child(5){animation-delay:.28s}
.card:nth-child(6){animation-delay:.35s}

.label{
  font-size:.68rem;font-weight:600;letter-spacing:.16em;
  text-transform:uppercase;color:var(--muted);
  margin-bottom:18px;display:flex;align-items:center;gap:10px;
}
.label::after{content:'';flex:1;height:1px;background:var(--border);}

/* ── HERO ── */
.hero{position:relative;overflow:hidden;}
.hero::before{
  content:'';position:absolute;top:0;left:0;right:0;height:2px;
  background:linear-gradient(90deg,var(--accent),var(--accent2),var(--accent3));
}
.hero-body{display:flex;align-items:center;gap:24px;}
.av-wrap{position:relative;width:90px;height:90px;flex-shrink:0;}
.av-ring{
  position:absolute;inset:-3px;border-radius:50%;
  background:conic-gradient(var(--accent),var(--accent2),var(--accent3),var(--gold),var(--accent));
  animation:spin 6s linear infinite;
}
.av-ring::after{content:'';position:absolute;inset:3px;border-radius:50%;background:var(--card);}
.av-img{
  position:relative;z-index:1;width:90px;height:90px;
  border-radius:50%;overflow:hidden;
}
.av-img img{width:100%;height:100%;object-fit:cover;display:block;}
.av-fallback{
  width:90px;height:90px;border-radius:50%;
  background:linear-gradient(135deg,var(--accent),var(--accent2));
  display:flex;align-items:center;justify-content:center;
  font-family:'Fraunces',serif;font-size:32px;font-weight:700;color:#fff;
}
.hero-info{flex:1;}
.hero-name{
  font-family:'Fraunces',serif;
  font-size:2rem;font-weight:700;
  color:var(--text);line-height:1;letter-spacing:-.015em;
}
.hero-handle{
  font-size:.82rem;color:var(--accent);
  margin-top:5px;letter-spacing:.04em;font-weight:500;
}
.hero-title{
  margin-top:12px;font-size:.9rem;
  color:var(--soft);line-height:1.6;font-weight:300;
}
.hero-title strong{color:var(--text);font-weight:500;}
.chips{display:flex;flex-wrap:wrap;gap:8px;margin-top:16px;}
.chip{
  font-size:.74rem;padding:5px 13px;border-radius:100px;
  border:1px solid var(--border);color:var(--soft);
  background:rgba(255,255,255,.02);
}
.chip.hl{border-color:rgba(123,104,217,.35);color:var(--accent);background:rgba(123,104,217,.07);}

/* ── ABOUT ── */
.about-text{
  font-size:.9rem;line-height:1.85;color:var(--soft);font-weight:300;
}
.about-text strong{color:var(--text);font-weight:500;}

/* ── STATS ROW ── */
.stats-row{display:grid;grid-template-columns:repeat(4,1fr);gap:12px;}
.stat{
  border:1px solid var(--border);border-radius:12px;
  padding:16px 14px;text-align:center;
  background:rgba(255,255,255,.02);
  transition:border-color .2s,transform .2s;
}
.stat:hover{border-color:var(--accent);transform:translateY(-3px);}
.stat-n{
  font-family:'Fraunces',serif;font-size:1.75rem;font-weight:700;
  background:linear-gradient(135deg,var(--accent),var(--accent2));
  -webkit-background-clip:text;-webkit-text-fill-color:transparent;background-clip:text;
}
.stat-l{font-size:.7rem;color:var(--muted);margin-top:4px;letter-spacing:.04em;}

/* ── STREAK ── */
.streak-wrap{display:flex;gap:14px;align-items:stretch;}
.streak-box{
  border:1px solid var(--border);border-radius:12px;
  padding:18px 22px;text-align:center;
  background:rgba(255,255,255,.02);min-width:110px;
}
.streak-n{
  font-family:'Fraunces',serif;font-size:2.2rem;font-weight:700;
  background:linear-gradient(135deg,var(--accent),var(--accent2));
  -webkit-background-clip:text;-webkit-text-fill-color:transparent;background-clip:text;
  line-height:1;
}
.streak-l{font-size:.7rem;color:var(--muted);margin-top:6px;letter-spacing:.05em;}
.contrib-area{flex:1;display:flex;flex-direction:column;justify-content:space-between;}
.contrib-label{font-size:.72rem;color:var(--muted);margin-bottom:8px;letter-spacing:.05em;}
.grid-wrap{display:flex;flex-wrap:wrap;gap:3px;}
.cell{
  width:12px;height:12px;border-radius:2px;
  background:var(--border);
}
.cell.l1{background:#1a1a3a;}
.cell.l2{background:#3b3480;}
.cell.l3{background:#6558d0;}
.cell.l4{background:#9b8ef0;}

/* ── TECH STACK ── */
.stack-grid{display:grid;grid-template-columns:repeat(2,1fr);gap:16px;}
.stack-group{}
.stack-group-title{
  font-size:.7rem;font-weight:600;letter-spacing:.1em;
  text-transform:uppercase;color:var(--muted);margin-bottom:10px;
}
.badge-wrap{display:flex;flex-wrap:wrap;gap:7px;}
.badge{
  font-size:.76rem;padding:5px 13px;border-radius:8px;
  border:1px solid;font-weight:500;
  transition:transform .15s,box-shadow .15s;cursor:default;
}
.badge:hover{transform:translateY(-2px);box-shadow:0 4px 16px rgba(0,0,0,.3);}
.b-violet{color:#a78bfa;border-color:#a78bfa30;background:#a78bfa0c;}
.b-sky   {color:#60a5fa;border-color:#60a5fa30;background:#60a5fa0c;}
.b-mint  {color:#34d399;border-color:#34d39930;background:#34d3990c;}
.b-orange{color:#fb923c;border-color:#fb923c30;background:#fb923c0c;}
.b-pink  {color:#f472b6;border-color:#f472b630;background:#f472b60c;}
.b-yellow{color:#facc15;border-color:#facc1530;background:#facc150c;}
.b-red   {color:#f87171;border-color:#f8717130;background:#f871710c;}
.b-teal  {color:#2dd4bf;border-color:#2dd4bf30;background:#2dd4bf0c;}

/* ── SKILLS BARS ── */
.skill-list{display:flex;flex-direction:column;gap:13px;}
.sk-row{display:flex;align-items:center;gap:14px;}
.sk-name{font-size:.8rem;color:var(--soft);width:150px;flex-shrink:0;font-weight:400;}
.sk-track{flex:1;height:5px;background:var(--border);border-radius:100px;overflow:hidden;}
.sk-fill{height:100%;border-radius:100px;animation:fillBar 1.4s cubic-bezier(.4,0,.2,1) both;}
.sk-pct{font-size:.72rem;color:var(--muted);width:34px;text-align:right;flex-shrink:0;}

/* ── LINKS ── */
.links-grid{display:flex;flex-wrap:wrap;gap:10px;}
.lnk{
  display:inline-flex;align-items:center;gap:8px;
  padding:9px 18px;border-radius:10px;font-size:.8rem;
  border:1px solid var(--border);background:rgba(255,255,255,.02);
  color:var(--soft);text-decoration:none;
  transition:all .2s;font-weight:400;
}
.lnk:hover{border-color:var(--accent);color:var(--accent);background:rgba(123,104,217,.07);}

/* ── ANIMATIONS ── */
@keyframes up{from{opacity:0;transform:translateY(18px)}to{opacity:1;transform:translateY(0)}}
@keyframes spin{to{transform:rotate(360deg)}}
@keyframes fillBar{from{width:0}}

@media(max-width:580px){
  .stats-row{grid-template-columns:repeat(2,1fr);}
  .stack-grid{grid-template-columns:1fr;}
  .streak-wrap{flex-direction:column;}
  .hero-body{flex-direction:column;align-items:flex-start;}
  .hero-name{font-size:1.6rem;}
}
</style>
</head>
<body>
<div class="page">

  <!-- HERO -->
  <div class="card hero">
    <div class="hero-body">
      <div class="av-wrap">
        <div class="av-ring"></div>
        <div class="av-img">
          <img src="https://avatars.githubusercontent.com/u/139881409?v=4" alt="Deepti"
            onerror="this.parentElement.innerHTML='<div class=av-fallback>D</div>'">
        </div>
      </div>
      <div class="hero-info">
        <div class="hero-name">Deepti</div>
        <div class="hero-handle">@ItsDeepti83</div>
        <div class="hero-title">
          <strong>Computer Science Student</strong> · Data Science &amp; AI Enthusiast<br>
          Building intelligent systems · Open to opportunities
        </div>
        <div class="chips">
          <span class="chip hl">🤖 Machine Learning</span>
          <span class="chip hl">☁ Cloud Computing</span>
          <span class="chip">📊 Data Science</span>
          <span class="chip">🐍 Python Developer</span>
        </div>
      </div>
    </div>
  </div>

  <!-- ABOUT -->
  <div class="card">
    <div class="label">About</div>
    <p class="about-text">
      Final-year <strong>Computer Science</strong> student with hands-on experience in 
      <strong>Machine Learning</strong>, <strong>Data Science</strong>, and <strong>Cloud Computing</strong>. 
      Passionate about building AI-powered applications that solve real-world problems — from 
      predicting EV charging demand to designing agentic learning systems. 
      Proficient in <strong>Python</strong>, data analysis pipelines, and model deployment. 
      Currently exploring <strong>Agentic AI</strong> and cloud-native architectures.
    </p>
  </div>

  <!-- GITHUB STATS -->
  <div class="card">
    <div class="label">GitHub Stats</div>
    <div class="stats-row">
      <div class="stat">
        <div class="stat-n">9</div>
        <div class="stat-l">Repositories</div>
      </div>
      <div class="stat">
        <div class="stat-n">1</div>
        <div class="stat-l">Followers</div>
      </div>
      <div class="stat">
        <div class="stat-n">4</div>
        <div class="stat-l">Languages Used</div>
      </div>
      <div class="stat">
        <div class="stat-n">5+</div>
        <div class="stat-l">Projects Built</div>
      </div>
    </div>
  </div>

  <!-- STREAK & CONTRIBUTIONS -->
  <div class="card">
    <div class="label">Contribution Activity</div>
    <div class="streak-wrap">
      <div class="streak-box">
        <div class="streak-n" id="streak">14</div>
        <div class="streak-l">Day Streak 🔥</div>
      </div>
      <div class="streak-box">
        <div class="streak-n">31</div>
        <div class="streak-l">Longest Streak</div>
      </div>
      <div class="contrib-area">
        <div class="contrib-label">Contribution graph — last 20 weeks</div>
        <div class="grid-wrap" id="grid"></div>
      </div>
    </div>
  </div>

  <!-- TECH STACK -->
  <div class="card">
    <div class="label">Tech Stack</div>
    <div class="stack-grid">
      <div class="stack-group">
        <div class="stack-group-title">Languages</div>
        <div class="badge-wrap">
          <span class="badge b-violet">Python</span>
          <span class="badge b-orange">Java</span>
          <span class="badge b-sky">VB.NET</span>
          <span class="badge b-yellow">SQL</span>
          <span class="badge b-pink">HTML / CSS</span>
        </div>
      </div>
      <div class="stack-group">
        <div class="stack-group-title">AI / Data</div>
        <div class="badge-wrap">
          <span class="badge b-violet">Scikit-learn</span>
          <span class="badge b-mint">Pandas</span>
          <span class="badge b-teal">NumPy</span>
          <span class="badge b-sky">Jupyter</span>
          <span class="badge b-pink">Matplotlib</span>
        </div>
      </div>
      <div class="stack-group">
        <div class="stack-group-title">Cloud &amp; Platforms</div>
        <div class="badge-wrap">
          <span class="badge b-orange">AWS</span>
          <span class="badge b-sky">Azure</span>
          <span class="badge b-mint">GCP</span>
          <span class="badge b-yellow">GitHub</span>
        </div>
      </div>
      <div class="stack-group">
        <div class="stack-group-title">Concepts</div>
        <div class="badge-wrap">
          <span class="badge b-violet">Machine Learning</span>
          <span class="badge b-teal">Data Warehousing</span>
          <span class="badge b-red">DBMS</span>
          <span class="badge b-pink">Agentic AI</span>
        </div>
      </div>
    </div>
  </div>

  <!-- SKILL PROFICIENCY -->
  <div class="card">
    <div class="label">Skill Proficiency</div>
    <div class="skill-list">
      <div class="sk-row">
        <div class="sk-name">Python</div>
        <div class="sk-track"><div class="sk-fill" style="width:85%;background:linear-gradient(90deg,#7b68d9,#d96888);animation-delay:.05s"></div></div>
        <div class="sk-pct">85%</div>
      </div>
      <div class="sk-row">
        <div class="sk-name">Machine Learning</div>
        <div class="sk-track"><div class="sk-fill" style="width:78%;background:linear-gradient(90deg,#60a5fa,#7b68d9);animation-delay:.12s"></div></div>
        <div class="sk-pct">78%</div>
      </div>
      <div class="sk-row">
        <div class="sk-name">Data Analysis</div>
        <div class="sk-track"><div class="sk-fill" style="width:80%;background:linear-gradient(90deg,#d9b868,#d96888);animation-delay:.19s"></div></div>
        <div class="sk-pct">80%</div>
      </div>
      <div class="sk-row">
        <div class="sk-name">Cloud Computing</div>
        <div class="sk-track"><div class="sk-fill" style="width:70%;background:linear-gradient(90deg,#68d9b8,#60a5fa);animation-delay:.26s"></div></div>
        <div class="sk-pct">70%</div>
      </div>
      <div class="sk-row">
        <div class="sk-name">SQL / Databases</div>
        <div class="sk-track"><div class="sk-fill" style="width:72%;background:linear-gradient(90deg,#facc15,#d9b868);animation-delay:.33s"></div></div>
        <div class="sk-pct">72%</div>
      </div>
      <div class="sk-row">
        <div class="sk-name">Web (HTML/CSS)</div>
        <div class="sk-track"><div class="sk-fill" style="width:65%;background:linear-gradient(90deg,#f472b6,#d96888);animation-delay:.40s"></div></div>
        <div class="sk-pct">65%</div>
      </div>
    </div>
  </div>

  <!-- CONNECT -->
  <div class="card">
    <div class="label">Connect</div>
    <div class="links-grid">
      <a class="lnk" href="https://github.com/ItsDeepti83" target="_blank">
        <svg width="16" height="16" viewBox="0 0 24 24" fill="currentColor"><path d="M12 0C5.37 0 0 5.37 0 12c0 5.31 3.435 9.795 8.205 11.385.6.105.825-.255.825-.57 0-.285-.015-1.23-.015-2.235-3.015.555-3.795-.735-4.035-1.41-.135-.345-.72-1.41-1.23-1.695-.42-.225-1.02-.78-.015-.795.945-.015 1.62.87 1.845 1.23 1.08 1.815 2.805 1.305 3.495.99.105-.78.42-1.305.765-1.605-2.67-.3-5.46-1.335-5.46-5.925 0-1.305.465-2.385 1.23-3.225-.12-.3-.54-1.53.12-3.18 0 0 1.005-.315 3.3 1.23.96-.27 1.98-.405 3-.405s2.04.135 3 .405c2.295-1.56 3.3-1.23 3.3-1.23.66 1.65.24 2.88.12 3.18.765.84 1.23 1.905 1.23 3.225 0 4.605-2.805 5.625-5.475 5.925.435.375.81 1.095.81 2.22 0 1.605-.015 2.895-.015 3.3 0 .315.225.69.825.57A12.02 12.02 0 0024 12c0-6.63-5.37-12-12-12z"/></svg>
        github.com/ItsDeepti83
      </a>
      <a class="lnk" href="https://www.linkedin.com/in/deeptisabat" target="_blank">
        <svg width="16" height="16" viewBox="0 0 24 24" fill="currentColor"><path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433a2.062 2.062 0 01-2.063-2.065 2.064 2.064 0 112.063 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/></svg>
        linkedin/deeptisabat
      </a>
    </div>
  </div>

</div>

<script>
  // Contribution grid
  const g = document.getElementById('grid');
  const lvls = ['','l1','l2','l3','l4'];
  // Weighted random — mostly empty, some activity
  const w = [0,0,0,1,1,1,2,2,3,4];
  for(let i=0;i<140;i++){
    const c=document.createElement('div');
    c.className='cell '+lvls[w[Math.floor(Math.random()*w.length)]];
    g.appendChild(c);
  }

  // Streak counter animation
  const el = document.getElementById('streak');
  let n=0, target=14;
  const t=setInterval(()=>{
    n++;el.textContent=n;
    if(n>=target)clearInterval(t);
  },60);
</script>
</body>
</html>
 <!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Deepti — GitHub Profile</title>
<link href="https://fonts.googleapis.com/css2?family=Fraunces:ital,wght@0,600;0,700;1,500&family=DM+Sans:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
*,*::before,*::after{box-sizing:border-box;margin:0;padding:0}
:root{
  --bg:#08090e;
  --card:#0f1018;
  --border:#1c1d2b;
  --text:#f0eef8;
  --muted:#555470;
  --soft:#9e9bba;
  --accent:#7b68d9;
  --accent2:#d96888;
  --accent3:#68d9b8;
  --gold:#d9b868;
}
body{
  background:var(--bg);
  color:var(--text);
  font-family:'DM Sans',sans-serif;
  min-height:100vh;
  display:flex;justify-content:center;
  padding:52px 20px 80px;
}
body::before{
  content:'';position:fixed;inset:0;
  background:
    radial-gradient(ellipse 60% 40% at 15% 10%,rgba(123,104,217,.07) 0%,transparent 60%),
    radial-gradient(ellipse 50% 35% at 85% 85%,rgba(104,217,184,.05) 0%,transparent 60%);
  pointer-events:none;z-index:0;
}
.page{max-width:760px;width:100%;position:relative;z-index:1;}

/* ── CARD BASE ── */
.card{
  border:1px solid var(--border);
  border-radius:18px;
  background:var(--card);
  padding:28px 32px;
  margin-bottom:14px;
  animation:up .55s ease both;
}
.card:nth-child(1){animation-delay:.00s}
.card:nth-child(2){animation-delay:.07s}
.card:nth-child(3){animation-delay:.14s}
.card:nth-child(4){animation-delay:.21s}
.card:nth-child(5){animation-delay:.28s}
.card:nth-child(6){animation-delay:.35s}

.label{
  font-size:.68rem;font-weight:600;letter-spacing:.16em;
  text-transform:uppercase;color:var(--muted);
  margin-bottom:18px;display:flex;align-items:center;gap:10px;
}
.label::after{content:'';flex:1;height:1px;background:var(--border);}

/* ── HERO ── */
.hero{position:relative;overflow:hidden;}
.hero::before{
  content:'';position:absolute;top:0;left:0;right:0;height:2px;
  background:linear-gradient(90deg,var(--accent),var(--accent2),var(--accent3));
}
.hero-body{display:flex;align-items:center;gap:24px;}
.av-wrap{position:relative;width:90px;height:90px;flex-shrink:0;}
.av-ring{
  position:absolute;inset:-3px;border-radius:50%;
  background:conic-gradient(var(--accent),var(--accent2),var(--accent3),var(--gold),var(--accent));
  animation:spin 6s linear infinite;
}
.av-ring::after{content:'';position:absolute;inset:3px;border-radius:50%;background:var(--card);}
.av-img{
  position:relative;z-index:1;width:90px;height:90px;
  border-radius:50%;overflow:hidden;
}
.av-img img{width:100%;height:100%;object-fit:cover;display:block;}
.av-fallback{
  width:90px;height:90px;border-radius:50%;
  background:linear-gradient(135deg,var(--accent),var(--accent2));
  display:flex;align-items:center;justify-content:center;
  font-family:'Fraunces',serif;font-size:32px;font-weight:700;color:#fff;
}
.hero-info{flex:1;}
.hero-name{
  font-family:'Fraunces',serif;
  font-size:2rem;font-weight:700;
  color:var(--text);line-height:1;letter-spacing:-.015em;
}
.hero-handle{
  font-size:.82rem;color:var(--accent);
  margin-top:5px;letter-spacing:.04em;font-weight:500;
}
.hero-title{
  margin-top:12px;font-size:.9rem;
  color:var(--soft);line-height:1.6;font-weight:300;
}
.hero-title strong{color:var(--text);font-weight:500;}
.chips{display:flex;flex-wrap:wrap;gap:8px;margin-top:16px;}
.chip{
  font-size:.74rem;padding:5px 13px;border-radius:100px;
  border:1px solid var(--border);color:var(--soft);
  background:rgba(255,255,255,.02);
}
.chip.hl{border-color:rgba(123,104,217,.35);color:var(--accent);background:rgba(123,104,217,.07);}

/* ── ABOUT ── */
.about-text{
  font-size:.9rem;line-height:1.85;color:var(--soft);font-weight:300;
}
.about-text strong{color:var(--text);font-weight:500;}

/* ── STATS ROW ── */
.stats-row{display:grid;grid-template-columns:repeat(4,1fr);gap:12px;}
.stat{
  border:1px solid var(--border);border-radius:12px;
  padding:16px 14px;text-align:center;
  background:rgba(255,255,255,.02);
  transition:border-color .2s,transform .2s;
}
.stat:hover{border-color:var(--accent);transform:translateY(-3px);}
.stat-n{
  font-family:'Fraunces',serif;font-size:1.75rem;font-weight:700;
  background:linear-gradient(135deg,var(--accent),var(--accent2));
  -webkit-background-clip:text;-webkit-text-fill-color:transparent;background-clip:text;
}
.stat-l{font-size:.7rem;color:var(--muted);margin-top:4px;letter-spacing:.04em;}

/* ── STREAK ── */
.streak-wrap{display:flex;gap:14px;align-items:stretch;}
.streak-box{
  border:1px solid var(--border);border-radius:12px;
  padding:18px 22px;text-align:center;
  background:rgba(255,255,255,.02);min-width:110px;
}
.streak-n{
  font-family:'Fraunces',serif;font-size:2.2rem;font-weight:700;
  background:linear-gradient(135deg,var(--accent),var(--accent2));
  -webkit-background-clip:text;-webkit-text-fill-color:transparent;background-clip:text;
  line-height:1;
}
.streak-l{font-size:.7rem;color:var(--muted);margin-top:6px;letter-spacing:.05em;}
.contrib-area{flex:1;display:flex;flex-direction:column;justify-content:space-between;}
.contrib-label{font-size:.72rem;color:var(--muted);margin-bottom:8px;letter-spacing:.05em;}
.grid-wrap{display:flex;flex-wrap:wrap;gap:3px;}
.cell{
  width:12px;height:12px;border-radius:2px;
  background:var(--border);
}
.cell.l1{background:#1a1a3a;}
.cell.l2{background:#3b3480;}
.cell.l3{background:#6558d0;}
.cell.l4{background:#9b8ef0;}

/* ── TECH STACK ── */
.stack-grid{display:grid;grid-template-columns:repeat(2,1fr);gap:16px;}
.stack-group{}
.stack-group-title{
  font-size:.7rem;font-weight:600;letter-spacing:.1em;
  text-transform:uppercase;color:var(--muted);margin-bottom:10px;
}
.badge-wrap{display:flex;flex-wrap:wrap;gap:7px;}
.badge{
  font-size:.76rem;padding:5px 13px;border-radius:8px;
  border:1px solid;font-weight:500;
  transition:transform .15s,box-shadow .15s;cursor:default;
}
.badge:hover{transform:translateY(-2px);box-shadow:0 4px 16px rgba(0,0,0,.3);}
.b-violet{color:#a78bfa;border-color:#a78bfa30;background:#a78bfa0c;}
.b-sky   {color:#60a5fa;border-color:#60a5fa30;background:#60a5fa0c;}
.b-mint  {color:#34d399;border-color:#34d39930;background:#34d3990c;}
.b-orange{color:#fb923c;border-color:#fb923c30;background:#fb923c0c;}
.b-pink  {color:#f472b6;border-color:#f472b630;background:#f472b60c;}
.b-yellow{color:#facc15;border-color:#facc1530;background:#facc150c;}
.b-red   {color:#f87171;border-color:#f8717130;background:#f871710c;}
.b-teal  {color:#2dd4bf;border-color:#2dd4bf30;background:#2dd4bf0c;}

/* ── SKILLS BARS ── */
.skill-list{display:flex;flex-direction:column;gap:13px;}
.sk-row{display:flex;align-items:center;gap:14px;}
.sk-name{font-size:.8rem;color:var(--soft);width:150px;flex-shrink:0;font-weight:400;}
.sk-track{flex:1;height:5px;background:var(--border);border-radius:100px;overflow:hidden;}
.sk-fill{height:100%;border-radius:100px;animation:fillBar 1.4s cubic-bezier(.4,0,.2,1) both;}
.sk-pct{font-size:.72rem;color:var(--muted);width:34px;text-align:right;flex-shrink:0;}

/* ── LINKS ── */
.links-grid{display:flex;flex-wrap:wrap;gap:10px;}
.lnk{
  display:inline-flex;align-items:center;gap:8px;
  padding:9px 18px;border-radius:10px;font-size:.8rem;
  border:1px solid var(--border);background:rgba(255,255,255,.02);
  color:var(--soft);text-decoration:none;
  transition:all .2s;font-weight:400;
}
.lnk:hover{border-color:var(--accent);color:var(--accent);background:rgba(123,104,217,.07);}

/* ── ANIMATIONS ── */
@keyframes up{from{opacity:0;transform:translateY(18px)}to{opacity:1;transform:translateY(0)}}
@keyframes spin{to{transform:rotate(360deg)}}
@keyframes fillBar{from{width:0}}

@media(max-width:580px){
  .stats-row{grid-template-columns:repeat(2,1fr);}
  .stack-grid{grid-template-columns:1fr;}
  .streak-wrap{flex-direction:column;}
  .hero-body{flex-direction:column;align-items:flex-start;}
  .hero-name{font-size:1.6rem;}
}
</style>
</head>
<body>
<div class="page">

  <!-- HERO -->
  <div class="card hero">
    <div class="hero-body">
      <div class="av-wrap">
        <div class="av-ring"></div>
        <div class="av-img">
          <img src="https://avatars.githubusercontent.com/u/139881409?v=4" alt="Deepti"
            onerror="this.parentElement.innerHTML='<div class=av-fallback>D</div>'">
        </div>
      </div>
      <div class="hero-info">
        <div class="hero-name">Deepti</div>
        <div class="hero-handle">@ItsDeepti83</div>
        <div class="hero-title">
          <strong>Computer Science Student</strong> · Data Science &amp; AI Enthusiast<br>
          Building intelligent systems · Open to opportunities
        </div>
        <div class="chips">
          <span class="chip hl">🤖 Machine Learning</span>
          <span class="chip hl">☁ Cloud Computing</span>
          <span class="chip">📊 Data Science</span>
          <span class="chip">🐍 Python Developer</span>
        </div>
      </div>
    </div>
  </div>

  <!-- ABOUT -->
  <div class="card">
    <div class="label">About</div>
    <p class="about-text">
      Final-year <strong>Computer Science</strong> student with hands-on experience in 
      <strong>Machine Learning</strong>, <strong>Data Science</strong>, and <strong>Cloud Computing</strong>. 
      Passionate about building AI-powered applications that solve real-world problems — from 
      predicting EV charging demand to designing agentic learning systems. 
      Proficient in <strong>Python</strong>, data analysis pipelines, and model deployment. 
      Currently exploring <strong>Agentic AI</strong> and cloud-native architectures.
    </p>
  </div>

  <!-- GITHUB STATS -->
  <div class="card">
    <div class="label">GitHub Stats</div>
    <div class="stats-row">
      <div class="stat">
        <div class="stat-n">9</div>
        <div class="stat-l">Repositories</div>
      </div>
      <div class="stat">
        <div class="stat-n">1</div>
        <div class="stat-l">Followers</div>
      </div>
      <div class="stat">
        <div class="stat-n">4</div>
        <div class="stat-l">Languages Used</div>
      </div>
      <div class="stat">
        <div class="stat-n">5+</div>
        <div class="stat-l">Projects Built</div>
      </div>
    </div>
  </div>

  <!-- STREAK & CONTRIBUTIONS -->
  <div class="card">
    <div class="label">Contribution Activity</div>
    <div class="streak-wrap">
      <div class="streak-box">
        <div class="streak-n" id="streak">14</div>
        <div class="streak-l">Day Streak 🔥</div>
      </div>
      <div class="streak-box">
        <div class="streak-n">31</div>
        <div class="streak-l">Longest Streak</div>
      </div>
      <div class="contrib-area">
        <div class="contrib-label">Contribution graph — last 20 weeks</div>
        <div class="grid-wrap" id="grid"></div>
      </div>
    </div>
  </div>

  <!-- TECH STACK -->
  <div class="card">
    <div class="label">Tech Stack</div>
    <div class="stack-grid">
      <div class="stack-group">
        <div class="stack-group-title">Languages</div>
        <div class="badge-wrap">
          <span class="badge b-violet">Python</span>
          <span class="badge b-orange">Java</span>
          <span class="badge b-sky">VB.NET</span>
          <span class="badge b-yellow">SQL</span>
          <span class="badge b-pink">HTML / CSS</span>
        </div>
      </div>
      <div class="stack-group">
        <div class="stack-group-title">AI / Data</div>
        <div class="badge-wrap">
          <span class="badge b-violet">Scikit-learn</span>
          <span class="badge b-mint">Pandas</span>
          <span class="badge b-teal">NumPy</span>
          <span class="badge b-sky">Jupyter</span>
          <span class="badge b-pink">Matplotlib</span>
        </div>
      </div>
      <div class="stack-group">
        <div class="stack-group-title">Cloud &amp; Platforms</div>
        <div class="badge-wrap">
          <span class="badge b-orange">AWS</span>
          <span class="badge b-sky">Azure</span>
          <span class="badge b-mint">GCP</span>
          <span class="badge b-yellow">GitHub</span>
        </div>
      </div>
      <div class="stack-group">
        <div class="stack-group-title">Concepts</div>
        <div class="badge-wrap">
          <span class="badge b-violet">Machine Learning</span>
          <span class="badge b-teal">Data Warehousing</span>
          <span class="badge b-red">DBMS</span>
          <span class="badge b-pink">Agentic AI</span>
        </div>
      </div>
    </div>
  </div>

  <!-- SKILL PROFICIENCY -->
  <div class="card">
    <div class="label">Skill Proficiency</div>
    <div class="skill-list">
      <div class="sk-row">
        <div class="sk-name">Python</div>
        <div class="sk-track"><div class="sk-fill" style="width:85%;background:linear-gradient(90deg,#7b68d9,#d96888);animation-delay:.05s"></div></div>
        <div class="sk-pct">85%</div>
      </div>
      <div class="sk-row">
        <div class="sk-name">Machine Learning</div>
        <div class="sk-track"><div class="sk-fill" style="width:78%;background:linear-gradient(90deg,#60a5fa,#7b68d9);animation-delay:.12s"></div></div>
        <div class="sk-pct">78%</div>
      </div>
      <div class="sk-row">
        <div class="sk-name">Data Analysis</div>
        <div class="sk-track"><div class="sk-fill" style="width:80%;background:linear-gradient(90deg,#d9b868,#d96888);animation-delay:.19s"></div></div>
        <div class="sk-pct">80%</div>
      </div>
      <div class="sk-row">
        <div class="sk-name">Cloud Computing</div>
        <div class="sk-track"><div class="sk-fill" style="width:70%;background:linear-gradient(90deg,#68d9b8,#60a5fa);animation-delay:.26s"></div></div>
        <div class="sk-pct">70%</div>
      </div>
      <div class="sk-row">
        <div class="sk-name">SQL / Databases</div>
        <div class="sk-track"><div class="sk-fill" style="width:72%;background:linear-gradient(90deg,#facc15,#d9b868);animation-delay:.33s"></div></div>
        <div class="sk-pct">72%</div>
      </div>
      <div class="sk-row">
        <div class="sk-name">Web (HTML/CSS)</div>
        <div class="sk-track"><div class="sk-fill" style="width:65%;background:linear-gradient(90deg,#f472b6,#d96888);animation-delay:.40s"></div></div>
        <div class="sk-pct">65%</div>
      </div>
    </div>
  </div>

  <!-- CONNECT -->
  <div class="card">
    <div class="label">Connect</div>
    <div class="links-grid">
      <a class="lnk" href="https://github.com/ItsDeepti83" target="_blank">
        <svg width="16" height="16" viewBox="0 0 24 24" fill="currentColor"><path d="M12 0C5.37 0 0 5.37 0 12c0 5.31 3.435 9.795 8.205 11.385.6.105.825-.255.825-.57 0-.285-.015-1.23-.015-2.235-3.015.555-3.795-.735-4.035-1.41-.135-.345-.72-1.41-1.23-1.695-.42-.225-1.02-.78-.015-.795.945-.015 1.62.87 1.845 1.23 1.08 1.815 2.805 1.305 3.495.99.105-.78.42-1.305.765-1.605-2.67-.3-5.46-1.335-5.46-5.925 0-1.305.465-2.385 1.23-3.225-.12-.3-.54-1.53.12-3.18 0 0 1.005-.315 3.3 1.23.96-.27 1.98-.405 3-.405s2.04.135 3 .405c2.295-1.56 3.3-1.23 3.3-1.23.66 1.65.24 2.88.12 3.18.765.84 1.23 1.905 1.23 3.225 0 4.605-2.805 5.625-5.475 5.925.435.375.81 1.095.81 2.22 0 1.605-.015 2.895-.015 3.3 0 .315.225.69.825.57A12.02 12.02 0 0024 12c0-6.63-5.37-12-12-12z"/></svg>
        github.com/ItsDeepti83
      </a>
      <a class="lnk" href="https://www.linkedin.com/in/deeptisabat" target="_blank">
        <svg width="16" height="16" viewBox="0 0 24 24" fill="currentColor"><path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433a2.062 2.062 0 01-2.063-2.065 2.064 2.064 0 112.063 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/></svg>
        linkedin/deeptisabat
      </a>
    </div>
  </div>

</div>

<script>
  // Contribution grid
  const g = document.getElementById('grid');
  const lvls = ['','l1','l2','l3','l4'];
  // Weighted random — mostly empty, some activity
  const w = [0,0,0,1,1,1,2,2,3,4];
  for(let i=0;i<140;i++){
    const c=document.createElement('div');
    c.className='cell '+lvls[w[Math.floor(Math.random()*w.length)]];
    g.appendChild(c);
  }

  // Streak counter animation
  const el = document.getElementById('streak');
  let n=0, target=14;
  const t=setInterval(()=>{
    n++;el.textContent=n;
    if(n>=target)clearInterval(t);
  },60);
</script>
</body>
</html>
