# 🚀 Blog Writing Agent

An advanced **AI-powered blog generation system** built using **LangGraph, LLMs, and Streamlit**.

This agent doesn't just write blogs — it **plans, researches, generates, and enhances content with images automatically**.

---

## ✨ Features

- 🧠 Intelligent topic understanding (Router Agent)
- 🔍 Automatic research using Tavily (optional)
- 🧩 Structured blog planning (Orchestrator)
- ✍️ Section-wise content generation (Workers)
- 🖼️ AI-powered image generation & placement
- 📦 Export as Markdown or ZIP bundle
- 📚 Past blog loading system
- ⚡ Real-time streaming UI with Streamlit

---

## 🏗️ Architecture

```
User Input
↓
Router → (Research?) → Orchestrator → Workers → Reducer
↓
Merge → Images → Final Blog
```

Built using:

- LangGraph (multi-agent workflow)
- Google Gemini (LLM)
- HuggingFace (Image generation)
- Tavily (Web search)
- Streamlit (Frontend)

---

## 📸 Demo Workflow

1. Enter a topic
2. Agent decides:
   - Need research or not
3. Generates blog structure
4. Writes sections in parallel
5. Adds diagrams/images
6. Outputs final blog

---

## ⚙️ Installation

```bash
git clone https://github.com/Engr-Mujeeb-Rahman/blog-writing-agent.git
cd blog-writing-agent

pip install -r requirements.txt

🔑 Setup Environment Variables

```
Create .env file:
GOOGLE_API_KEY=your_key
TAVILY_API_KEY=your_key
HUGGINGFACEHUB_API_TOKEN=your_token
```

▶️ Run the App

```
streamlit run app/frontend.py
```

📂 Project Structure

```
app/
 ├── frontend.py     # Streamlit UI
 ├── backend.py      # LangGraph logic
```


🧠 How It Works
1. Router
Decides:
Closed-book (no research)
Hybrid
Open-book (latest info)

2. Research (Optional)
Fetches real-world data using Tavily

3. Orchestrator
Creates structured blog outline

4. Workers
Each section generated independently

5. Reducer + Images
Merges content
Adds placeholders
Generates images
Final blog output

---

📦 Output
Markdown blog
Image assets
Downloadable ZIP bundle

---

⚠️ Limitations
Image generation depends on API reliability
Tavily required for real-time research
May hallucinate if no evidence is provided

---

🚀 Future Improvements
Add SEO optimization
Add blog publishing (Medium/WordPress)
Add RAG-based personalization
Multi-language support

---

👤 Author

Engr. M Mujeeb Ur Rahman
AI Engineer
