<h1 align="center">🔍 LangSmith Masterclass</h1>
<h3 align="center">Tracing, Debugging & Observability for LLM Chains built with LangChain + Groq</h3>

<p align="center">
  <img src="https://img.shields.io/badge/LangChain-🦜-1C3C3C?style=for-the-badge" alt="LangChain"/>
  <img src="https://img.shields.io/badge/LangSmith-Tracing-3B82F6?style=for-the-badge" alt="LangSmith"/>
  <img src="https://img.shields.io/badge/Groq-Inference-F55036?style=for-the-badge" alt="Groq"/>
  <img src="https://img.shields.io/badge/Python-3.10+-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python"/>
</p>

<hr/>

<h2>📌 About the Project</h2>
<p>
  This repository is a hands-on playground for learning and testing <b>LangSmith</b> —
  the observability and tracing platform for LLM applications. Each script demonstrates
  a different chain pattern (simple calls, sequential chains, and more to come), instrumented
  end-to-end with LangSmith tracing so every step, prompt, and token can be inspected in the
  LangSmith dashboard.
</p>

<h2>🎯 What This Repo Covers</h2>
<ul>
  <li>✅ Setting up <code>LANGSMITH_TRACING</code> for automatic run logging</li>
  <li>✅ Simple single-turn LLM calls via <b>Groq</b> models</li>
  <li>✅ Sequential / multi-step chains using <b>LangChain Runnables (LCEL)</b></li>
  <li>✅ Debugging latency, token usage, and intermediate outputs per run</li>
  <li>✅ Organizing traces into projects inside the LangSmith UI</li>
</ul>

<h2>🗂️ Project Structure</h2>
<pre>
langsmith-masterclass/
├── 1_simple_llm_call.py       # Basic single LLM invocation with tracing
├── 2_sequential_chain.py      # Multi-step chain with tracing
├── .env.example                # Sample environment variables (safe to commit)
├── .gitignore
└── README.md
</pre>

<h2>⚙️ Setup & Installation</h2>

<h3>1️⃣ Clone the repository</h3>
<pre>
git clone https://github.com/Ashuto321/LangSmith-test-for-My-RAG-and-Other-Chains.git
cd LangSmith-test-for-My-RAG-and-Other-Chains
</pre>

<h3>2️⃣ Create a virtual environment</h3>
<pre>
python -m venv venv
venv\Scripts\activate      # Windows
source venv/bin/activate   # macOS/Linux
</pre>

<h3>3️⃣ Install dependencies</h3>
<pre>
pip install langchain langchain-groq python-dotenv langsmith
</pre>

<h3>4️⃣ Configure environment variables</h3>
<p>Create a <code>.env</code> file in the root directory (never commit this file):</p>
<pre>
GROQ_API_KEY=your_groq_api_key_here
LANGSMITH_TRACING=true
LANGSMITH_ENDPOINT=https://api.smith.langchain.com
LANGSMITH_API_KEY=your_langsmith_api_key_here
LANGSMITH_PROJECT=LANGSMITH_DEMO
</pre>

<blockquote>
  ⚠️ <b>Never commit your <code>.env</code> file.</b> Make sure it's listed in
  <code>.gitignore</code> before pushing to GitHub.
</blockquote>

<h2>▶️ Running the Scripts</h2>
<pre>
python 1_simple_llm_call.py
python 2_sequential_chain.py
</pre>
<p>
  After running any script, open the
  <a href="https://smith.langchain.com">LangSmith dashboard</a> →
  <b>Tracing</b> → your configured project name to view the full trace,
  including prompts, latency, and token counts.
</p>

<h2>🧠 Tech Stack</h2>
<table>
  <tr>
    <th>Layer</th>
    <th>Tool</th>
  </tr>
  <tr>
    <td>LLM Inference</td>
    <td>Groq (Llama models)</td>
  </tr>
  <tr>
    <td>Orchestration</td>
    <td>LangChain (LCEL / Runnables)</td>
  </tr>
  <tr>
    <td>Observability</td>
    <td>LangSmith</td>
  </tr>
  <tr>
    <td>Environment Management</td>
    <td>python-dotenv</td>
  </tr>
</table>

<h2>🚧 Roadmap</h2>
<ul>
  <li>⬜ Add RAG pipeline with tracing</li>
  <li>⬜ Add agent-based chain examples</li>
  <li>⬜ Add evaluation datasets in LangSmith</li>
  <li>⬜ Add custom feedback scoring for traces</li>
</ul>

<h2>🤝 Contributing</h2>
<p>
  This is primarily a personal learning repo, but suggestions and PRs around
  cleaner tracing patterns, new chain examples, or bug fixes are welcome.
</p>

<h2>📬 Connect</h2>
<p>
  <a href="https://github.com/Ashuto321">GitHub</a> •
  <a href="https://www.linkedin.com/">LinkedIn</a>
</p>

<hr/>
<p align="center"><i>Built while learning LLM observability, one traced call at a time. 🧵</i></p>
