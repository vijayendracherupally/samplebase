<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>TextMorph — Clean README</title>
</head>

<body>

<p>AI-powered content simplification, summarization & paraphrasing — domain-aware, Streamlit-based.</p>

<nav>
  <a href="#usage">Get Started</a> |
  <a href="#features">Features</a> |
  <a href="#architecture">Architecture</a> |
  <a href="#models">Models</a>
</nav>

<hr>

<h2 id="overview">Overview</h2>
<p>TextMorph is a modular NLP suite built to transform complex domain text into clear, readable outputs using transformer models tuned per-domain.</p>

<ul>
  <li>Streamlit UI</li>
  <li>Hugging Face Transformers</li>
  <li>FLAN-T5 (domain)</li>
  <li>SQLite / Logs</li>
  <li>Docker-ready</li>
</ul>

<hr>

<h2 id="features">Key Features</h2>

<h3>User Features</h3>
<ul>
  <li>Secure Authentication — JWT login, registration, OTP recovery.</li>
  <li>Readability Analyzer — Flesch, Gunning Fog, SMOG, Coleman-Liau.</li>
  <li>Summarization — length control; domain-aware prompts.</li>
  <li>Paraphrasing — simple / neutral / advanced styles.</li>
  <li>Side-by-Side Comparison — original vs output.</li>
  <li>Feedback & History — ratings, comments, exports.</li>
  <li>Profile Management — password change, validation.</li>
</ul>

<h3>Admin Features</h3>
<ul>
  <li>Model Management — load domain models from Drive.</li>
  <li>Account Limits — max admin accounts.</li>
  <li>Usage Analytics — visual reports.</li>
  <li>Feedback Monitoring — sentiment analysis.</li>
  <li>Global Search — search all histories.</li>
  <li>Full Audit View — inputs/outputs.</li>
  <li>Hot-swap Models — reload at runtime.</li>
</ul>

<hr>

<h2 id="installation">Installation</h2>

<pre>
git clone &lt;repository-link&gt;
cd TextMorph
pip install -r requirements.txt
streamlit run app.py
</pre>

<p>Models are expected in Google Drive:</p>

<pre>/content/drive/MyDrive/flan_models/</pre>

<p>Examples: <code>flan_t5_academic_1k</code>, <code>academic_1k</code></p>

<hr>

<h2 id="usage">Usage Guide</h2>

<ol>
  <li>Run: <code>streamlit run app.py</code></li>
  <li>Create/login account</li>
  <li>Select domain & load model</li>
  <li>Enter text or upload file</li>
  <li>Select Summarize / Paraphrase</li>
  <li>Review results</li>
  <li>Save history; give feedback</li>
  <li>Admins can view analytics and logs</li>
</ol>

<hr>

<h2 id="architecture">Architecture</h2>
<p>Streamlit frontend + Python backend using Transformers. SQLite for history and logs. Drive for model storage.</p>

<table>
<tr><th>Component</th><th>Responsibility</th></tr>
<tr><td>Streamlit UI</td><td>User interaction & admin panel</td></tr>
<tr><td>ML Engine</td><td>Tokenization & text generation</td></tr>
<tr><td>Google Drive</td><td>Model storage</td></tr>
<tr><td>SQLite</td><td>History & feedback</td></tr>
</table>

<hr>

<h2 id="models">Models & Loading</h2>

<table>
<tr><th>Model</th><th>Purpose</th><th>Notes</th></tr>
<tr><td>FLAN-T5 (domain)</td><td>Summarization & paraphrasing</td><td>Fine-tuned per domain</td></tr>
<tr><td>Pegasus</td><td>Summarization</td><td>Optional</td></tr>
<tr><td>BART</td><td>Balance between rewrite & summary</td><td>Optional</td></tr>
<tr><td>NLTK</td><td>Readability metrics</td><td>Flesch, SMOG, Fog</td></tr>
</table>

<hr>

<h2 id="datasets">Datasets & Evaluation</h2>

<ul>
  <li>WikiAuto — simplification</li>
  <li>Newsela — grade-level rewriting</li>
  <li>ASSET — paraphrasing benchmark</li>
</ul>

<p>Metrics: ROUGE-L, BLEU, readability shifts.</p>

<hr>

<h2 id="roadmap">Roadmap</h2>

<ul>
  <li>OCR & PDF extraction</li>
  <li>Multilingual support</li>
  <li>Batch processing</li>
  <li>FastAPI backend</li>
  <li>ONNX export</li>
  <li>Docker GPU images</li>
</ul>

<hr>

<h2 id="screenshots">Screenshots (placeholders)</h2>
<ul>
  <li>Login</li>
  <li>Dashboard</li>
  <li>Graphs</li>
  <li>Summarization View</li>
  <li>Admin Analytics</li>
  <li>History View</li>
</ul>

<hr>

<h2 id="security">Security & Privacy</h2>

<ul>
  <li>JWT authentication + bcrypt hashing</li>
  <li>SMTP for OTP</li>
  <li>Audit logs</li>
  <li>HTTPS recommended</li>
</ul>

<hr>

<h2>Project Structure</h2>

<pre>
TextMorph/
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
└── docs/
</pre>

<hr>

<h2>Team</h2>

<table>
<tr><th>Name</th><th>Role</th><th>Responsibility</th></tr>
<tr><td>Add Name</td><td>ML Engineer</td><td>Model integration</td></tr>
<tr><td>Add Name</td><td>Backend Developer</td><td>API & Auth</td></tr>
<tr><td>Add Name</td><td>Frontend Developer</td><td>UI/UX</td></tr>
<tr><td>Add Name</td><td>Documentation</td><td>Reports & README</td></tr>
</table>

<hr>

<h2>License</h2>
<p>MIT License — free to use and modify.</p>

</body>
</html>

