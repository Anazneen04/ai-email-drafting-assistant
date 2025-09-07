# AI Email Drafting Assistant

---

## 🎯 Objective

The goal was to design and build a system where a staff member could submit a request via a simple form, and an AI chatbot would generate a high-quality first draft of an email in a Google Doc, ready for final review.

---

## ⚙️ How It Works

I built a complete, end-to-end automation using the following steps:

1.  **Input:** A user submits a request through a simple **Google Form**.
2.  **Data Bridge:** The form response is logged in a **Google Sheet**, creating a reliable data source for the workflow.
3.  **Automation (n8n):**
    * A **Trigger** in n8n watches the Google Sheet for new rows.
    * An **AI Node (OpenAI)** takes the data and, using a detailed prompt, generates the email draft.
    * A **Google Docs Node** creates a new document and inserts the AI-generated text.
4.  **Output:** The final draft is saved in a shared **Google Drive** folder, ready for human review.

---

## 🛠️ Technology Stack

* **Input & Data:** Google Forms & Google Sheets
* **Automation Platform:** n8n (`workflow.json` is included in this repository)
* **AI Engine:** OpenAI (GPT-4o)
* **Output & Storage:** Google Docs & Google Drive

---

## 💡 Key Learnings & Challenges

A key challenge during development was discovering that the standard n8n trigger for my data source was unavailable. I demonstrated resourcefulness by researching and implementing a more resilient solution using a spreadsheet as a stable intermediary, proving the system can be adapted to different environments. This project was also a great opportunity to quickly learn the n8n platform and build a functional prototype from scratch.

---

*For a detailed breakdown of the build process, design considerations, and cost analysis, please see the `Project_Report.md` file in this repository.*
