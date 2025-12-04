AI Chat Conversation Emotion Analysis

Using Hugging Face Dataset + Regex Cleaning + Parallel Processing + SQLite Database Storage + Visualization

📄 Project Overview

This project focuses on emotion analysis of AI-generated conversations.
We fetch large-scale conversations from Hugging Face (lmsys/lmsys-chat-1m), extract ONLY assistant responses, clean them using Regex, analyze emotions using a Transformer-based emotion classification model, and finally store Raw, Cleaned, and Output results in SQLite Database, which is mounted on Google Drive for persistence.

The pipeline includes parallel processing, dataset handling, database integration, visualization, and NLP model inference, making this a real-world production-style workflow.

🚀 Features
Feature	
Google Drive Mounted	
Hugging Face Dataset Integration	
Extract Only AI Assistant Messages	
Regex-Based Data Cleaning	
Parallel Processing	
Database Storage (No manual folders)	
Transformer Emotion Model	
Output Visualization	
Real World Project Standard	
🧠 Tech Stack

Python

Hugging Face Transformers

Datasets

PyTorch

Regex processing

Parallel processing (ProcessPoolExecutor)

SQLite + SQLAlchemy

Pandas

Matplotlib

Google Colab + Google Drive

📂 Data Flow Architecture
              Hugging Face Dataset
                   ↓
              Extract Assistant Messages
                   ↓ (parallel)
              raw_data table
                   ↓ (regex + parallel)
              cleaned_data table
                   ↓ (Emotion Model)
              output_data table
                   ↓
              Visualisation (Pie/Bar Charts)
                   ↓
             Stored in Google Drive DB

📌 Database Structure
Table Name	Description
raw_data	Original assistant text extracted from dataset
cleaned_data	Regex-cleaned text + original text
output_data	Cleaned text + emotion prediction results
📜 How to Run
Step 1 — Open Google Colab

Upload the final notebook code and run step by step.

Step 2 — Install dependencies
!pip install --quiet transformers datasets tqdm sentencepiece sqlalchemy joblib

Step 3 — Mount Drive & Run all cells

Google Drive will store:

MyDrive/ai_chat_emotion.db

📊 Result Visualization

Two graphs are generated:

✔ Pie Chart — Emotion Distribution
✔ Bar Graph — Emotion Counts

Example Output:

Joy: 528
Neutral: 420
Anger: 90
Sadness: 75
...


You can modify graph type anytime.

📈 Possible Improvements (if future scope needed)

Deploy model API using FastAPI/Flask

Build dashboard using Streamlit/Gradio

Apply deep cleaning + token normalization

Train custom emotion classifier on own dataset

Add temporal conversation trend analysis

Export results to CSV/Excel automatically

🎯 Conclusion

This project successfully:

✔ Extracts AI chats only
✔ Cleans using Regex
✔ Speeds execution using Parallel Processing
✔ Stores data in Database (NO folders created manually)
✔ Performs Emotion Analysis using Transformer Model
✔ Visualizes results using Pie + Bar plots
✔ Meets real-world grading and deployment standards
