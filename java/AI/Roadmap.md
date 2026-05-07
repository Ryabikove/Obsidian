It is system focused path. It teaches how to use and integrate AI into projects, but there is no information about how it creates.

It starts on 04.05.2026.

**Month 1 - conceptual practice:**
- Concept - understanding transformers, tokenization and **context windows**;
- Practice - learning **prompt engineering** - not just for chat, but for structured outputs like JSON or Java Objects;
- Goal - create a simple spring boot service, that calls an LLM API using standart REST client;

**Month 2 - mastering the frameworks (Spring AI and LangChain4j):**
- Spring AI - learning spring boot for AI philosophy, which allows to swap models providers without changing code;
- LangChain4j - the most popular Java alternative to the Python LangChain. Focus on its low-level abstraction for models and prompts;
- Goal - build a "Translator Service" that takes text and returns a specific Java DTO


**Month 3 - data and memory (the RAG pattern):**
- Embedding - learning how to turn text into lists of numbers;
- Vector Databases - practicing with pgvector or Chroma/Pinecone;
- Goal - build a service that "ingests" PDF documents, stores them in a vector DB and allows the AI to answer questions based only on thoose files;

**Month 4 - Agent and Orchestration:**
- Function calling - learning how to give the AI access to your Java methods;
- Stateful chains - using tools like LangGraph to build multi-step workflows;
- Goal - create an AI Agent that can browse your local database and send automated email summaries basaed on its findings;

**Month 5 - Production and the Capstone project:**
- Observability - use tools like LangSmith to monitor costs and "hallucinations";
- System design - learn about rate limiting for AI APIs and Caching stategies;
- Final project - build smart enterprise search for spring boot app that searches both relational data and unstructured documentation;