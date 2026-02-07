# Document-Analysis-Using-LLMs-with-Python


This repository demonstrates a document analysis pipeline using Python and Large Language Models (LLMs). The workflow automates extraction, summarization, question generation, and question answering from unstructured PDF documents.

## Pipeline Overview

### Step 1: Extract Text from the PDF

Convert PDFs into raw text for processing.

Tools: PyPDF2, pdfplumber, Tika, or OCR for scanned PDFs.

### Step 2: Preview the Extracted Text

Validate text extraction quality and detect any OCR errors.

Quick checks ensure clean data before further processing.

### Step 3: Summarize the Document

Generate a concise summary of the document’s content.

Tools: LLMs like OpenAI GPT, Anthropic Claude, or Hugging Face models.

### Step 4: Split the Document into Sentences and Passages

Break long documents into chunks or passages to improve LLM context handling.

Each chunk can later be analyzed or queried independently.

### Step 5: Generate Questions from the Passages Using LLMs

Automatically generate relevant questions from each passage.

Prompts can simulate expert reasoning to identify key information.

### Step 6: Answer the Generated Questions Using a QA Model

Use LLMs to answer questions based on extracted passages (RAG: Retrieval-Augmented Generation).

Produces structured answers suitable for dashboards, chatbots, or automated workflows.

# Real-World Case Study: Condé Nast Contract Analysis

Condé Nast, a major media company in the Amazon ecosystem, implemented a document analysis system for contract review using Amazon Bedrock LLMs. (AWS Case Study
)

## Business Challenge

Manual review of hundreds of contracts (content licenses, publishing rights) was slow and error-prone.

Needed fast extraction of key clauses, dates, rights, and obligations to accelerate editorial decisions.

| Step               | Implementation at Condé Nast                              | AWS Services / LLM                 |
| ------------------ | --------------------------------------------------------- | ---------------------------------- |
| Extract Text       | Convert PDFs into structured text                         | Amazon Bedrock (Claude 3.7 Sonnet) |
| Preview / Validate | Automated validation and human spot-checks                | Amazon Comprehend, S3              |
| Summarize          | Generate concise summaries of contract terms              | Amazon Bedrock LLM                 |
| Split              | Break long contracts into passages for context            | Custom chunking logic              |
| Generate Questions | Identify important queries (e.g., exclusivity, royalties) | Amazon Bedrock LLM                 |
| Answer Questions   | Retrieve context-aware answers for each question          | RAG + Amazon Bedrock LLM           |

### Business Impact

Contract analysis time reduced from weeks → minutes

Legal and editorial teams focus on decision-making, not reading PDFs

Faster capture of licensing opportunities

Significant operational efficiency improvement

### Key Takeaways

LLMs can automate document-heavy workflows across industries: healthcare, finance, legal, media, and enterprise knowledge management.

The 6-step pipeline (extract → preview → summarize → split → question → answer) forms a foundation for RAG-based document intelligence systems.

AWS Bedrock allows organizations to deploy enterprise-grade LLMs (Claude, Titan, LLaMA) in production workflows with measurable ROI.

### References

https://amanxai.com/2024/10/21/document-analysis-using-llms-with-python/
https://aws.amazon.com/blogs/machine-learning/how-conde-nast-accelerated-contract-processing-and-rights-analysis-with-amazon-bedrock/?utm_source=chatgpt.com
