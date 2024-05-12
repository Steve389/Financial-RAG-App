# FinQBot: Financial Insights Generator :chart_with_upwards_trend: :mag_right:

Need a powerful LLM to cather to your specific needs and answer financial questions specific to your company?
Worried about data privacy issues related to the use of LLMs? __FinQBot__ is your answer!
Developed using open source technologies (Llama and LlamaIndex) __FinQBot__ offers unlimited power, accuracy and enhanced data security.

#### Technology used:
- Open source language model meta-llama/Llama-2-70b-chat-hf. This is the 70 billion parameter model optimized for dialogue use cases.
- Transformers API from HuggingFace. Transformers provides APIs and tools to easily download and train state-of-the-art pretrained models.
- Open source framework LlamaIndex. LlamaIndex is a framework for building context-augmented LLM applications.
- RunPod. This code was run in a GPU accelerated environment on RunPod. More specifically, I used a RTX-A6000 48 GB GPU.

#### Main Steps:
#### 1. Request grant access from Meta and get access token from HuggingFace
These steps are necessary if you want to access the Llama API.

#### 2. Instantiate the tokenizer and the model using the Transformers API
We need to instantiate a tokenizer before instantiating the model because the tokenizer is responsible for preprocessing 
the input text and tokenizing it into numerical representations that the model can understand.

#### 3. Test the model
<img width="965" alt="Screenshot 2024-05-12 at 8 01 50 PM" src="https://github.com/Steve389/Financial-RAG-App/assets/87010794/a362cee8-0b91-421e-a5e5-df76f46ee3b7">

#### 4. Create a Huggingface LLM instance for LlamaIndex
 The HuggingFaceLLM wrapper class abstracts away the complexities of integrating the model into the Llama index environment, 
 making it easier to use the model for retrieval-augmented generation tasks within the Llama index framework.

 #### 4. Create the embeddings for Retrieval Augmented Generation
 Embeddings play a crucial role in retrieval-augmented generation tasks by representing text documents or passages in a high-dimensional vector space.
 In retrieval-augmented generation, the model retrieves relevant passages or documents from a knowledge base using embeddings and then generates responses based on the retrieved information.

 #### 5. Load documents and create the Vector Store Index
 In this case, we're working with PDF files, so we need a PDF document loader capable of extracting text and metadata from PDF files (PyMuPDFReader).
 Once the documents are loaded, we create a vector store index from the loaded documents. A vector store index organizes documents by encoding them 
 into high-dimensional vector representations and storing them in a data structure optimized for efficient retrieval. 

  #### 6. Query the Vector Database in order to get the financial data of your company!

 <img width="1002" alt="Screenshot 2024-05-12 at 8 26 19 PM" src="https://github.com/Steve389/Financial-RAG-App/assets/87010794/fddb2e0d-4287-47c3-bc4a-d89fc208f38b">
