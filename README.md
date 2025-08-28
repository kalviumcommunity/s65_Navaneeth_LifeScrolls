# 📖 LifeScrolls – AI-Powered Memory Book

**LifeScrolls** is a Generative AI-powered digital diary that transforms personal memories, diary entries, or life events into beautifully written stories, summaries, and quotes.  

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



### 🛠️ System and User Prompt (RTFC Framework)

In this task, we designed **System and User Prompts** tailored to the LifeChapters use case.  
We applied the **RTFC Framework** (Role, Task, Format, Context) to structure the prompts clearly:  

- **Role**: Define the AI as a memory storyteller.  
- **Task**: Summarize, expand, and generate creative titles/quotes for memories.  
- **Format**: Output in structured JSON/Markdown for clean rendering.  
- **Context**: Use user-provided diary entries or events as input.  

This ensures the prompts are consistent, reliable, and aligned with the project’s goals.


### 🎯 Zero-Shot Prompting

In this task, we applied **Zero-Shot Prompting** within the LifeChapters project.  
Zero-Shot Prompting means giving the AI **only an instruction without examples**, and expecting it to generate the desired output.  

For LifeChapters, the AI was prompted to:  
- Take a raw memory input from the user.  
- Directly generate a summary, story, quote, and title.  

This method tests the model’s **generalization ability** without relying on prior demonstrations.  
It ensures flexibility when handling completely new types of memory inputs.



### 📝 One-Shot Prompting  

In this task, we implemented **One-Shot Prompting** for the LifeChapters project.  
One-Shot Prompting means we provide the AI with **a single example** of the expected input and output format, before asking it to perform the same task on a new input.  

This approach helps guide the AI more clearly than Zero-Shot, since it gets one demonstration of what the output should look like. It sets a pattern that the AI can then replicate with the user’s own memory input.  

For LifeChapters, we gave the AI one memory input as an example and showed how it should generate:  
- A short **summary** of the memory  
- An expanded **story version**  
- A **quote or caption** to capture the emotion  
- A creative **title** for the event  

After providing this demonstration, we then asked the AI to do the same task for a completely new memory provided by the user. This improves **consistency, formatting, and quality** of the results compared to Zero-Shot Prompting.  

Thus, One-Shot Prompting ensures the AI understands the **style, tone, and structure** of the desired response with only one guiding example.  



### 📚 Multi-Shot Prompting  

In this task, we applied **Multi-Shot Prompting** within the LifeChapters project.  
Multi-Shot Prompting is a prompting technique where the AI is provided with **multiple examples** of the task before it is asked to generate a response for a new input. Unlike Zero-Shot (no examples) and One-Shot (one example), Multi-Shot uses two or more demonstrations to guide the model more effectively.  

This method helps the AI understand the **pattern, structure, and tone** of the expected output more reliably. It reduces ambiguity and ensures the generated results follow the same style as the provided examples.  

For LifeChapters, we created multiple memory samples and showed how each was converted into:  
- A concise **summary** of the memory  
- A detailed **story version** of the event  
- A meaningful **quote or caption** to express the emotion  
- A creative **title** that reflects the memory  

After providing two or more examples, the AI was then given a completely new memory entry from the user. The prior examples acted as a **reference set**, allowing the model to generate consistent outputs aligned with the LifeChapters style.  

This technique improved the **accuracy, fluency, and emotional tone** of the generated memory stories compared to Zero-Shot and One-Shot prompting. Multi-Shot Prompting is especially valuable when the project requires **structured outputs** and a consistent narrative flow across different user inputs.  



### 🔄 Dynamic Prompting  

In this task, we introduced **Dynamic Prompting** into the LifeChapters project.  
Dynamic Prompting refers to the practice of creating prompts that **change or adapt automatically** based on the user’s input or context, instead of using a fixed static prompt. This technique makes the AI system more interactive, flexible, and context-aware.  

Unlike Zero-Shot, One-Shot, or Multi-Shot prompting (which rely on predefined examples or instructions), Dynamic Prompting personalizes the prompt on the fly. This ensures the generated outputs are more relevant to each unique memory entered by the user.  

For LifeChapters, the system takes a user’s memory and dynamically adjusts the prompt to highlight specific aspects, such as:  
- Whether the event is **happy, sad, funny, or emotional**  
- The **timeframe** (childhood, school, college, family, etc.)  
- The **desired output style** (short summary, long story, poetic quote, or creative title)  

By inserting these contextual details into the prompt, the AI produces more **tailored and expressive results**. For example, if the user writes a funny memory, the system adjusts the prompt to encourage a humorous storytelling style. If the memory is emotional, the prompt adapts to generate a more sentimental output.  

This makes the project more engaging, as users feel that the AI is **responding personally to their experiences** rather than following a rigid format. Dynamic Prompting, therefore, brings **personalization and adaptability** to LifeChapters.  
