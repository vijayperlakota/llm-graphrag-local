# llm-graphrag-local

### NOTE: ignore the peotry setup

This project is done by following the demo of https://www.youtube.com/watch?v=BLyGDTNdad0

- Uses https://microsoft.github.io/graphrag/ which is efficient than common RAG
- Commands to run
  - To index the data
    - python -m graphrag.index --init --root .
  - To query the data
    - python -m graphrag.query --root . --method global "what are the top themes in this story"
- Used Mahabarata summray data

NOTE: It took lot of time to index the input text given in the input folder

- Setup
  - In setup.yaml make sure that base url and embeddings models are correctly configured for local
  - Used LMStudio to run the Open AI compatible embeddings api
  - Used ollama gemma2 model
