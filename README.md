# 🤖 Gemini-powered Real-Time Web Search Agent using LangChain

A powerful AI agent that blends **LLM reasoning** with **live web search capabilities**. It uses **Gemini 1.5 Flash** from Google Generative AI to understand complex questions, and **SerpAPI** to fetch real-time information from the web.

## 🧠 What It Does

This intelligent agent can:
- Answer **current events and market trends**.
- Fetch **latest stock prices**, weather reports, and breaking news.
- Combine reasoning with real-time search to **generate better responses**.
- Understand natural language queries and route them to the appropriate tool (LLM vs Web Search).

## 📸 Example Use Case

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
