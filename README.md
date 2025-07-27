# Chatbot com Vetorização de Documentos e memória.

Este projeto implementa um chatbot inteligente que responde perguntas com base em documentos enviados pelo usuário. Ele usa recebe arquivos de diversos tipos, realiza o chunking do texto extraído, faz o embedding dos fragmentos e envia para um banco de dados postgres já configurado para receber valores de tipo "vetor". Em seguida o usuário fará uma pergunta ao chatbot, caso haja proximidade dos vetores entre a pergunta realizada e as sentenças do banco de dados, o bot retorna uma mensagem enriquecida por IA sobre as sentenças identificadas, caso não encontre, o bot deixa claro sua incapacidade de encontrar o tema sugerido. Toda a conversa é armazenada dentro de outra tabela no Postgres, para garantir que sempre que o usuário abrir a aplicação, o histórico estará presente, mesmo que o sistema seja reiniciado.

---

## Tecnologias Utilizadas

- Python 3.9+
- [FastAPI](https://fastapi.tiangolo.com/)
- [LangChain](https://www.langchain.com/)
- [OpenAI API](https://platform.openai.com/)
- [pgvector (extensão PostgreSQL)](https://github.com/pgvector/pgvector)
- [Unstructured](https://github.com/Unstructured-IO/unstructured)
- [NLTK](https://www.nltk.org/)
- [Uvicorn](https://www.uvicorn.org/)
- [Jupyter Notebook](https://jupyter.org/)

---

## 📂 Funcionalidades

- Upload de arquivos (PDF, DOCX, etc.)
- Extração e limpeza de texto
- Decomposição de sentenças complexas em proposições simples
- Vetorização com `OpenAI Embeddings`
- Armazenamento de vetores e histórico de conversa no PostgreSQL
- Chat com busca por similaridade vetorial
- API FastAPI dentro do próprio notebook

---
