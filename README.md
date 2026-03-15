# Peblo AI Backend Engineer Challenge
Mini Content Ingestion + Adaptive Quiz Engine

Author: Vuskamalla Vyshnavi

## Project Overview
This project demonstrates a prototype backend system that ingests educational PDF content, extracts structured text, generates quiz questions using an AI model, and serves quizzes through API endpoints.

The system also adapts quiz difficulty based on student performance.

## System Architecture
PDF Input
↓
Content Extraction
↓
Text Chunking
↓
AI Quiz Generation
↓
Database Storage
↓
Quiz API
↓
Student Answer Submission
↓
Adaptive Difficulty Adjustment

## Technology Stack
Backend Framework: Python + FastAPI  
Database: SQLite  
PDF Processing: pdfplumber  
AI Model: Large Language Model API  
API Testing: Swagger UI / Postman  

## Features
- PDF content ingestion
- Text extraction and cleaning
- Content chunking
- AI-generated quiz questions
- Adaptive difficulty mechanism
- REST API endpoints

## API Endpoints
POST /ingest  
Processes a PDF file and extracts content chunks.

POST /generate-quiz  
Generates quiz questions from stored content chunks.

GET /quiz  
Retrieves quiz questions filtered by topic or difficulty.

POST /submit-answer  
Stores student answers and evaluates correctness.

## Example Content Chunk
{
 "source_id": "SRC_001",
 "chunk_id": "SRC_001_CH_01",
 "grade": 1,
 "subject": "Math",
 "topic": "Shapes",
 "text": "A triangle has three sides and three angles."
}

## Example Question
{
 "question": "How many sides does a triangle have?",
 "type": "MCQ",
 "options": ["2","3","4","5"],
 "answer": "3",
 "difficulty": "easy"
}

## Conclusion
This project demonstrates how AI can transform educational content into interactive quizzes using a structured backend pipeline.
