#  Multi-Agent Financial Assistant

This project sets up a **Multi-Agent AI Assistant** using the `phidata` framework, leveraging agents for both **web search** and **financial data analysis** through the Groq Llama-3.3-70b-versatile model.

---

##  Features

* **Financial Data Retrieval:** An agent specialized in fetching real-time stock prices, analyst recommendations, company fundamentals, and news using the `YFinanceTools`.
* **Web Search Capabilities:** An agent for general web search using `DuckDuckGo`.
* **Multi-Agent Coordination:** A `multi_AI_agent` is defined to delegate tasks between the Web Search and Financial Agents to provide comprehensive answers.
* **Playground Interface:** A web interface is set up using `phi.playground.Playground` for interactive testing of the agents.
* **Model Used:** All agents utilize the `Groq(id="llama-3.3-70b-versatile")` model.

---

##  Setup and Installation

### Prerequisites

* Python (3.8+)
* API keys for **Groq**, **Phi**, and **OpenAI** (Note: Groq and Phi keys are required for the agents/playground; the OpenAI key is loaded but not strictly used for the Groq model calls).

### 1. Environment Variables

Create a file named **`.env`** in the root directory and populate it with your API keys:


GROQ_API_KEY=YOUR_GROQ_API_KEY_HERE
PHI_API_KEY=YOUR_PHI_API_KEY_HERE
OPENAI_API_KEY=YOUR_OPENAI_API_KEY_HERE

#  Running the Agents
There are two main ways to interact with the agents: via a direct script execution or through the interactive web playground.
---------------------
## Running the Direct Execution Script
The financial_agent.py script demonstrates the multi_AI_agent in action by streaming a response to a specific financial query.

Bash
python financial_agent.py
This script executes the multi-agent task: "summarize analyst recommendation and share the latest news for NVDA".

## Running the Interactive Playground
The playground.py script starts a local web server, allowing you to interact with the individual Financial AI Agent and Web Search Agent through a user interface.
Bash
python playground.py
