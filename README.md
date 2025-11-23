<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>TextMorph — Full README (VS-style)</title>
  <style>
    /* Visual Studio / VS Code inspired dark theme */
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
    /* responsive */
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
          <a class="btn" href="/mnt/data/TextMorph Readme.md.pdf">Original PDF</a>
        </nav>
      </div>
    </header>

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
        <section id="features" class="card">
          <h2>Key Features</h2>
          <div style="display:flex;gap:18px;flex-wrap:wrap">
            <div style="flex:1;min-width:260px">
              <h3 class="small">User Features</h3>
              <ul>
                <li><strong>Secure Authentication</strong> — JWT-based login, registration, OTP recovery (configurable).</li>
                <li><strong>Readability Analyzer</strong> — Flesch, Gunning Fog, SMOG, Coleman-Liau with visual graphs.</li>
                <li><strong>Summarization</strong> — Short / Medium / Long length control; domain-aware prompts.</li>
                <li><strong>Paraphrasing</strong> — Simple / Neutral / Advanced styles (FLAN-T5).</li>
                <li><strong>Side-by-Side Comparison</strong> — Original vs Generated outputs.</li>
                <li><strong>Feedback & History</strong> — Ratings, comments, and downloadable history.</li>
                <li><strong>Profile Management</strong> — Change password, security validation.</li>
              </ul>
            </div>
            <div style="flex:1;min-width:260px">
              <h3 class="small">Admin Features</h3>
              <ul>
                <li><strong>Model Management</strong> — Load domain-specific models from Google Drive (folder-only loader).</li>
                <li><strong>Account Limits</strong> — Max 2 admin accounts (configurable).</li>
                <li><strong>Usage Analytics</strong> — Visual reports, domain usage statistics.</li>
                <li><strong>Feedback Monitoring</strong> — Ratings + sentiment analysis.</li>
                <li><strong>Global Search</strong> — Search history & feedback across all users.</li>
                <li><strong>Full Audit View</strong> — Input/output visibility for compliance and debugging.</li>
                <li><strong>Hot-swap Models</strong> — Clear/reload models in runtime.</li>
              </ul>
            </div>
          </div>
        </section>

        <section id="installation" class="card" style="margin-top:18px">
          <h2>Installation</h2>
          <p class="muted">Quick local setup</p>
          <pre class="codeblock">git clone &lt;repository-link&gt;
cd TextMorph
pip install -r requirements.txt
# copy .env.example to .env and edit
streamlit run app.py</pre>
          <p class="muted">Models are expected in your Google Drive under:</p>
          <pre class="codeblock">/content/drive/MyDrive/flan_models/</pre>
          <p class="small">Model folder examples: <code>flan_t5_academic_1k</code>, <code>academic_1k</code>. The loader matches folders containing the domain name and a <code>config.json</code>. Zip extraction is <strong>disabled</strong>.</p>
        </section>

        <section id="usage" class="card" style="margin-top:18px">
          <h2>Usage Guide</h2>
          <ol>
            <li>Start the app: <code>streamlit run app.py</code></li>
            <li>Create or login with your account (if auth enabled)</li>
            <li>Choose domain &amp; (Admin) load model from Drive</li>
            <li>Enter/paste text or upload a document</li>
            <li>Select Summarize / Paraphrase and set readability preferences</li>
            <li>Generate &amp; review result; edit if needed</li>
            <li>Save to history and submit feedback</li>
            <li>Admins can view analytics, audit logs, and re-load models</li>
          </ol>
        </section>

        <section id="architecture" class="card" style="margin-top:18px">
          <h2>Architecture</h2>
          <p class="muted">Monolithic Streamlit frontend with a Python inference backend using Hugging Face transformers. Optional FastAPI backend for authentication and API access. SQLite is used for logging and history by default.</p>
          <table>
            <thead><tr><th>Component</th><th>Responsibility</th></tr></thead>
            <tbody>
              <tr><td>Streamlit UI</td><td>User interaction, admin panel, visualizations</td></tr>
              <tr><td>ML Engine</td><td>Tokenization, generation, readability scoring</td></tr>
              <tr><td>Google Drive</td><td>Model storage (mounted in Colab/VM)</td></tr>
              <tr><td>SQLite</td><td>History, feedback, audit logs</td></tr>
            </tbody>
          </table>
        </section>

        <section id="models" class="card" style="margin-top:18px">
          <h2>Models &amp; Loading</h2>
          <p class="muted">Primary models used and their roles.</p>
          <table>
            <thead><tr><th>Model</th><th>Purpose</th><th>Notes</th></tr></thead>
            <tbody>
              <tr><td>FLAN-T5 (domain)</td><td>Domain-specific summarization & paraphrase</td><td>Fine-tuned per domain (academic, news, medical, legal)</td></tr>
              <tr><td>Pegasus</td><td>High-quality abstractive summarization</td><td>Optional fallback</td></tr>
              <tr><td>BART</td><td>Balanced summarization & rewriting</td><td>Optional fallback</td></tr>
              <tr><td>NLTK</td><td>Readability metrics</td><td>Flesch, SMOG, Gunning Fog, Coleman-Liau</td></tr>
            </tbody>
          </table>
          <p class="small">Loader behaviour: folder-only, searches for folders matching domain patterns and containing <code>config.json</code>. If not found, it will raise an informative error. Loader chooses GPU if available.</p>
        </section>

        <section id="datasets" class="card" style="margin-top:18px">
          <h2>Datasets &amp; Evaluation</h2>
          <ul>
            <li><strong>WikiAuto</strong> — text simplification</li>
            <li><strong>Newsela</strong> — grade-level rewriting</li>
            <li><strong>ASSET</strong> — paraphrasing benchmark</li>
          </ul>
          <p class="muted">Evaluation metrics: ROUGE-L, BLEU, and Readability Delta (before vs after).</p>
        </section>

        <section id="roadmap" class="card" style="margin-top:18px">
          <h2>Roadmap</h2>
          <ul>
            <li>Add OCR &amp; PDF text extraction pipeline</li>
            <li>Multilingual support</li>
            <li>Batch &amp; large-file processing</li>
            <li>FastAPI production backend with auth &amp; rate-limiting</li>
            <li>ONNX/FP16 export for optimized inference</li>
            <li>Auto-scaling Docker images with GPU support</li>
          </ul>
        </section>

        <section id="screenshots" class="card" style="margin-top:18px">
          <h2>Screenshots</h2>
          <p class="muted">Add real UI images here. Placeholder list:</p>
          <ul>
            <li>Login Page</li>
            <li>Dashboard Overview</li>
            <li>Readability Graphs</li>
            <li>Summarization Result Page</li>
            <li>Admin Analytics Dashboard</li>
            <li>History View</li>
          </ul>
        </section>

        <section id="security" class="card" style="margin-top:18px">
          <h2>Security &amp; Privacy</h2>
          <ul>
            <li>JWT authentication and bcrypt for password hashing.</li>
            <li>Optional SMTP configuration for OTP &amp; notifications.</li>
            <li>Audit logs capture input/output for admin review (configurable retention).</li>
            <li>Recommend deploying behind HTTPS in production and limiting access to models and DB.</li>
          </ul>
        </section>

      </main>

      <aside>
        <div class="card">
          <h3>Quick Links</h3>
          <ul>
            <li><a class="pdf-link" href="/mnt/data/TextMorph Readme.md.pdf">Original PDF README</a></li>
            <li><a class="pdf-link" href="#usage">Get Started</a></li>
            <li><a class="pdf-link" href="#features">Features</a></li>
          </ul>
        </div>

        <div class="card" style="margin-top:16px">
          <h3>Tech Stack</h3>
          <div class="tech" style="margin-top:8px">
            <div class="chip">Streamlit</div>
            <div class="chip">FastAPI (optional)</div>
            <div class="chip">Hugging Face</div>
            <div class="chip">SQLite</div>
            <div class="chip">Docker</div>
          </div>
        </div>

        <div class="card" style="margin-top:16px">
          <h3>Project Structure</h3>
          <pre class="codeblock">TextMorph/
├── app.py
├── backend/
│   ├── auth.py
│   ├── models.py
│   ├── ml_engine.py
│   ├── readability.py
│   ├── history.py
│   ├── feedback.py
│   └── admin.py
├── requirements.txt
├── Dockerfile
└── docs/</pre>
        </div>

        <div class="card" style="margin-top:16px">
          <h3>Team</h3>
          <table>
            <thead><tr><th>Name</th><th>Role</th><th>Responsibility</th></tr></thead>
            <tbody>
              <tr><td>Add Name</td><td>ML Engineer</td><td>Model integration &amp; evaluation</td></tr>
              <tr><td>Add Name</td><td>Backend Developer</td><td>API, DB, Auth</td></tr>
              <tr><td>Add Name</td><td>Frontend Developer</td><td>Streamlit UI &amp; UX</td></tr>
              <tr><td>Add Name</td><td>Documentation</td><td>README, PPT, Reports</td></tr>
            </tbody>
          </table>
        </div>

        <div class="card" style="margin-top:16px">
          <h3>License</h3>
          <p class="muted">MIT License — free to use, modify, and share with attribution.</p>
        </div>

      </aside>
    </div>

    <footer>
      <div>Generated README • TextMorph</div>
      <div class="right">
        <a class="btn" href="#">Contribute</a>
        <a class="btn" href="/mnt/data/TextMorph Readme.md.pdf">View Original PDF</a>
      </div>
    </footer>
  </div>
</body>
</html>
