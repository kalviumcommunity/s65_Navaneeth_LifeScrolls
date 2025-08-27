# 📖 LifeChapters – AI-Powered Memory Book

**LifeChapters** is a Generative AI-powered digital diary that transforms personal memories, diary entries, or life events into beautifully written stories, summaries, and quotes.  

It works like a **memory capsule** – preserving special life moments in a narrative form. Users can input text about an event (e.g., a trip, birthday, or achievement), and the AI will:  

- Summarize it concisely  
- Generate a story-like narrative  
- Suggest emotional quotes or captions  
- Create creative event titles  
- Export everything into a structured **Memory Book (PDF/HTML)**  

---

## ✨ Features

### 🔹 Core AI Features
- **Memory Summarization** → turns raw user text into short summaries.  
- **Story Generation** → expands small notes into longer narratives.  
- **Quote/Caption Generator** → produces captions for photos or highlights.  
- **Title Suggestions** → generates creative titles for events.  

### 🔹 Prompt Engineering & LLM Features
- **Zero-shot prompting** → direct story generation without examples.  
- **One-shot / Multi-shot prompting** → guide AI with sample inputs.  
- **Dynamic prompting** → adjust tone (emotional, funny, formal).  
- **Chain-of-Thought prompting** → AI explains reasoning step by step.  
- **Structured outputs** → outputs in JSON/Markdown for clean PDF/HTML export.  
- **Stop Sequences, Temperature, Top-P, Top-K** → control style and creativity.  

### 🔹 Embeddings & Retrieval
- **Embeddings** → memories stored as vectors for semantic search.  
- **Vector Database** → store and retrieve memories (FAISS / Chroma).  
- **Similarity Metrics** → Cosine, Euclidean, Dot Product comparisons.  

### 🔹 Export & UI Features
- **Export to PDF/HTML** → create a memory book or capsule.  
- **Optional Image Captions** → generate visuals with free text-to-image models.  
- **Search Past Memories** → semantic search with embeddings.  

---

## ⚙️ Technical Stack

- **Backend**: Node.js / Python (for AI processing)  
- **Models**: Open-source Hugging Face models  
  - `t5-small`, `bart`, or `distilGPT-2` for text generation/summarization  
  - `sentence-transformers/all-MiniLM-L6-v2` for embeddings  
- **Vector DB**: FAISS or Chroma (for semantic search)  
- **Frontend (Optional)**: React for diary-like UI  
- **Output**: Export memory book as PDF/HTML  

---

## 📌 Example Workflow

### User Input
```text
We went to Goa last December, enjoyed the beach, did parasailing, and celebrated Christmas together.


AI Output

Summary:
A Christmas getaway in Goa filled with adventure and joy.

Story:
In December 2023, our family embarked on a memorable trip to Goa. Between parasailing above the waves and Christmas celebrations on the beach, it became a chapter of laughter, togetherness, and sunshine.

Quote:
“The ocean keeps our laughter safe in its waves.”

Title:
Waves of December

