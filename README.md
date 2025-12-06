# ⭐ Task 1 — Rating Prediction via Prompting
🎯 Objective

Build an LLM-based classifier that predicts a Yelp review rating (1–5 stars) purely through prompting and returns strict JSON:

{
  "predicted_stars": 4,
  "explanation": "Brief reasoning"
}


The task requires:

Designing three different prompting strategies

Comparing accuracy, JSON validity, and consistency

Running evaluation on ~200 sampled reviews

Providing a structured analysis

🧠 Approach Summary

Three prompts were designed:

Prompt A – Strict JSON Instruction

Prompt B – Few-Shot Examples

Prompt C – Rubric-Based Rating Criteria

Each prompt was executed on 200 Yelp reviews using LLaMA-3.1-70B-Instruct (OpenRouter) with deterministic settings.

JSON robustness increased as prompt structure became more explicit.

📌 Steps

Load Yelp dataset & sample 200 entries

Define three prompting strategies

Call LLM for each review

Parse JSON outputs & measure validity

Compute:

Accuracy

JSON Validity Rate

Behavioral consistency

Generate plots & comparison tables

📊 Evaluation Results
🔹 Accuracy Comparison
Prompt	Accuracy	JSON Validity
A	0.590	0.910
B	0.615	0.915
C	0.625	0.940

📌 Prompt C performed best because rubric-based guidance reduced ambiguity.

📈 Plots (Insert Image Here)

Add image from notebook (e.g., accuracy_plot.png)

![Task 1 Accuracy Plot](./Task2/feedback/plots.png)

# 🛠️ Task 2 — AI-Powered Feedback System (Django)
🎯 Objective

Build and deploy a two-dashboard web app where users submit ratings & reviews and receive an AI-generated response, while admins view summaries, actions, and analytics.

Includes:

User Dashboard

Admin Dashboard

AI response generation

Review summarization

Suggested actions

Persistent storage

Deployment

🧠 System Architecture

Backend: Django + Django REST Framework

Database: SQLite

LLM: LLaMA 3.1 70B (OpenRouter)

Frontend: Django Templates

Deployment: Render

OpenRouter headers were configured for production (Referer, X-Title, X-Request-ID, etc.) to avoid 401 errors.

📋 Steps
1️⃣ Build Backend & Models

Submission model

API endpoints (/api/submit/, /api/submissions/)

2️⃣ Implement LLM Logic

AI reply

Summary

Business actions

3️⃣ Build Dashboards

User: review form + AI response display

Admin: list with summary + actions + analytics

4️⃣ Deploy on Render

Add environment variables

Add correct OpenRouter headers

Configure static files

🔗 Live Links

(Insert your final deployment links here)

🌐 User Dashboard

👉 https://your-url/user

(Insert screenshot)

![User Dashboard](./Task2/feedback/User_dashboard.png)

🔐 Admin Dashboard

👉 https://your-url/admin_dashboard

(Insert screenshot)

![Admin Dashboard](./Task2/feedback/admin_dashboard.png)

📝 Features
✅ User Dashboard

Submit rating & review

Real-time AI-generated friendly response

Clear, simple UI

✅ Admin Dashboard

View all submissions

AI-generated summaries

Suggested actions

Total count & average rating