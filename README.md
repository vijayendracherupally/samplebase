<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>TextMorph — Full README (VS-style)</title>
  <style>
    :root{
      --bg:#1e1e1e;
      --panel:#252526;
      --muted:#9cdcfe;
      --text:#d4d4d4;
      --accent:#007acc;
      --accent-2:#569cd6;
      --success:#6bb56b;
      --danger:#f14c4c;
      --glass: rgba(255,255,255,0.03);
      --code-bg:#1e1e1e;
      --card:#2d2d2d;
      --mono: "Consolas", "Monaco", "Courier New", monospace;
      --ui: "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
    }
    html,body{height:100%;margin:0;background:linear-gradient(180deg,var(--bg),#151515);font-family:var(--ui);color:var(--text)}
    .container{max-width:1100px;margin:36px auto;padding:28px;background:linear-gradient(180deg, rgba(255,255,255,0.02), transparent);border-radius:8px;box-shadow:0 6px 30px rgba(0,0,0,0.6);border:1px solid rgba(255,255,255,0.03)}
    header{display:flex;align-items:center;gap:16px}
    .logo{width:64px;height:64px;border-radius:8px;background:linear-gradient(135deg,var(--accent),var(--accent-2));display:flex;align-items:center;justify-content:center;color:white;font-weight:700;font-family:var(--mono)}
    h1{font-size:22px;margin:0}
    p.lead{color:var(--muted);margin-top:6px}
    nav{margin-top:18px;display:flex;gap:10px;flex-wrap:wrap}
    a.btn{background:var(--glass);padding:8px 12px;border-radius:6px;color:var(--text);text-decoration:none;border:1px solid rgba(255,255,255,0.03);font-size:13px}
    a.btn.primary{background:linear-gradient(90deg,var(--accent),var(--accent-2));color:white;border:none}
    section{margin-top:22px}
    .grid{display:grid;grid-template-columns:1fr 340px;gap:20px}
    .card{background:var(--card);padding:16px;border-radius:8px;border:1px solid rgba(255,255,255,0.03)}
    .muted{color:var(--muted);font-size:13px}
    h2{margin:6px 0 12px 0;color:#e7e7e7}
    ul{margin:8px 0 8px 18px}
    pre,code{font-family:var(--mono);font-size:13px}
    pre.codeblock{background:var(--code-bg);padding:12px;border-radius:6px;border:1px solid rgba(255,255,255,0.02);overflow:auto}
    .tech{display:flex;flex-wrap:wrap;gap:8px}
    .chip{background:rgba(255,255,255,0.02);padding:6px 10px;border-radius:999px;border:1px solid rgba(255,255,255,0.03);font-size:13px}
    footer{margin-top:26px;color:var(--muted);font-size:13px;display:flex;justify-content:space-between;align-items:center}
    .right{display:flex;gap:10px}
    .pdf-link{color:var(--accent);text-decoration:underline}
    table {width:100%;border-collapse:collapse;margin-top:8px}
    th,td{padding:8px;border-bottom:1px solid rgba(255,255,255,0.03);text-align:left}
    .small{font-size:13px;color:var(--muted)}
    @media (max-width:900px){.grid{grid-template-columns:1fr} .logo{width:52px;height:52px}}
  </style>
</head>
<body>
  <div class="container">
    <header>
      <div class="logo">TM</div>
      <div>
        <h1>TextMorph — Full README (Visual Studio style)</h1>
        <p class="lead">AI-powered content simplification, summarization & paraphrasing — domain-aware, Streamlit-based.</p>
        <nav>
          <a class="btn primary" href="#usage">Get Started</a>
          <a class="btn" href="#features">Features</a>
          <a class="btn" href="#architecture">Architecture</a>
          <a class="btn" href="#models">Models</a>
        </nav>
      </div>
    </header>

    <!-- ==== Overview ==== -->
    <section id="overview" class="card">
      <h2>Overview</h2>
      <p class="muted">TextMorph is a modular NLP suite built to transform complex domain text into clear, readable outputs using transformer models tuned per-domain.</p>
      <div style="display:flex;gap:12px;margin-top:12px;flex-wrap:wrap">
        <div class="chip">Streamlit UI</div>
        <div class="chip">Hugging Face Transformers</div>
        <div class="chip">FLAN-T5 (domain)</div>
        <div class="chip">SQLite / Logs</div>
        <div class="chip">Docker-ready</div>
      </div>
    </section>

    <div class="grid" style="margin-top:18px">
      <main>

        <!-- FEATURES -->
        <section id="features" class="card">
          <h2>Key Features</h2>
          <div style="display:flex;gap:18px;flex-wrap:wrap">
            <div style="flex:1;min-width:260px">
              <h3 class="small">User Features</h3>
              <ul>
                <li><strong>Secure Authentication</strong> — JWT-based login & OTP recovery.</li>
                <li><strong>Readability Analyzer</strong></li>
                <li><strong>Summarization</strong></li>
                <li><strong>Paraphrasing</strong></li>
                <li><strong>Side-by-Side Comparison</strong></li>
                <li><strong>Feedback & History</strong></li>
              </ul>
            </div>
            <div style="flex:1;min-width:260px">
              <h3 class="small">Admin Features</h3>
              <ul>
                <li><strong>Model Management</strong></li>
                <li><strong>Account Limits</strong></li>
                <li><strong>Usage Analytics</strong></li>
                <li><strong>Feedback Monitoring</strong></li>
                <li><strong>Global Search</strong></li>
                <li><strong>Hot-swap Models</strong></li>
              </ul>
            </div>
          </div>
        </section>

        <!-- INSTALLATION -->
        <section id="installation" class="card" style="margin-top:18px">
          <h2>Installation</h2>
          <p class="muted">Quick local setup</p>
          <pre class="codeblock">git clone &lt;repository-link&gt;
cd TextMorph
pip install -r requirements.txt
streamlit run app.py</pre>
        </section>

        <!-- USAGE -->
        <section id="usage" class="card">
          <h2>Usage Guide</h2>
          <ol>
            <li>Start the app</li>
            <li>Login / Register</li>
            <li>Choose domain and load model</li>
            <li>Enter text or upload file</li>
            <li>Generate outputs</li>
            <li>Save & review history</li>
          </ol>
        </section>

        <!-- ARCHITECTURE -->
        <section id="architecture" class="card">
          <h2>Architecture</h2>
          <p class="muted">Streamlit frontend + Python backend.</p>
          <table>
            <tr><td>Streamlit UI</td><td>User-facing interface</td></tr>
            <tr><td>ML Engine</td><td>Tokenization & Generation</td></tr>
            <tr><td>SQLite</td><td>History & logs</td></tr>
          </table>
        </section>

        <!-- MODELS -->
        <section id="models" class="card">
          <h2>Models & Loading</h2>
          <table>
            <tr><td>FLAN-T5</td><td>Summarization / Paraphrase</td></tr>
            <tr><td>Pegasus</td><td>Abstractive Summaries</td></tr>
            <tr><td>BART</td><td>Rewriting / Fallback</td></tr>
          </table>
        </section>

      </main>

      <!-- SIDEBAR -->
      <aside>
        <div class="card">
          <h3>Quick Links</h3>
          <ul>
            <li><a href="#usage" class="pdf-link">Get Started</a></li>
            <li><a href="#features" class="pdf-link">Features</a></li>
          </ul>
        </div>

        <div class="card">
          <h3>Tech Stack</h3>
          <div class="tech">
            <div class="chip">Streamlit</div>
            <div class="chip">FastAPI</div>
            <div class="chip">HF Transformers</div>
            <div class="chip">SQLite</div>
          </div>
        </div>

      </aside>
    </div>

    <footer>
      <div>Generated README • TextMorph</div>
      <div class="right">
        <a class="btn" href="#">Contribute</a>
      </div>
    </footer>
  </div>
</body>
</html>
