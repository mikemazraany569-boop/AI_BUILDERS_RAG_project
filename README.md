# 🏢 Organizational Behavior Course Assistant (RAG Pipeline)

An interactive, locally deployed **Retrieval-Augmented Generation (RAG)** academic assistant designed specifically for an **Organizational Behavior (OB)** course. Powered by **FAISS** vector indexing and a **Gradio** web interface, this assistant delivers precise, grounded answers to complex OB topics—from leadership frameworks and motivation theories to team dynamics and organizational culture—complete with strict hallucination guardrails and source citations.
The Organizational Behavior pdf is a course I took when I studied Data Science at the university.
---

## 🌟 Key Features

* **Context-Grounded Q&A:** Answers questions using course notes, textbooks, and case studies to prevent hallucinations and out-of-scope responses.
* **Source & Metadata Transparency:** Displays exact retrieved source passages, course module citations, and relevance scores alongside every response.
* **Fast Vector Retrieval:** Powered by **FAISS (Facebook AI Similarity Search)** for instant similarity matching over dense embedding vectors.
* **Local & Secure:** Ingests and processes course materials locally to keep study data private.
* **Interactive UI:** A clean **Gradio** dashboard supporting streaming responses, query history, and context inspection.

---

## 🏗️ System Architecture

  [ User Query ] ──► (e.g., "Compare Herzberg's two-factor theory vs. Maslow's hierarchy")
        │
        ▼
  [ Text Embedder ] ──► Vector Representation
                             │
                             ▼
  [ OB Knowledge Base ] ──► [ FAISS Vector Store ]
  (PDFs / Notes / Cases)         │
                                 ▼
                      [ Top-K Source Passages ]
                                 │
                                 ▼
                  [ LLM Generator + Guardrails ]
                                 │
                                 ▼
                     [ Gradio Web Interface ]


