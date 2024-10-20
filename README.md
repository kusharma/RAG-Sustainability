# RAG with LangChain: Streamlining Sustainability Reporting

## Overview
This project demonstrates the use of **LangChain**, **OpenAI**, and **ChromaDB** to streamline sustainability reporting workflows. The focus is on extracting, processing, and generating insights from dense sustainability reports such as those from **SwissRe** and **BlackRock**. By leveraging **Retrieval-Augmented Generation (RAG)** and advanced query techniques, this project enhances the efficiency of handling large sustainability reports and providing clear, actionable insights.

## Features
- **PDF Extraction with PyMuPDF**: Efficiently extract text from sustainability reports in PDF format.
- **Text Splitting**: The project uses **RecursiveCharacterTextSplitter** to ensure extracted text is split into coherent chunks for better processing.
- **Embeddings and Vector Store**: The extracted chunks are embedded using **OpenAI's embeddings**, and **ChromaDB** is used to store and retrieve these embeddings during query processing.
- **Query Transformation**: **LangChain** transforms user questions into optimal queries by utilizing techniques like query decomposition and multiple query generation, ensuring accurate and relevant answers.
- **LCEL (LangChain Expression Language)**: This enables seamless query conversion into structured formats, making it easier to work with different databases in the future (SQL, GraphDB).

## Technical Stack
- **LangChain**: Provides the framework for agent-based query management and RAG workflows.
- **OpenAI**: Used for text embedding, facilitating semantic understanding and retrieval.
- **ChromaDB**: A vector store used for storing document embeddings and supporting efficient query retrieval.
- **PyMuPDF**: Used for extracting text from PDFs of sustainability reports.

## Query Transformation Techniques

Query transformations are a set of approaches focused on re-writing and/or modifying questions for retrieval.

| Technique      | Purpose/Objective                                     | Potential Examples                                                |
|----------------|-------------------------------------------------------|-------------------------------------------------------------------|
| Multi-query    | Retrieve data from various sections                   | CO2 reduction targets, ESG metrics                                |
| RAG-Fusion     | Combine data from different sources                   | Climate-risk metrics with performance indicators, Underwriting + Investment data |
| Decomposition  | Break down complex topics into sub-queries            | Carbon reduction strategies, Climate-related disclosures           |
| Step-back      | Evaluate alignment with external standards            | Sustainability governance, ESG risk management                     |
| HyDE           | Generate hypothetical future projections              | GHG emission reduction predictions, Impact of new policies on targets |
