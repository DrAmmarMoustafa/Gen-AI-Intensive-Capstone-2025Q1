

The Challenge: Traditional medicinal knowledge, a cornerstone of cultural heritage and potential source for modern health solutions, is often locked in unstructured formats or oral traditions. Data collected on 257 Mediterranean_Plants represents such invaluable knowledge, but its accessibility and analytical potential are limited in raw form. This risks knowledge loss and hinders alignment with the WHO's goal of integrating traditional medicine effectively.
Our Solution: EthnoMed leverages cutting-edge Generative AI to transform this dataset into a dynamic, interactive knowledge base. We build an AI-powered Advisor that allows users to query, analyze, and understand Mediterranean_Plants in a structured and grounded manner.

Importance: This project contributes to:

    Cultural Heritage Preservation:** Digitizing and organizing vital traditional knowledge.
    WHO Strategy Alignment:** Supporting the goals of the Traditional Medicine Strategy (2025–2034).
    Knowledge Discovery:** Making complex ethnobotanical data searchable and analyzable.
    Advanced AI Demonstration:** Showcasing RAG, AI Agents, and Prompt Engineering with Gemini.

2. 💎 Methodology & AI Capabilities

We employ a sophisticated AI architecture:

    RAG System (Retrieval-Augmented Generation):
        Embedding: Plant data is converted into semantic vectors using models/embedding-001.
        Indexing: These vectors are stored locally and persistently (within this Kaggle session) using ChromaDB in /kaggle/working/.
        Retrieval: User queries are embedded, and ChromaDB finds the most relevant plant data via vector similarity search.
        Generation: The Gemini 2.0 Flash model (implemented via gemini-1.5-flash-latest) generates answers only based on the retrieved, relevant context, ensuring factual grounding.

    AI Agents (Task-Specific Functions):
        Q&A Agent: Uses the RAG pipeline to answer natural language questions.
        Extraction Agent: Parses unstructured 'Folk Uses' text into structured JSON (ailments, actions, categories).
        Generation Agent: Creates summaries and informational usage descriptions (with disclaimers) for specific plants.

    Prompt Engineering (Command Engineering):
        Each AI Agent relies on carefully crafted prompts. These instructions guide the Gemini model, define expected output formats (e.g., JSON), enforce constraints (e.g., using only retrieved context, adding disclaimers), and optimize for accuracy and relevance using the target gemini-1.5-flash-latest capabilities

