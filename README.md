# MotivAgent---Custom-Agent-Loop
It’s a custom agent loop using structured prompts and code to manage thought-action-observation-answer steps.

## This project uses an "agent-like" behavior 

 ### What is used:

    1) A manual agent loop is implemented with:
    
    2) Thought → Action → Observation → Answer structure
    
    3) Action parsing via regex
    
    4) Custom defined tools (mindset_search, wikipedia, calculate)
    
    5) Re-injection of observations into the prompt loop
  
  
  This is what we call a manual or "lightweight agent" pattern — it mimics how agents operate by orchestrating reasoning and actions without using LangChain’s built-in AgentExecutor or Tool abstraction.


## 🤖 Motivational Coach Chatbot

This project is a **Motivational Coach Chatbot Agent** built using [LangChain](https://www.langchain.com/), [Groq](https://groq.com/), and custom action tools like Wikipedia search, mindset tips, and math calculation. The chatbot follows a structured reasoning-action-observation-answer loop to provide motivating, actionable responses.

## 💡 Features

- LLM-powered chatbot using **Groq LLaMA3** and **Gemma2-9b-It**
- Structured Reasoning Chain: 
  - **Thought → Action → Observation → Answer**
- Custom actions:
  - `mindset_search`: Provide motivational insights
  - `wikipedia`: Fetch snippets from Wikipedia
  - `calculate`: Perform basic math calculations
- Agent-style prompting for deeper interaction
- Modular code with query loop and action detection

## 📁 File Structure

- `motivation_coach_using_custome_agent.ipynb`: Jupyter notebook with full implementation
- `.env`: File storing API keys (not included)

## 🔧 Setup Instructions

### 1. Clone the Repository

git clone https://github.com/gurmeet289/motivational-coach-chatbot.git
cd motivational-coach-chatbot

---

### 2. Create and Activate Environment

conda create -p venv python=3.10 -y
conda activate venv

---

### 3. Install Requirements

pip install -r requirements.txt

---

### 4. Set Up .env File

GOOGLE_API_KEY=your_google_api_key
TAVILY_API_KEY=your_tavily_api_key  # optional
GROQ_API_KEY=your_groq_api_key
LANGCHAIN_API_KEY=your_langchain_api_key
LANGCHAIN_PROJECT=your_langchain_project_name

---

### 5. Run the Notebook

jupyter notebook

---

## 🧠 Prompt Format (Agent Loop)

The agent always follows:

    Thought: I need to ...
    Action: [action_name]: [input]
    PAUSE
    
    Observation: ...
    Answer: ...


## Supported Actions:

| Action          | Description                              | Example                             |
|-----------------|------------------------------------------|-------------------------------------|
| `mindset_search`| Returns motivational insight on a keyword| `mindset_search: discipline`        |
| `wikipedia`     | Searches Wikipedia for a topic           | `wikipedia: Artificial Intelligence`|
| `calculate`     | Evaluates a basic math expression        | `calculate: 50 * 25`                |


## 💬 Sample Queries

query("How can I become more disciplined?")
query("Tell me a quote about success.")
query("What's 50 * 25?")
query("Tell me about Artificial Intelligence from Wikipedia.")


## 🚀 Roadmap

1) Add memory for contextual follow-ups

2) Enhance mindset database with dynamic sources

3) Add speech-to-text and text-to-speech interface

4) Deploy as API or web chatbot
   

## 🙌 Acknowledgments

1) LangChain

2) Groq Cloud

3) Wikipedia API
