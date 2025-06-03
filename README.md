# Career-MultiAgent
# 💼 Career AI Agent

An AI-powered career assistant built using **LangGraph**, **LangChain**, and **Tavily API**, designed to assist users—especially fresh graduates—in navigating their job search journey. This intelligent agent follows a **multi-agentic flow**, invoking multiple LLMs across distinct nodes to simulate the reasoning process of a real-world career consultant.

---

## 🎯 Motivation

Many job seekers, particularly freshers, struggle to:
- Identify relevant job roles based on their project experience
- Write professional cover letters
- Search and filter meaningful job listings online

**Career AI Agent** automates all of the above by simulating a guided job application journey using powerful LLMs.

---

## ✨ Features

✅ Extracts structured profile data (skills, experience) from plain resumes  
✅ Generates intelligent job search queries based on your profile  
✅ Searches for live job listings via Tavily API  
✅ Matches and ranks job listings most suited to your background  
✅ Writes a customized cover letter tailored to the top-ranked role  
✅ All done through a **modular, extendable LangGraph-based architecture**

---
## 🔐 Required API Keys

To run this agent, you need the following keys:

| API Key        | Description                                   |
|----------------|-----------------------------------------------|
| `APIKEY     | Google Gemini API Key (via Google Colab `userdata) |
| `Search_key  | Tavily API Key (for live job search)          |

In Colab, add your keys using:

from google.colab import userdata
api_key = userdata.get("APIKEY")
search_key = userdata.get("Search_key")
## 🔀 Flow Diagram

text
        ┌──────────────┐
        │  User Input  │
        └──────┬───────┘
               ▼
        ┌──────────────┐
        │ Profile Node │ ← Extracts skills, experience
        └──────┬───────┘
               ▼
        ┌──────────────┐
        │ Job Search   │ ← Crafts search query + Tavily Search
        └──────┬───────┘
               ▼
        ┌──────────────┐
        │ Match Jobs   │ ← Selects top 3 jobs
        └──────┬───────┘
               ▼
        ┌──────────────┐
        │ Cover Letter │ ← Generates custom letter
        └──────┬───────┘
               ▼
             [ END ]

## Screenshots:
![image](https://github.com/user-attachments/assets/e8de2607-0512-4e8a-be50-aa648bbaac00)


