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


##🚀 How to Run the Chatbot
Run the Python script or Jupyter notebook:

bash
Copy
Edit
python clat_chatbot.py
The chatbot will run in a terminal/console interface:

text
Copy
Edit
📚 CLAT Chatbot (type 'exit' to quit)

👩‍⚖️ You: What’s the CLAT 2025 syllabus?
🤖 Chatbot: The CLAT 2025 syllabus includes English Language, Current Affairs...
📚 Sample Questions in the Knowledge Base
What is the syllabus for CLAT 2025?

How many questions are there in the English section?

What is the duration of the CLAT exam?

Give me last year’s cut-off for NLSIU Bangalore.

Is there any negative marking in CLAT?

What are the eligibility criteria for CLAT UG?

💡 Bonus: Future Scaling with GPT
To scale this system:

Use LangChain + OpenAI API with Retrieval-Augmented Generation (RAG)

Fine-tune a GPT-based model on NLTI-specific data (past year papers, mentor chats)

Use tools like Haystack or HuggingFace Transformers for production-ready QA systems

📈 Limitations
Works only with questions similar to those in the knowledge base.

Doesn’t use deep learning (good for lightweight prototypes).

Not trained on actual CLAT documents or historical data.


