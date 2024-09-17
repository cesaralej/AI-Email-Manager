# AI-Powered Email Processing for Fashion Store Orders and Inquiries

## Overview

This project is a proof-of-concept application designed to automate the processing of customer emails for a fashion store. The system intelligently categorizes emails as either **product inquiries** or **order requests**, processes order requests by checking stock availability, and generates professional responses. The project leverages advanced AI techniques, including **Large Language Models (LLMs)**, **Retrieval-Augmented Generation (RAG)**, and **vector stores** to handle customer queries based on real-time product catalog data.

## Key Features

- **Email Classification**: Automatically classifies emails into either _product inquiries_ or _order requests_ using GPT-4's natural language understanding capabilities.
- **Order Processing**: Extracts product and quantity information from order request emails, checks stock levels, and updates order status (created or out of stock).
- **Dynamic Product Inquiry Responses**: Handles customer product inquiries using **RAG** techniques, ensuring that responses are tailored based on real-time product catalog data without exceeding LLM token limits.
- **Automated Stock Management**: Adjusts product stock levels based on successfully processed orders and suggests alternatives if products are out of stock.
- **Professional Tone Adaptation**: Ensures all email responses are generated with a professional, customer-friendly tone, improving user experience and engagement.

## Project Skills Demonstrated

### 1. **Natural Language Processing (NLP)**
   - Deployed **LLM-based classification** to distinguish between customer inquiries and orders.
   - Utilized **prompt engineering** for extracting structured data from unstructured email content, such as product names and quantities.
   - Handled open-ended customer inquiries by generating responses based on product catalog data, using scalable approaches.

### 2. **Retrieval-Augmented Generation (RAG)**
   - Implemented **RAG** for customer product inquiries, using a vector database to retrieve relevant product information from a large catalog.
   - Integrated **FAISS** or similar vector stores to index product details and optimize retrieval based on customer requests.

### 3. **Workflow Automation**
   - Automated **order processing workflows** by chaining together multiple steps (email classification, stock verification, response generation) using **Langchain Sequential Chains**.
   - Designed a system capable of processing emails efficiently at scale, ensuring high accuracy in order management and product inquiry handling.

### 4. **Data Handling and Integration**
   - Integrated data from **Google Sheets** (product catalog and email list) into the application, using Python’s `gspread` library to update sheets with results (classified emails, order statuses, and generated responses).
   - Managed real-time product inventory updates, ensuring that stock levels are dynamically adjusted after order processing.

## Technical Stack

- **Python**: Core programming language used for building the system.
- **OpenAI GPT-4**: Advanced LLM used for natural language understanding, classification, and response generation.
- **Langchain**: Deployed for chaining multiple tasks, managing workflows, and integrating **LLMs** with external knowledge sources.
- **Hugging Face**: For loading a pre-trained embedding model and using it to create vectors out of documents.
- **Chroma**: Vector database used for indexing and retrieving product information efficiently.
- **Google Sheets API**: Used for seamless integration with product catalog and email data, allowing automated updates.
- **gspread**: Library for automating Google Sheets interactions and storing processed results.
