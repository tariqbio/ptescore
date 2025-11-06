<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>PTE Academic • Ultimate Scoreboard</title>
<meta name="viewport" content="width=device-width, initial-scale=1">
<style>
  /* ========== CSS Variables ========== */
  :root {
    /* Dark Mode - Premium Purple/Blue Gradient */
    --primary: #8B5CF6;
    --secondary: #6366F1;
    --accent: #EC4899;
    --success: #10B981;
    --bg-primary: #0F172A;
    --bg-secondary: #1E293B;
    --bg-card: rgba(30, 41, 59, 0.6);
    --text-primary: #F1F5F9;
    --text-secondary: #CBD5E1;
    --border: rgba(148, 163, 184, 0.1);
    --glow: 0 20px 60px rgba(139, 92, 246, 0.3);
    --shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.5);
  }

  /* ========== Base Styles ========== */
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }

  body {
    font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
    background: linear-gradient(135deg, #0F172A 0%, #1E293B 50%, #312E81 100%);
    color: var(--text-primary);
    min-height: 100vh;
    overflow-x: hidden;
    transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
    position: relative;
  }

  body::before {
    content: '';
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: 
      radial-gradient(circle at 20% 50%, rgba(139, 92, 246, 0.15) 0%, transparent 50%),
      radial-gradient(circle at 80% 80%, rgba(236, 72, 153, 0.15) 0%, transparent 50%),
      radial-gradient(circle at 40% 20%, rgba(99, 102, 241, 0.1) 0%, transparent 50%);
    pointer-events: none;
    z-index: 0;
  }

  /* ========== Light Mode ========== */
  body.light {
    --primary: #8B5CF6;
    --secondary: #6366F1;
    --accent: #EC4899;
    --bg-primary: #FFFFFF;
    --bg-secondary: #F8FAFC;
    --bg-card: rgba(255, 255, 255, 0.8);
    --text-primary: #0F172A;
    --text-secondary: #475569;
    --border: rgba(148, 163, 184, 0.2);
    --glow: 0 20px 60px rgba(139, 92, 246, 0.2);
    --shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.1);
    background: linear-gradient(135deg, #F8FAFC 0%, #EEF2FF 50%, #F5F3FF 100%);
  }

  body.light::before {
    background: 
      radial-gradient(circle at 20% 50%, rgba(139, 92, 246, 0.08) 0%, transparent 50%),
      radial-gradient(circle at 80% 80%, rgba(236, 72, 153, 0.08) 0%, transparent 50%),
      radial-gradient(circle at 40% 20%, rgba(99, 102, 241, 0.05) 0%, transparent 50%);
  }

  body.light .header {
    background: linear-gradient(180deg, #FFFFFF 0%, #6366F1 100%);
  }

  body.light .logo-icon {
    background: linear-gradient(135deg, #EC4899, #8B5CF6);
  }

  body.light th {
    background: linear-gradient(135deg, rgba(139, 92, 246, 0.1), rgba(99, 102, 241, 0.1));
    color: var(--text-primary);
  }

  body.light th:hover {
    background: linear-gradient(135deg, rgba(139, 92, 246, 0.2), rgba(99, 102, 241, 0.2));
  }

  body.light td {
    background: rgba(139, 92, 246, 0.03);
    color: var(--text-primary);
  }

  body.light tr:hover td {
    background: rgba(139, 92, 246, 0.08);
  }

  body.light .total {
    background: linear-gradient(135deg, #8B5CF6, #6366F1) !important;
    color: white;
  }

  body.light .btn {
    background: rgba(139, 92, 246, 0.08);
    color: var(--primary);
    border-color: rgba(139, 92, 246, 0.2);
  }

  body.light .btn:hover {
    background: rgba(139, 92, 246, 0.15);
    box-shadow: 0 10px 30px rgba(139, 92, 246, 0.2);
  }

  body.light .btn.active {
    background: linear-gradient(135deg, var(--primary), var(--secondary));
    color: white;
    border-color: transparent;
  }

  body.light input,
  body.light select {
    background: rgba(139, 92, 246, 0.05);
    color: var(--text-primary);
    border: 2px solid rgba(139, 92, 246, 0.2);
  }

  body.light .card {
    background: var(--bg-card);
    backdrop-filter: blur(20px);
    border-color: var(--border);
  }

  body.light .mod-card {
    background: linear-gradient(135deg, rgba(139, 92, 246, 0.08), rgba(99, 102, 241, 0.08));
  }

  body.light .stat-number {
    background: linear-gradient(135deg, var(--primary), var(--secondary));
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
  }

body.light .sum-row td {
    background: linear-gradient(135deg, #8b5cf6, #0f172a) !important;
}
  /* ========== Header ========== */
  .header {
    text-align: center;
    padding: 4rem 2rem;
    background: linear-gradient(135deg, rgba(139, 92, 246, 0.2) 0%, rgba(99, 102, 241, 0.2) 100%);
    position: relative;
    z-index: 1;
    backdrop-filter: blur(10px);
    border-bottom: 1px solid var(--border);
  }

  .logo-container {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 1rem;
    margin-bottom: 1rem;
  }

  .logo-icon {
    width: 60px;
    height: 60px;
    background: linear-gradient(135deg, var(--accent), var(--primary));
    border-radius: 16px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 2rem;
    font-weight: 900;
    color: white;
    box-shadow: var(--glow);
    transform: rotate(-5deg);
  }

  .logo {
    font-size: 2.5rem;
    font-weight: 800;
    letter-spacing: -1px;
    color: white;
  }

  .subtitle {
    font-size: 1rem;
    color: rgba(255, 255, 255, 0.8);
    text-transform: uppercase;
    letter-spacing: 3px;
    font-weight: 600;
    margin-bottom: 1rem;
  }

  .title {
    font-size: 4.5rem;
    font-weight: 900;
    background: linear-gradient(135deg, #EC4899, #8B5CF6, #6366F1);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    margin: 1rem 0;
    letter-spacing: -2px;
    line-height: 1.1;
  }

  .header-subtitle {
    font-size: 1.8rem;
    font-weight: 700;
    color: white;
    margin: 1.5rem 0;
  }

  .badge {
    background: linear-gradient(135deg, var(--accent), var(--primary));
    padding: 0.9rem 2.5rem;
    border-radius: 100px;
    font-weight: 700;
    display: inline-block;
    box-shadow: var(--glow);
    color: white;
    margin-top: 1rem;
    font-size: 0.95rem;
    text-transform: uppercase;
    letter-spacing: 1px;
    transition: all 0.3s ease;
  }

  .badge:hover {
    transform: translateY(-2px);
    box-shadow: 0 25px 70px rgba(236, 72, 153, 0.4);
  }

  /* ========== Container ========== */
  .container {
    max-width: 1400px;
    margin: 0 auto;
    padding: 3rem 2rem;
    position: relative;
    z-index: 1;
  }

  /* ========== Controls ========== */
  .controls {
    display: flex;
    flex-wrap: wrap;
    gap: 1rem;
    justify-content: center;
    margin: 2rem 0 3rem;
    padding: 1rem;
    background: var(--bg-card);
    backdrop-filter: blur(20px);
    border-radius: 20px;
    border: 1px solid var(--border);
  }

  .btn {
    padding: 1rem 2rem;
    border: 2px solid var(--border);
    border-radius: 100px;
    background: rgba(139, 92, 246, 0.1);
    backdrop-filter: blur(10px);
    color: var(--text-primary);
    font-weight: 700;
    cursor: pointer;
    transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
    font-size: 0.9rem;
    text-transform: uppercase;
    letter-spacing: 0.5px;
  }

  .btn:hover {
    transform: translateY(-3px);
    box-shadow: 0 15px 40px rgba(139, 92, 246, 0.3);
    border-color: var(--primary);
  }

  .btn.active {
    background: linear-gradient(135deg, var(--primary), var(--secondary));
    color: white;
    border-color: transparent;
    box-shadow: var(--glow);
  }

  /* ========== Card ========== */
  .card {
    background: var(--bg-card);
    backdrop-filter: blur(30px);
    border-radius: 24px;
    padding: 2.5rem;
    margin: 2rem 0;
    box-shadow: var(--shadow);
    border: 1px solid var(--border);
    transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
  }

  .card:hover {
    transform: translateY(-8px);
    box-shadow: 0 30px 60px -12px rgba(0, 0, 0, 0.3);
  }

  .card-title {
    text-align: center;
    margin-bottom: 2rem;
    font-size: 2rem;
    font-weight: 800;
    background: linear-gradient(135deg, var(--accent), var(--primary));
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
  }

  /* ========== Table ========== */
  .table-wrapper {
    overflow-x: auto;
    border-radius: 16px;
  }

  table {
    width: 100%;
    border-collapse: separate;
    border-spacing: 0 0.5rem;
  }

  th {
    background: linear-gradient(135deg, rgba(139, 92, 246, 0.2), rgba(99, 102, 241, 0.2));
    padding: 1.2rem 1rem;
    cursor: pointer;
    font-weight: 700;
    text-transform: uppercase;
    font-size: 0.8rem;
    letter-spacing: 1px;
    transition: all 0.3s ease;
    color: var(--text-primary);
    border: none;
    position: relative;
  }

  th:first-child {
    border-radius: 12px 0 0 12px;
  }

  th:last-child {
    border-radius: 0 12px 12px 0;
  }

  th:hover {
    background: linear-gradient(135deg, rgba(139, 92, 246, 0.35), rgba(99, 102, 241, 0.35));
    transform: translateY(-2px);
  }

  th::after {
    content: '↕';
    margin-left: 6px;
    opacity: 0.5;
    font-size: 0.9rem;
  }

  td {
    padding: 1.3rem 1rem;
    text-align: center;
    background: rgba(139, 92, 246, 0.05);
    transition: all 0.3s ease;
    font-weight: 500;
    border: none;
  }

  tr td:first-child {
    border-radius: 12px 0 0 12px;
  }

  tr td:last-child {
    border-radius: 0 12px 12px 0;
  }

  tbody tr {
    transition: all 0.3s ease;
  }

  tbody tr:hover td {
    background: rgba(139, 92, 246, 0.12);
    transform: scale(1.01);
  }

  .total {
    font-weight: 800;
    background: linear-gradient(135deg, var(--primary), var(--secondary)) !important;
    color: white !important;
    font-size: 1.1rem;
  }

  .rank {
    font-weight: 800;
    color: var(--accent);
    font-size: 1.1rem;
  }

  /* ========== Sum Row ========== */
  .sum-row {
    border-top: 3px solid var(--primary);
  }

  .sum-row td {
    background: linear-gradient(135deg, #8b5cf6, #0f172a) !important;
    color: white !important;
    font-weight: 800;
    font-size: 1.1rem;
    padding: 1.5rem 1rem;
  }

  .sum-row:hover td {
    background: linear-gradient(135deg, #8b5cf6, #0f172a) !important;
    transform: scale(1.01);
  }

  /* ========== Modules ========== */
  .module {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 1.5rem;
    margin: 2rem 0;
  }

  .mod-card {
    background: linear-gradient(135deg, rgba(139, 92, 246, 0.1), rgba(99, 102, 241, 0.1));
    padding: 2rem;
    border-radius: 20px;
    text-align: center;
    backdrop-filter: blur(10px);
    border: 1px solid var(--border);
    transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
    position: relative;
    overflow: hidden;
  }

  .mod-card::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    height: 4px;
    background: linear-gradient(90deg, var(--primary), var(--accent));
  }

  .mod-card:hover {
    transform: translateY(-8px) scale(1.02);
    box-shadow: 0 20px 50px rgba(139, 92, 246, 0.25);
    border-color: var(--primary);
  }

  .stat-number {
    font-size: 3.5rem;
    font-weight: 900;
    background: linear-gradient(135deg, var(--accent), var(--primary));
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    display: block;
    margin-bottom: 0.5rem;
    line-height: 1;
  }

  .stat-label {
    font-size: 1.1rem;
    font-weight: 600;
    color: var(--text-secondary);
    text-transform: uppercase;
    letter-spacing: 1px;
  }

  /* ========== Converter ========== */
  .converter {
    display: flex;
    gap: 1rem;
    align-items: center;
    flex-wrap: wrap;
    justify-content: center;
    margin: 2rem 0;
  }

  input,
  select {
    padding: 1.2rem 1.5rem;
    border-radius: 16px;
    border: 2px solid var(--border);
    background: rgba(139, 92, 246, 0.08);
    color: var(--text-primary);
    backdrop-filter: blur(10px);
    font-size: 1rem;
    font-weight: 600;
    transition: all 0.3s ease;
    min-width: 200px;
  }

  input:focus,
  select:focus {
    outline: none;
    border-color: var(--primary);
    box-shadow: 0 0 0 4px rgba(139, 92, 246, 0.1);
  }

  input::placeholder {
    color: var(--text-secondary);
    opacity: 0.6;
  }

  #result {
    font-size: 3.5rem;
    font-weight: 900;
    background: linear-gradient(135deg, var(--accent), var(--primary));
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    min-width: 100px;
    text-align: center;
  }

  .converter-hint {
    text-align: center;
    margin-top: 1.5rem;
    padding: 1rem 2rem;
    background: rgba(139, 92, 246, 0.08);
    border-radius: 16px;
    color: var(--text-secondary);
    font-weight: 500;
    border: 1px solid var(--border);
  }

  /* ========== Footer ========== */
  .footer {
    text-align: center;
    padding: 4rem 2rem;
    color: var(--text-secondary);
    font-size: 0.95rem;
    border-top: 1px solid var(--border);
    margin-top: 4rem;
  }

  .footer p {
    margin: 0.8rem 0;
    line-height: 1.6;
  }

  .footer b {
    color: var(--accent);
    font-weight: 700;
  }

  /* ========== Theme Toggle ========== */
  .theme-toggle {
    position: fixed;
    top: 24px;
    right: 24px;
    background: var(--bg-card);
    backdrop-filter: blur(20px);
    color: var(--text-primary);
    padding: 1rem 1.5rem;
    border-radius: 100px;
    cursor: pointer;
    box-shadow: var(--shadow);
    z-index: 1000;
    border: 1px solid var(--border);
    font-weight: 700;
    transition: all 0.3s ease;
    display: flex;
    align-items: center;
    gap: 0.5rem;
  }

  .theme-toggle:hover {
    transform: scale(1.05) rotate(10deg);
    box-shadow: 0 20px 50px rgba(139, 92, 246, 0.3);
  }

  /* ========== Responsive ========== */
  @media (max-width: 768px) {
    .title {
      font-size: 2.5rem;
    }

    .logo {
      font-size: 1.8rem;
    }

    .logo-icon {
      width: 50px;
      height: 50px;
      font-size: 1.5rem;
    }

    .card {
      padding: 1.5rem;
    }

    table {
      font-size: 0.85rem;
    }

    th, td {
      padding: 0.8rem 0.5rem;
    }

    .stat-number {
      font-size: 2.5rem;
    }

    .module {
      grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
      gap: 1rem;
    }

    .converter {
      flex-direction: column;
    }

    input, select {
      width: 100%;
      min-width: auto;
    }
  }

  /* ========== Print Styles ========== */
  @media print {
    .theme-toggle,
    .controls {
      display: none;
    }

    body {
      background: white;
      color: black;
    }

    .card {
      break-inside: avoid;
      box-shadow: none;
    }
  }

  /* ========== Animations ========== */
  @keyframes fadeInUp {
    from {
      opacity: 0;
      transform: translateY(30px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }

  .card {
    animation: fadeInUp 0.6s ease-out;
  }

  .card:nth-child(2) {
    animation-delay: 0.1s;
  }

  .card:nth-child(3) {
    animation-delay: 0.2s;
  }

  .card:nth-child(4) {
    animation-delay: 0.3s;
  }
</style>
</head>
<body>

<!-- Theme Toggle -->
<button class="theme-toggle" id="themeToggle">
  <span id="themeIcon">🌙</span>
  <span id="themeText">Dark</span>
</button>

<!-- Header -->
<div class="header">
  <div class="logo-container">
    <div class="logo-icon">P</div>
    <div class="logo">Pearson</div>
  </div>
  <div class="subtitle">Test of English</div>
  <h1 class="title">PTE Academic</h1>
  <h2 class="header-subtitle">Ultimate Scoreboard</h2>
  <div class="badge">🎯 TARIQUL Edition</div>
</div>

<!-- Main Container -->
<div class="container">

  <!-- Filter Controls -->
  <div class="controls">
    <button class="btn active" data-skill="all">📊 ALL TASKS</button>
    <button class="btn" data-skill="speak">🎤 SPEAKING</button>
    <button class="btn" data-skill="write">✍️ WRITING</button>
    <button class="btn" data-skill="read">📖 READING</button>
    <button class="btn" data-skill="listen">🎧 LISTENING</button>
  </div>

  <!-- Score Table -->
  <div class="card">
    <h2 class="card-title">📈 Live PTE Scoreboard • Click to Sort</h2>
    <div class="table-wrapper">
      <table id="table">
        <thead>
          <tr>
            <th data-sort="rank">#</th>
            <th data-sort="task">TASK</th>
            <th data-sort="items">Items</th>
            <th data-sort="speak">Speak</th>
            <th data-sort="write">Write</th>
            <th data-sort="read">Read</th>
            <th data-sort="listen">Listen</th>
            <th data-sort="total" class="total">TOTAL</th>
          </tr>
        </thead>
        <tbody id="tbody">
          <!-- JS fills this -->
        </tbody>
        <tfoot>
          <tr class="sum-row">
            <td colspan="2" style="text-align:left; padding-left: 1.5rem;">📊 TOTAL RAW POINTS</td>
            <td>—</td>
            <td id="sumSpeak">116</td>
            <td id="sumWrite">68</td>
            <td id="sumRead">49</td>
            <td id="sumListen">119</td>
            <td id="sumTotal">352</td>
          </tr>
          <tr class="sum-row">
            <td colspan="2" style="text-align:left; padding-left: 1.5rem;">🎯 APPROX. PTE SCORE (≈90 each)</td>
            <td>—</td>
            <td id="pteSpeak">90</td>
            <td id="pteWrite">90</td>
            <td id="pteRead">90</td>
            <td id="pteListen">90</td>
            <td id="pteOverall">360</td>
          </tr>
        </tfoot>
      </table>
    </div>
  </div>

  <!-- Module Breakdown -->
  <div class="card">
    <h3 class="card-title">🎯 Module Breakdown</h3>
    <div class="module" id="modules">
      <div class="mod-card">
        <span class="stat-number">116</span>
        <div class="stat-label">🎤 Speaking</div>
      </div>
      <div class="mod-card">
        <span class="stat-number">68</span>
        <div class="stat-label">✍️ Writing</div>
      </div>
      <div class="mod-card">
        <span class="stat-number">49</span>
        <div class="stat-label">📖 Reading</div>
      </div>
      <div class="mod-card">
        <span class="stat-number">119</span>
        <div class="stat-label">🎧 Listening</div>
      </div>
    </div>
  </div>

  <!-- Score Converter -->
  <div class="card">
    <h3 class="card-title">⚡ Raw → PTE Score Converter</h3>
    <div class="converter">
      <input type="number" id="raw" placeholder="Raw points (0–352)" value="300" min="0" max="352">
      <select id="target">
        <option>Overall</option>
        <option>Speaking</option>
        <option>Writing</option>
        <option>Reading</option>
        <option>Listening</option>
      </select>
      <button class="btn active" onclick="convert()">CONVERT →</button>
      <div id="result">86</div>
    </div>
    <div class="converter-hint">
      💡 <b>352 raw = 90</b> • <b>300 raw ≈ 86</b> • <b>250 raw ≈ 79</b>
    </div>
  </div>

</div>

<!-- Footer -->
<div class="footer">
  <p>✨ Made with love for future 90+ legends • Double-click any row to highlight your focus task</p>
  <p>🚀 Pro Tip: Master <b>Repeat Sentence (45)</b> + <b>Write From Dictation (41)</b> = <b>+86 raw points</b> in 14 days</p>
</div>

<script>
  // ========== Data ==========
  const data = [
    {rank:1, task:"Repeat Sentence", items:"10–12", speak:27, write:0, read:0, listen:18, total:45},
    {rank:2, task:"Write From Dictation", items:"3–4", speak:0, write:20, read:0, listen:21, total:41},
    {rank:3, task:"Retell Lecture", items:"2–3", speak:18, write:0, read:0, listen:18, total:36},
    {rank:3, task:"Summarize Group Discussion", items:"2–3", speak:18, write:0, read:0, listen:18, total:36},
    {rank:5, task:"Read Aloud", items:"6–7", speak:25, write:0, read:0, listen:0, total:25},
    {rank:6, task:"Summarize Spoken Text", items:"1", speak:0, write:8, read:0, listen:10, total:18},
    {rank:7, task:"Reading & Writing Blanks", items:"5–6", speak:0, write:2, read:12, listen:3, total:17},
    {rank:7, task:"Reading Drag-Drop Blanks", items:"4–5", speak:0, write:0, read:17, listen:0, total:17},
    {rank:9, task:"Describe Image", items:"5–6", speak:15, write:0, read:0, listen:0, total:15},
    {rank:9, task:"Write Email", items:"1", speak:0, write:15, read:0, listen:0, total:15},
    {rank:9, task:"Write Essay", items:"1", speak:0, write:15, read:0, listen:0, total:15},
    {rank:9, task:"Highlight Incorrect Words", items:"2–3", speak:0, write:0, read:5, listen:10, total:15},
    {rank:13, task:"Listening Fill-in Blanks", items:"2–3", speak:0, write:0, read:0, listen:12, total:12},
    {rank:13, task:"Summarize Written Text", items:"2", speak:0, write:8, read:4, listen:0, total:12},
    {rank:15, task:"Respond to a Situation", items:"1", speak:10, write:0, read:0, listen:0, total:10},
    {rank:16, task:"Reorder Paragraphs", items:"2–3", speak:0, write:0, read:6, listen:0, total:6},
    {rank:17, task:"Answer Short Question", items:"5–6", speak:3, write:0, read:0, listen:2, total:5},
    {rank:18, task:"MC Multiple (R+L)", items:"4", speak:0, write:0, read:3, listen:3, total:6},
    {rank:20, task:"MC Single (R+L)", items:"4", speak:0, write:0, read:2, listen:2, total:4},
    {rank:21, task:"Select Missing Word", items:"1–2", speak:0, write:0, read:0, listen:2, total:2}
  ];

  // ========== DOM Elements ==========
  const tbody = document.getElementById('tbody');
  const buttons = document.querySelectorAll('[data-skill]');
  const themeToggle = document.getElementById('themeToggle');
  const themeIcon = document.getElementById('themeIcon');
  const themeText = document.getElementById('themeText');

  // ========== Render Table ==========
  function render(filter = 'all') {
    tbody.innerHTML = '';
    let filtered = filter === 'all' ? data : data.filter(r => r[filter] > 0);
    
    // Calculate sums
    let sumSpeak = 0, sumWrite = 0, sumRead = 0, sumListen = 0, sumTotal = 0;
    
    filtered.forEach((row, i) => {
      const tr = document.createElement('tr');
      tr.innerHTML = `
        <td class="rank">${i+1}</td>
        <td style="text-align:left; padding-left: 1.5rem;">${row.task}</td>
        <td>${row.items}</td>
        <td>${row.speak||'—'}</td>
        <td>${row.write||'—'}</td>
        <td>${row.read||'—'}</td>
        <td>${row.listen||'—'}</td>
        <td class="total">${row.total}</td>
      `;
      tr.ondblclick = () => {
        tr.style.background = 'rgba(236, 72, 153, 0.25)';
        tr.style.transform = 'scale(1.02)';
      };
      tbody.appendChild(tr);
      
      // Sum up totals
      sumSpeak += row.speak;
      sumWrite += row.write;
      sumRead += row.read;
      sumListen += row.listen;
      sumTotal += row.total;
    });
    
    // Update sum row
    document.getElementById('sumSpeak').textContent = sumSpeak;
    document.getElementById('sumWrite').textContent = sumWrite;
    document.getElementById('sumRead').textContent = sumRead;
    document.getElementById('sumListen').textContent = sumListen;
    document.getElementById('sumTotal').textContent = sumTotal;
    
    // Calculate approximate PTE scores (90 scale)
    document.getElementById('pteSpeak').textContent = Math.round((sumSpeak / 116) * 90);
    document.getElementById('pteWrite').textContent = Math.round((sumWrite / 68) * 90);
    document.getElementById('pteRead').textContent = Math.round((sumRead / 49) * 90);
    document.getElementById('pteListen').textContent = Math.round((sumListen / 119) * 90);
    document.getElementById('pteOverall').textContent = Math.round((sumTotal / 352) * 90);
  }

  // ========== Sort Table ==========
  document.querySelectorAll('th').forEach((th, i) => {
    th.onclick = () => {
      const key = th.getAttribute('data-sort');
      const asc = th.classList.toggle('asc');
      const rows = Array.from(tbody.querySelectorAll('tr'));
      
      rows.sort((a, b) => {
        let A = a.children[i].textContent;
        let B = b.children[i].textContent;
        
        if (key === 'rank' || !isNaN(A)) {
          A = parseFloat(A) || 0;
          B = parseFloat(B) || 0;
        }
        
        return asc ? (A > B ? 1 : -1) : (A < B ? 1 : -1);
      });
      
      rows.forEach(r => tbody.appendChild(r));
    };
  });

  // ========== Filter Buttons ==========
  buttons.forEach(btn => {
    btn.onclick = () => {
      buttons.forEach(b => b.classList.remove('active'));
      btn.classList.add('active');
      render(btn.dataset.skill);
    };
  });

  // ========== Score Converter ==========
  function convert() {
    const raw = parseInt(document.getElementById('raw').value) || 0;
    const clampedRaw = Math.max(0, Math.min(352, raw));
    const pte = Math.min(90, Math.max(10, Math.round(10 + (clampedRaw / 352) * 80)));
    document.getElementById('result').textContent = pte;
  }

  // Auto-convert on input
  document.getElementById('raw').addEventListener('input', convert);

  // ========== Theme Toggle ==========
  themeToggle.onclick = () => {
    document.body.classList.toggle('light');
    const isLight = document.body.classList.contains('light');
    themeIcon.textContent = isLight ? '☀️' : '🌙';
    themeText.textContent = isLight ? 'Light' : 'Dark';
  };

  // ========== Initialize ==========
  render();
  convert();
</script>

</body>
</html>
