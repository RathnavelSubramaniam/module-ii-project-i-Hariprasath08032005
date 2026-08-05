# 🩺 Medical Diagnosis Chatbot using Retrieval-Augmented Generation (RAG) and Llama-2

## 📌 Project Overview

This project implements an **AI-powered Medical Diagnosis Chatbot** using **Retrieval-Augmented Generation (RAG)** and the **Llama-2-13B Chat** Large Language Model. The chatbot answers medical questions by retrieving relevant information from a medical reference document (Merck Manual) and generating context-aware responses.

Unlike traditional LLM-based chatbots, this project does **not** use the OpenAI API. Instead, it runs a **locally hosted Llama-2 GGUF model** using **llama-cpp-python** and **Hugging Face Embeddings**, making it completely open-source and offline after downloading the model.

---

# 🚀 Features

- Medical Question Answering
- Retrieval-Augmented Generation (RAG)
- Llama-2-13B Chat GGUF Model
- Hugging Face Sentence Transformer Embeddings
- FAISS Vector Database
- PDF Document Processing
- Prompt Engineering
- Fully Offline (No OpenAI API)
- Google Colab Compatible

---

# 🎯 Objectives

- Build a Medical AI Assistant.
- Compare LLM and RAG approaches.
- Improve response accuracy using document retrieval.
- Reduce hallucinations in medical question answering.
- Eliminate dependency on paid APIs.

---

# 📚 Dataset

**Medical Reference**

- Merck Manual of Diagnosis & Therapy (PDF)

The document contains:

- Diseases
- Symptoms
- Diagnosis
- Treatments
- Medications
- Prevention
- Clinical Guidelines

---

# 🏗️ Project Architecture

```
                 Medical PDF
                      │
                      ▼
               PDF Loader
                      │
                      ▼
              Text Chunking
                      │
                      ▼
        Hugging Face Embeddings
                      │
                      ▼
            FAISS Vector Database
                      │
                      ▼
                 Retriever
                      │
                      ▼
              Prompt Engineering
                      │
                      ▼
            Llama-2 13B Chat Model
                      │
                      ▼
               Generated Response
```

---

# 🔄 Workflow

```
Medical PDF
      │
      ▼
Load Document
      │
      ▼
Split into Chunks
      │
      ▼
Generate Embeddings
      │
      ▼
Store in FAISS
      │
      ▼
User Question
      │
      ▼
Retrieve Relevant Chunks
      │
      ▼
Prompt Engineering
      │
      ▼
Llama-2
      │
      ▼
Medical Response
```

---

# 🛠️ Technologies Used

## Programming Language

- Python

## Frameworks

- LangChain

## LLM

- Llama-2-13B Chat GGUF

## Embedding Model

- sentence-transformers/all-MiniLM-L6-v2

## Vector Database

- FAISS

## Libraries

- llama-cpp-python
- huggingface_hub
- langchain
- langchain-community
- langchain-huggingface
- sentence-transformers
- transformers
- faiss-cpu
- pandas
- pypdf

---

# 📂 Project Structure

```
Medical-Diagnosis-RAG/
│
├── Medical_Diagnosis_RAG.ipynb
├── medical_reference.pdf
├── requirements.txt
├── README.md
└── images/
```

---

# ⚙️ Installation

## Clone Repository

```bash
git clone https://github.com/yourusername/Medical-Diagnosis-RAG.git

cd Medical-Diagnosis-RAG
```

---

## Install Dependencies

```bash
pip install -U llama-cpp-python
pip install -U langchain
pip install -U langchain-community
pip install -U langchain-huggingface
pip install -U sentence-transformers
pip install -U transformers
pip install -U huggingface_hub
pip install -U faiss-cpu
pip install -U pypdf
```

---

# 📥 Download Llama-2 Model

```python
from huggingface_hub import hf_hub_download

model_name = "TheBloke/Llama-2-13B-chat-GGUF"

model_file = "llama-2-13b-chat.Q5_K_M.gguf"

model_path = hf_hub_download(
    repo_id=model_name,
    filename=model_file
)
```

---

# ▶️ Run the Project

1. Install dependencies.
2. Download the Llama-2 GGUF model.
3. Upload the medical PDF.
4. Generate embeddings.
5. Create the FAISS vector database.
6. Ask medical questions.

---

# 📊 Two Approaches

## 1️⃣ LLM Approach

- Prompt Engineering
- Direct response generation
- Uses only the Llama-2 model

### Workflow

```
Question
    │
    ▼
Prompt
    │
    ▼
Llama-2
    │
    ▼
Response
```

---

## 2️⃣ RAG Approach

- PDF Retrieval
- Embeddings
- FAISS
- Context-based Answer

### Workflow

```
Question
     │
     ▼
Retriever
     │
     ▼
Relevant Chunks
     │
     ▼
Llama-2
     │
     ▼
Answer
```

---

# 📈 Results

The project compares:

- LLM Response
- RAG Response

The RAG approach produces:

- Higher Accuracy
- Context-aware Answers
- Reduced Hallucination
- Better Reliability

---

# ✅ Advantages

- No OpenAI API required
- Completely Offline
- Open Source
- Fast Semantic Search
- Accurate Medical Responses
- Easily Extendable
- Cost Effective

---

# ⚠️ Limitations

- Requires initial model download.
- Response quality depends on the uploaded medical document.
- Large models require sufficient RAM and GPU resources.

---

# 🔮 Future Enhancements

- Streamlit Web Application
- Voice-based Medical Assistant
- Multi-PDF Knowledge Base
- Medical Image Analysis
- Multi-language Support
- Hospital Information System Integration
- Fine-tuned Medical LLM

---

# 📸 Sample Output

**Question**

```
What are the symptoms of diabetes?
```

**Answer**

```
Common symptoms of diabetes include frequent urination,
increased thirst, fatigue, blurred vision,
and unexplained weight loss.
```

---

# 📖 References

- Merck Manual of Diagnosis & Therapy
- Hugging Face
- LangChain
- FAISS
- llama-cpp-python
- Sentence Transformers

---

# 👨‍💻 Author

**Hari Prasath**

B.E. Computer Science and Engineering

R.V.S. College of Engineering

---

# ⭐ If you found this project useful

Please ⭐ Star this repository and share it with others.