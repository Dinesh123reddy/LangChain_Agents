# 🤖 Gemini-powered Real-Time Web Search Agent using LangChain

A powerful AI agent that blends **LLM reasoning** with **live web search capabilities**. It uses **Gemini 1.5 Flash** from Google Generative AI to understand complex questions, and **SerpAPI** to fetch real-time information from the web.

## 🧠 What It Does

This intelligent agent can:
- Answer **current events and market trends**.
- Fetch **latest stock prices**, weather reports, and breaking news.
- Combine reasoning with real-time search to **generate better responses**.
- Understand natural language queries and route them to the appropriate tool (LLM vs Web Search).

## 📸 Example Use Case
```python
query = "Latest ICICI Bank share price in INR on NSE/BSE"

The agent will:
Use the SerpAPI tool to search real-time stock prices.
Feed the search results into the Gemini 1.5 Flash model.
Return a human-readable answer like: "The latest share price of ICICI Bank is ₹1,112.25 on NSE."

## 🛠 Architecture
+-------------------+        +-----------------+        +------------------+
|  User Query Input |  --->  | LangChain Agent |  --->  | Gemini 1.5 Flash |
+-------------------+        | + Tools (SERP)  |        +------------------+
                             +-----------------+
                                     |
                                     v
                          +----------------------+
                          | Real-Time Web Search |
                          |   (via SerpAPI)      |
                          +----------------------+

🔐 API Keys Setup
You'll need the following API keys:

Google Gemini API Key (for gemini_key)
SerpAPI Key (for real-time web search)

Set them in your environment:
export GOOGLE_API_KEY="your_gemini_api_key"
export SERPAPI_API_KEY="your_serpapi_key"

Or directly in your Python script (not recommended for production):
gemini_key = "your_gemini_api_key"
