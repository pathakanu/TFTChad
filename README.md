How does it work?

1. Upload any file(s) or enter any path or url
2. The data source is detected and loaded into text documents
3. The text documents are embedded using openai embeddings
4. The embeddings are stored as a vector dataset to activeloop's database hub
5. A langchain is created consisting of a LLM model (gpt-3.5-turbo by default) and the vector store as retriever
6. When asking questions to the app, the chain embeds the input prompt and does a similarity search of in the vector store and uses the best results as context for the LLM to generate an appropriate response
7. Finally the chat history is cached locally to enable a ChatGPT like Q&A conversation
