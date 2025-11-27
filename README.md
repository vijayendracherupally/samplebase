<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
</head>

<body>

<h1>✨ TextMorph — AI-powered Content Simplification, Summarization & Paraphrasing</h1>
<p>
TextMorph is an AI-driven text processing system designed to make complex content more understandable, 
structured, and reader-friendly. Built around state-of-the-art NLP models, the platform transforms 
dense writing into clearer formats without losing meaning or context. Whether used by students, 
researchers, writers, or professionals, TextMorph provides a seamless way to simplify, summarize, 
or rewrite content with exceptional quality.
</p>

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

<hr>

<h2 id="overview">📘 Overview</h2>
<p>
TextMorph was designed to address a common challenge: working with long, technical, or poorly structured 
text. Many students and professionals struggle to condense large amounts of information into clear, 
understandable summaries, while others require paraphrasing tools that preserve meaning but enhance 
readability. TextMorph solves these problems by combining an intuitive interface with advanced language 
models that excel at understanding context, tone, and linguistic structure.
</p>
<p>
Unlike traditional summarizers or paraphrasers that rely on static rules, TextMorph adapts to the content 
it processes. The system supports multiple domains, such as academic research, medical information, news 
articles, and legal documents. Each domain can be paired with a specialized, fine-tuned model that delivers 
better accuracy and improves the usefulness of generated outputs. This allows the platform to transform 
highly technical documents while ensuring the integrity of the information remains intact.
</p>
<p>
The platform’s goal is to democratize access to high-quality NLP tools. Users do not need a background 
in machine learning; instead, they interact with a clean web interface powered by Streamlit, where text 
processing is as simple as entering content and choosing the desired transformation. The system is portable, 
cloud-ready, and optimized for CUDA or CPU environments, making it adaptable for research labs, classrooms, 
content teams, and enterprise environments.
</p>

<hr>

<h2 id="features">🔧 Key Features</h2>

<h3>👤 User Features</h3>

<p>
TextMorph offers a smooth and refined experience tailored for everyday users who want powerful text 
transformation tools without dealing with technical complexity. The platform guides users through an 
intuitive workflow where they can paste or upload content, choose how they want it transformed, and 
instantly view clean, structured results. Every feature is designed to help users process information 
more efficiently—whether summarizing research papers, simplifying complex articles, or paraphrasing 
content for better clarity. The system stores previous results, tracks readability metrics, and 
provides a convenient side-by-side comparison for easier evaluation. Overall, the goal is to make 
writing and comprehension faster, clearer, and more accessible.
</p>

<ul>
  <li>Secure login with JWT-based authentication.</li>
  <li>Easy-to-use input system for pasting or uploading documents.</li>
  <li>Summarization with adjustable lengths (short, medium, long).</li>
  <li>Paraphrasing in simple, neutral, and advanced tones.</li>
  <li>Real-time readability analysis with detailed scoring.</li>
  <li>Side-by-side comparison of original and generated text.</li>
  <li>Automatic saving of history for later access.</li>
  <li>Feedback system to rate and improve results.</li>
  <li>Support for PDF and text extraction for long documents.</li>
</ul>

<hr>

<h3>🛠️ Admin Features</h3>

<p>
Administrators have deeper control over TextMorph, allowing them to manage the platform’s operations, 
monitor user activity, and optimize performance. The admin environment provides analytical dashboards 
that reveal how the system is being used, what models are performing well, and which areas may require 
updates or improvements. Admins can upload new domain-specific models, configure permissions, track 
feedback from users, and maintain detailed audit logs. By managing models, monitoring usage patterns, 
and ensuring system security, administrators keep TextMorph efficient, reliable, and aligned with its 
intended purpose.
</p>

<ul>
  <li>Ability to upload and load domain-specific FLAN-T5 models.</li>
  <li>Administrative access for managing user accounts.</li>
  <li>Usage analytics with charts and real-time insights.</li>
  <li>Full access to global history with advanced search filters.</li>
  <li>Feedback monitoring to understand model strengths and weaknesses.</li>
  <li>Audit logging for tracking critical user and system actions.</li>
  <li>Model hot-swapping without restarting the app.</li>
  <li>Strict limit of two super-admin accounts for security.</li>
  <li>Tools for monitoring workflow patterns and platform performance.</li>
</ul>


<hr>



<hr>

<h2 id="architecture">🏗️ Architecture</h2>
<p>
TextMorph follows a layered architecture that separates user interaction, model inference, and data 
management. This modular design ensures that each component can be optimized independently. The Streamlit 
frontend handles visual rendering and input collection. It communicates with the model processing layer, 
which handles tokenization, generation, and evaluation using modern Transformer architectures.
</p>
<p>
Google Drive is utilized as a flexible model repository, allowing users to store multiple fine-tuned 
variants without bundling them directly into the application. SQLite serves as the internal database for 
user sessions, text histories, and logs. This lightweight database makes TextMorph portable and 
self-contained, ideal for offline environments or small-scale deployments where setting up a full 
database server would be unnecessary.
</p>
<p>
This architecture also simplifies Docker deployment. The application can be containerized easily, with 
external models mounted as volumes or downloaded on startup. Future versions plan to introduce a 
FastAPI-based backend to separate UI from inference for improved performance and scaling.
</p>

<hr>

<h2 id="models">🧩 Models & Loading</h2>

<p>
TextMorph supports several state-of-the-art Transformer models from the Hugging Face ecosystem, each 
designed to handle specific text transformation tasks. The primary model used is <strong>FLAN-T5</strong>, a 
highly flexible instruction-tuned model that performs exceptionally well on summarization and paraphrasing, 
especially when fine-tuned on targeted domain datasets. <strong>Pegasus</strong> is included as a powerful option for 
abstractive summarization, particularly effective when dealing with structured, information-rich 
documents such as research papers, news reports, and technical explanations. <strong>BART</strong> offers a solid 
balance in rewriting and paraphrasing, providing outputs that preserve meaning while improving fluency 
and readability.
</p>

<p>
All models are loaded dynamically through the Transformers library, meaning TextMorph initializes only 
the models required for a given task. This makes the system memory-efficient and allows users to switch 
between models without restarting the application. Domain-specific and custom-trained model checkpoints 
stored in Google Drive can also be loaded seamlessly with a single click. This flexibility makes it easy 
to create specialized workflows for academic, legal, medical, and general-purpose writing needs.
</p>

<table border="1" cellpadding="10" cellspacing="0" style="border-collapse: collapse; margin-top: 15px;">
  <tr style="background-color: #f2f2f2; font-weight: bold;">
    <th>Model Name</th>
    <th>Purpose</th>
    <th>Description</th>
  </tr>

  <tr>
    <td>FLAN-T5</td>
    <td>Summarization & Paraphrasing</td>
    <td>
      FLAN-T5 is an instruction-tuned variant of T5, capable of following task-level prompts efficiently. 
      In TextMorph, it serves as the primary engine for generating summaries, simplified text, and 
      paraphrases, performing exceptionally well across domains after fine-tuning.
    </td>
  </tr>

  <tr>
    <td>Pegasus</td>
    <td>Abstractive Summarization</td>
    <td>
      Pegasus excels at producing high-quality abstractive summaries, especially for complex articles and 
      research-focused content. Its architecture is optimized for reconstructing masked sentences, making 
      it ideal for long-form summarization tasks.
    </td>
  </tr>

  <tr>
    <td>BART</td>
    <td>Paraphrasing & Rewriting</td>
    <td>
      With its bidirectional encoder and autoregressive decoder, BART generates fluent and coherent 
      paraphrases. It is highly effective for rewriting text while maintaining its original meaning.
    </td>
  </tr>

  <tr>
    <td>Custom FLAN-T5 Models</td>
    <td>Domain-Specific NLP Tasks</td>
    <td>
      Users can store custom fine-tuned FLAN-T5 models in Google Drive and load them directly from the 
      interface. These models offer improved performance for domain-sensitive tasks such as academic, 
      medical, or legal rewriting and summarization.
    </td>
  </tr>
</table>


<hr>

<h2 id="datasets">📚 Datasets & Evaluation</h2>
<p>
To ensure the highest possible output quality, TextMorph incorporates evaluation principles derived 
from widely recognized datasets in summarization and paraphrasing research. Each dataset represents a 
unique writing style and vocabulary range: ArXiv for scientific writing, CNN/DailyMail for 
journalistic content, PubMed for medical literature, and BillSum for legal text. 
</p>
<p>
Evaluation is conducted through multiple metrics. ROUGE and BLEU measure how closely outputs match 
reference summaries, while lexical diversity and readability metrics analyze clarity and style. 
This combination ensures that TextMorph produces text that is not only accurate but also easy to 
understand.
</p>

<hr>

<h2 id="roadmap">🛣️ Roadmap</h2>
<p>
Future updates aim to transform TextMorph into a more robust, multi-functional NLP platform. 
Upcoming features include more advanced PDF extraction techniques capable of recognizing 
headings, tables, and multi-column layouts. Multilingual models will expand support to 
several global languages. Batch processing will allow users to work with entire folders or 
document collections at once.
</p>
<p>
A dedicated FastAPI backend is in development to support scalable deployments and expert 
workflows. Optimizations using ONNX and GPU-accelerated Docker images will significantly reduce 
latency during inference. Additional improvements include customizable user roles, real-time 
collaboration, and integrations with educational systems or enterprise tools.
</p>

<hr>

<h2 id="screenshots">🖼️ Screenshots</h2>
<p>
The application includes several intuitive screens designed for clarity and productivity. 
The login interface guides users through secure access. The main dashboard contains quick 
navigation options to load models, upload files, or begin text transformation. The analytics 
panel helps administrators monitor global system activity through visual charts. The 
summarization and paraphrasing pages include structured views that allow users to compare 
original and transformed content effortlessly.
</p>

<hr>

<h2 id="security">🔐 Security & Privacy</h2>

<p>
TextMorph implements a multi-layered security model designed to protect user data and maintain a 
responsible and trustworthy environment. The system ensures that all stored passwords are hashed using 
strong cryptographic methods, preventing exposure of raw credentials even if the database is accessed. 
Authentication is handled through JWT tokens, which maintain user sessions securely without requiring 
the server to store session data. These tokens include expiry mechanisms to limit unauthorized access 
and reduce long-term session risks. For account recovery, an OTP-based verification system is used, 
ensuring that only legitimate users can regain access to their accounts through time-sensitive codes.
</p>

<p>
To support transparency and responsible platform usage, the system maintains detailed audit logs that 
record critical events such as login attempts, password-reset activity, account changes, and major 
administrative actions. These logs allow both developers and administrators to monitor potential misuse 
and maintain operational oversight. Although advanced deployment environments may integrate encryption 
or additional network-level protections, the core platform itself does not require HTTPS for general 
functionality and remains fully operational in secure offline or local environments.
</p>

<table border="1" cellpadding="10" cellspacing="0" style="border-collapse: collapse; margin-top: 15px;">
  <tr style="background-color: #f2f2f2; font-weight: bold;">
    <th>Security Feature</th>
    <th>Purpose</th>
    <th>Description</th>
  </tr>

  <tr>
    <td>Password Hashing (bcrypt)</td>
    <td>Protect stored credentials</td>
    <td>
      All user passwords are transformed using bcrypt hashing before being stored. This ensures that 
      even if the database is accessed, raw passwords cannot be recovered or misused.
    </td>
  </tr>

  <tr>
    <td>JWT Authentication</td>
    <td>Session management</td>
    <td>
      JSON Web Tokens maintain secure, stateless sessions. Token expiry adds an additional layer of 
      protection by limiting how long a session remains valid.
    </td>
  </tr>

  <tr>
    <td>OTP-Based Recovery</td>
    <td>Account recovery</td>
    <td>
      Users receive temporary, time-sensitive one-time passwords via email to reset their accounts. 
      This ensures recovery can only be performed by the legitimate user.
    </td>
  </tr>

  <tr>
    <td>Audit Logging</td>
    <td>User activity tracking</td>
    <td>
      Every critical system event—including login attempts, incorrect password entries, and admin 
      operations—is stored in an audit log to support monitoring and behavioral analysis.
    </td>
  </tr>

  <tr>
    <td>Admin Monitoring Tools</td>
    <td>Platform governance</td>
    <td>
      Administrators have access to logs and activity summaries that help them monitor system use, 
      identify unusual patterns, and ensure the platform is being used responsibly.
    </td>
  </tr>

  <tr>
    <td>Local / Offline Friendly</td>
    <td>Secure environments without HTTPS</td>
    <td>
      TextMorph functions securely in local or internal environments without requiring HTTPS. 
      Core security features operate independently of network-level encryption.
    </td>
  </tr>
</table>


<hr>

<h2 id="team">👥 Team</h2>

<table border="1" cellpadding="10" cellspacing="0" style="border-collapse: collapse; margin-top: 10px; width: 100%;">
  <tr style="background-color: #f2f2f2; font-weight: bold; text-align: left;">
    <th>Name</th>
    <th>Contribution</th>
    <th>GitHub</th>
  </tr>

  <tr>
    <td>Name</td>
    <td>Implemented JWT-based authentication, user profiles, and session management.</td>
    <td><a href="#" target="_blank">GitHub</a></td>
  </tr>

  <tr>
    <td>Name</td>
    <td>Designed and developed the UI/UX, dashboard layout, and navigation flow.</td>
    <td><a href="#" target="_blank">GitHub</a></td>
  </tr>

  <tr>
    <td>Name</td>
    <td>Integrated summarization and paraphrasing models and optimized inference performance.</td>
    <td><a href="#" target="_blank">GitHub</a></td>
  </tr>

  <tr>
    <td>Name</td>
    <td>Integrated summarization and paraphrasing models and optimized inference performance.</td>
    <td><a href="#" target="_blank">GitHub</a></td>
  </tr>

  <tr>
    <td>Name</td>
    <td>Integrated summarization and paraphrasing models and optimized inference performance.</td>
    <td><a href="#" target="_blank">GitHub</a></td>
  </tr>
</table>

<hr>


<h2 id="installation">⚙️ Installation</h2>
<p>
Installing TextMorph is straightforward and designed to cater to users from various technical backgrounds. 
Once the repository is downloaded, users only need to install the required Python packages through the 
provided <code>requirements.txt</code>. The Streamlit interface requires no additional setup, and launching 
the app opens an interactive web dashboard in the browser. 
</p>
<p>
For users working on cloud platforms such as Google Colab, the system integrates seamlessly with Google 
Drive. Models can be stored remotely, allowing users to access large fine-tuned weights without needing 
local storage. This enables large-scale experiments and production-like workflows even on lightweight 
devices such as Chromebooks.
</p>

<hr>

<h2 id="usage">🚀 Usage Guide</h2>
<p>
Using TextMorph begins with authentication. Once inside, the user is guided through a streamlined workflow 
that starts with selecting the domain or model best suited for their task. The interface supports both 
short text entries and long-form documents. Users can select summarization length, rewriting style, tone, 
and processing preferences before generating results. 
</p>
<p>
The platform processes text in seconds, providing refined output along with structured comparisons 
that highlight differences between the original and generated content. Users can revise input text, retry 
operations, adjust parameters, or save the results for future use. All previous work is accessible in the 
History panel, organized chronologically to help users track their progress over time.
</p>




<h2 id="license">📄 License</h2>
<p>
TextMorph is released under the MIT License, granting users the freedom to use, modify, and 
redistribute the project with minimal restrictions. The license encourages community 
contributions and ensures the project remains open and accessible for education, research, 
and personal development.
</p>

</body>
</html>






