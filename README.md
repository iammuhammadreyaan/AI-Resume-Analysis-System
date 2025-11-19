# AI-Resume-Analysis-System
A fully automated AI Resume Analysis System that processes incoming resumes, analyzes them using an AI recruiter agent, and stores structured results in Google Sheets.

🚀 AI Résumé Analysis System (n8n Automation)

A fully automated résumé screening pipeline built in n8n.
This workflow receives incoming résumés, extracts their content, analyzes them using an AI Recruiter Agent, and stores the structured results in Google Sheets.

📌 Features

✔️ Automatically processes résumés received via Gmail

✔️ Supports PDF, DOCX, and TXT files

✔️ Extracts text using format-specific methods

✔️ Standardizes the résumé for consistent AI input

✔️ Uses a Recruiter AI Agent for evaluation

✔️ Generates a structured summary (skills, score, strengths, etc.)

✔️ Saves output into Google Sheets

✔️ Zero manual input required — fully automated

🧩 Workflow Overview:

Gmail Trigger  
      ↓  
Upload to Google Drive  
      ↓  
Switch (File Type Detection)  
      ├── PDF → Extract → Standardize  
      ├── DOCX → Extract → Standardize  
      └── TXT → Extract → Standardize  
      ↓  
AI Recruiter Agent  
      ↓  
Information Extractor  
      ↓  
Append to Google Sheets


⚙️ Node-by-Node Explanation
1. Gmail Trigger

Starts the workflow whenever a new email arrives with a résumé attachment.


2. Google Drive Upload

Stores the file in Drive for secure access and processing.


3. Switch Node (File Type Detection)

Routes the workflow based on the file extension:

.pdf

.docx

.txt


4. Extract Nodes

PDF → PDF Extract

DOCX → Document Extract

TXT → Text Extract

Extracts clean résumé text for analysis.


5. Standardization Node

Normalizes extracted text to ensure the AI receives consistent, readable input.


6. Recruiter Agent (AI Model)

Analyzes:

Skills

Work experience

Education

Strengths and weaknesses

Candidate score

Summary of findings


7. Information Extractor

Structures the AI output into clean JSON.


8. Google Sheets Append

Stores:

Candidate details

Skill tags

Rating / score

Summary

AI remarks
