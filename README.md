# 🔬 ResearchMind

ResearchMind is an AI-powered **multi-agent research system** that automates web research, information extraction, report generation, and report evaluation.

The system uses specialized AI agents powered by **Google Gemini**, **LangChain**, and **Tavily Search**, with an interactive **Streamlit** interface.

## 🚀 Features

- 🔎 **Search Agent** — Searches the web for relevant information using Tavily.
- 📖 **Reader Agent** — Extracts and analyzes information from selected web pages.
- ✍️ **Writer Agent** — Converts gathered research into a structured report.
- 🧠 **Critic Agent** — Evaluates the generated report and provides a score, strengths, and areas for improvement.
- 🌐 **Streamlit UI** — Provides a simple interface for entering research topics and viewing results.

## 🏗️ Architecture

```text
                    User
                     │
                     ▼
               Streamlit UI
                     │
                     ▼
              Research Pipeline
                     │
             ┌───────┴───────┐
             ▼               ▼
       Search Agent      Reader Agent
             │               │
        Tavily Search     Web Scraping
             │               │
             └───────┬───────┘
                     ▼
              Research Data
                     │
                     ▼
               Writer Agent
                     │
                     ▼
              Research Report
                     │
                     ▼
               Critic Agent
                     │
                     ▼
          Score + Feedback + Report
```

## 🛠️ Tech Stack

- **Python**
- **LangChain**
- **Google Gemini**
- **Tavily Search API**
- **Streamlit**
- **BeautifulSoup**
- **Requests**
- **Python Dotenv**

## 📁 Project Structure

```text
ResearchMind/
│
├── agents.py          # AI agents and LLM chains
├── pipeline.py        # Multi-agent research workflow
├── tools.py           # Web search and scraping tools
├── app.py             # Streamlit application
├── requirements.txt   # Python dependencies
├── .gitignore
└── README.md
```

## ⚙️ Setup

### 1. Clone the repository

```bash
git clone git@github.com:capslockpranjal/ResearchMind.git
cd ResearchMind
```

### 2. Create a virtual environment

```bash
python -m venv .venv
```

Activate it on Windows:

```bash
.venv\Scripts\activate
```

For macOS/Linux:

```bash
source .venv/bin/activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Configure API Keys

Create a `.env` file in the project root:

```env
GOOGLE_API_KEY=your_gemini_api_key
TAVILY_API_KEY=your_tavily_api_key
```

> Never commit your `.env` file or API keys to GitHub.

### 5. Run the application

```bash
streamlit run app.py
```

Then open the local Streamlit URL shown in your terminal.

## 🔄 How It Works

1. The user enters a research topic.
2. The Search Agent finds relevant web sources using Tavily.
3. The Reader Agent extracts useful information from the discovered pages.
4. The Writer Agent uses Gemini to generate a structured research report.
5. The Critic Agent evaluates the report and provides feedback.
6. The final research report and evaluation are displayed through Streamlit.

## 🔐 Environment Variables

| Variable | Purpose |
|---|---|
| `GOOGLE_API_KEY` | Authentication for Google Gemini |
| `TAVILY_API_KEY` | Authentication for Tavily web search |

API keys are loaded from environment variables and are not stored directly in the source code.

## 🔮 Future Improvements

- Multiple rounds of research and refinement
- Source credibility evaluation
- Research history
- Export reports as PDF
- Parallel agent execution
- Additional LLM providers
- Improved citation handling

## 👨‍💻 Author

**Pranjal Kumar**

GitHub: `capslockpranjal`

---

⭐ If you find ResearchMind useful, consider giving the repository a star.