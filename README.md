<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
</head>

<body>

<h1>✨ TextMorph — AI-powered Content Simplification, Summarization & Paraphrasing</h1>
<p>Transform long and complex text into clear, readable content using modern NLP models. Simple UI, powerful backend. 🚀</p>

<nav>
  <a href="#usage">Get Started</a> |
  <a href="#features">Features</a> |
  <a href="#architecture">Architecture</a> |
  <a href="#models">Models</a>
</nav>

<hr>


<h2>📑 Table of Contents</h2>
<ul>
  <li><a href="#overview">Overview</a></li>
  <li><a href="#features">Key Features</a></li>
  <li><a href="#installation">Installation</a></li>
  <li><a href="#usage">Usage Guide</a></li>
  <li><a href="#architecture">Architecture</a></li>
  <li><a href="#models">Models & Loading</a></li>
  <li><a href="#datasets">Datasets & Evaluation</a></li>
  <li><a href="#roadmap">Roadmap</a></li>
  <li><a href="#screenshots">Screenshots</a></li>
  <li><a href="#security">Security & Privacy</a></li>
  <li><a href="#team">Team</a></li>
  <li><a href="#license">License</a></li>
</ul>


<h2 id="overview">📘 Overview</h2>
<p>TextMorph is a lightweight NLP suite designed to simplify, rewrite, and summarize text with AI. Built with practical components and easy expandability.</p>

<ul>
  <li>⚡ Streamlit UI</li>
  <li>🧠 Hugging Face Transformers</li>
  <li>🎯 FLAN-T5 (domain-aware)</li>
  <li>🗂️ SQLite for storage</li>
  <li>🐳 Docker-ready design</li>
</ul>

<hr>

<h2 id="features">🔧 Key Features</h2>

<h3>👤 User Features</h3>
<ul>
  <li>🔐 Secure Authentication — JWT login, registration, OTP recovery.</li>
  <li>📊 Readability Analyzer — Flesch, Gunning Fog, SMOG, Coleman-Liau.</li>
  <li>📝 Summarization — short / medium / long lengths.</li>
  <li>🔄 Paraphrasing — simple, neutral, advanced styles.</li>
  <li>🆚 Side-by-Side Comparison.</li>
  <li>💾 History & ⭐ Feedback system.</li>
  <li>⚙️ Profile Management.</li>
</ul>

<h3>🛠️ Admin Features</h3>
<ul>
  <li>📥 Load domain-specific models.</li>
  <li>👑 Admin account limits.</li>
  <li>📈 Usage Analytics.</li>
  <li>💬 Feedback monitoring.</li>
  <li>🔍 Global search in history.</li>
  <li>🧾 Full audit visibility.</li>
  <li>♻️ Hot-swap models.</li>
</ul>

<hr>

<h2 id="installation">⚙️ Installation</h2>

<pre>
git clone &lt;repository-link&gt;
cd TextMorph
pip install -r requirements.txt
streamlit run app.py
</pre>

<p>📁 Models should be stored in Google Drive:</p>

<pre>/content/drive/MyDrive/flan_models/</pre>

<p>Examples: <code>flan_t5_academic_1k</code>, <code>academic_1k</code></p>

<hr>

<h2 id="usage">🚀 Usage Guide</h2>

<ol>
  <li>Run the app: <code>streamlit run app.py</code> ⚡</li>
  <li>Create/login account 🔐</li>
  <li>Select domain & load model 🎯</li>
  <li>Paste text or upload file 📄</li>
  <li>Choose Summarize / Paraphrase 🔄</li>
  <li>Review results ✨</li>
  <li>Save history & give feedback ⭐</li>
  <li>Admins view analytics 📊</li>
</ol>

<hr>

<h2 id="architecture">🏗️ Architecture</h2>
<p>Simple and modular architecture focusing on accessibility and performance.</p>

<table>
<tr><th>Component</th><th>Responsibility</th></tr>
<tr><td>🌐 Streamlit UI</td><td>User interaction & admin panel</td></tr>
<tr><td>🤖 ML Engine</td><td>Tokenization & generation</td></tr>
<tr><td>🔒 Google Drive</td><td>Model storage</td></tr>
<tr><td>🗄️ SQLite</td><td>History & feedback</td></tr>
</table>

<hr>

<h2 id="models">🧩 Models & Loading</h2>

<table>
<tr><th>Model</th><th>Purpose</th><th>Notes</th></tr>
<tr><td>FLAN-T5</td><td>Summarization & paraphrasing</td><td>Domain tuned</td></tr>
<tr><td>Pegasus</td><td>Summarization & paraphrasing</td><td>Optional</td></tr>
<tr><td>BART</td><td>Summarization & paraphrasing</td><td>Optional</td></tr>
</table>

<hr>

<h2 id="datasets">📚 Datasets & Evaluation</h2>

<ul>
  <li>📘 academic->ccdv/arxiv-summarization</li>
  <li>📰 news->cnn_dailymail</li>
  <li>📝 medical->ccdv/pubmed-summarization</li>
  <li>📘 legal->billsum</li>
</ul>

<p>📏 Metrics used: ROUGE-L, BLEU, Readability delta.</p>

<hr>

<h2 id="roadmap">🛣️ Roadmap</h2>

<ul>
  <li>🖨️ OCR & PDF extraction</li>
  <li>🌍 Multilingual capabilities</li>
  <li>📦 Batch/large-file support</li>
  <li>⚡ FastAPI backend</li>
  <li>⚙️ ONNX acceleration</li>
  <li>🐳 GPU-powered Docker images</li>
</ul>

<hr>

<h2 id="screenshots">🖼️ Screenshots (Placeholders)</h2>
<ul>
  <li>🔑 Login</li>
  <li>📊 Dashboard</li>
  <li>📈 Graphs</li>
  <li>📝 Summarization Output</li>
  <li>📉 Analytics Panel</li>
  <li>📜 History View</li>
</ul>

<hr>

<h2 id="security">🔐 Security & Privacy</h2>

<ul>
  <li>🔑 JWT authentication</li>
  <li>📧 OTP via SMTP</li>
  <li>📜 Audit logs</li>
  <li>🔒 Use HTTPS in production</li>
</ul>

<hr>


<hr>

<h2>👥 Team</h2>

<table>
<tr><th>Name</th><th>Role</th><th>Responsibility</th></tr>
<tr><td>Add Name</td><td>ML Engineer 🤖</td><td>Model integration</td></tr>
<tr><td>Add Name</td><td>Backend Developer 🔧</td><td>API & Auth</td></tr>
<tr><td>Add Name</td><td>Frontend Developer 🎨</td><td>UI/UX</td></tr>
<tr><td>Add Name</td><td>Documentation ✍️</td><td>Reports & README</td></tr>
</table>

<hr>

<h2>📄 License</h2>
<p>MIT License — free to use, modify and share. 👐</p>

</body>
</html>



