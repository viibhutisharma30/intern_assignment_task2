# CLAT Exam Chatbot – Rule-Based & NLP Powered

A simple NLP-powered chatbot that answers common CLAT-related queries using a content-aware matching system.

This chatbot uses a small knowledge base of CLAT FAQs and responds to user queries by finding the most relevant answer based on text similarity (TF-IDF + Cosine Similarity).

---

## Problem Statement

Build a Python-based chatbot prototype that can respond to legal exam queries such as:

- "What is the syllabus for CLAT 2025?"
- "How many questions are there in the English section?"
- "Give me last year’s cut-off for NLSIU Bangalore."

---

## Summary of the Approach

1. Created a **mock knowledge base** of commonly asked CLAT-related questions and answers.
2. Used **TF-IDF Vectorization** to convert questions into vectors.
3. When a user types a question:
   - It is transformed into a vector.
   - **Cosine similarity** is calculated with all known questions.
   - The most similar question's answer is returned.
4. A **confidence threshold** ensures unrelated queries return a fallback response.
5. Optional: Preprocessing and intent detection with **spaCy** (loaded but not deeply used to keep it light).

---

## Setup Instructions

### Clone or Download

```bash
git clone https://github.com/yourusername/clat-chatbot.git
cd clat-chatbot
```
---
## How to Run the Chatbot
Run the Python script or Jupyter notebook:

```bash
python clat_chatbot.py
```
The chatbot will run in a terminal/console interface:
```bash
📚 CLAT Chatbot (type 'exit' to quit)

👩‍⚖️ You: What’s the CLAT 2025 syllabus?
🤖 Chatbot: The CLAT 2025 syllabus includes English Language, Current Affairs...
```

## Bonus: Future Scaling with GPT
To scale this system:

1.Use LangChain + OpenAI API with Retrieval-Augmented Generation (RAG)
2.Fine-tune a GPT-based model on NLTI-specific data (past year papers, mentor chats)
3.Use tools like Haystack or HuggingFace Transformers for production-ready QA systems

---

## Limitations

1.Works only with questions similar to those in the knowledge base.
2.Doesn’t use deep learning (good for lightweight prototypes).
3.Not trained on actual CLAT documents or historical data.



