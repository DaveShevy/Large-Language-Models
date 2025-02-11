# LLM Qualitative Analysis Pipeline

## Overview
This project leverages **LLMs (Large Language Models)** to extract qualitative insights from textual survey data. It automates key theme extraction, sentiment analysis, and PII redaction using **Azure OpenAI, Azure Text Analytics, and BERT models**. The processed data can be used for business intelligence, reporting, and decision-making.

## Features
- **Key Theme Extraction**: Uses LLMs to identify major themes from textual feedback.
- **Sentiment Analysis**: Combines Azure and BERT-based sentiment analysis for accuracy.
- **PII Redaction**: Uses Azure Text Analytics to detect and redact personally identifiable information (PII).
- **Text Clustering & Embeddings**: Implements TF-IDF, PCA, and K-Means clustering.
- **Cost & Performance Optimization**: Monitors token usage and API costs.

## Data Processing Pipeline
1. **Data Ingestion**: Loads survey comments from an Excel file.
2. **PII Redaction**: Redacts sensitive information before LLM processing.
3. **Key Theme Extraction**:
   - Prompts Azure OpenAI API to extract 1-3 key themes per comment.
   - Outputs themes as structured metadata.
4. **Sentiment Analysis**:
   - Uses Azure Text Analytics for sentiment classification.
   - Cross-validates with BERT sentiment model.
5. **Text Clustering & Similarity Analysis**:
   - Applies TF-IDF and PCA for dimensionality reduction.
   - Groups comments into thematic clusters using K-Means.

## Setup & Requirements
### Prerequisites
- Python (>= 3.8)
- Azure OpenAI & Text Analytics API keys
- Required Python packages:
  ```sh
  pip install pandas openai azure-ai-textanalytics scikit-learn transformers torch dotenv rouge-score
  ```

### Environment Variables
Set up API credentials in a `.env` file:
```sh
AZURE_OPENAI_API_KEY=your_api_key
AZURE_OPENAI_ENDPOINT=your_endpoint
AZURE_OPENAI_DEPLOYMENT_NAME=your_deployment
AZURE_LANGUAGE_API_KEY=your_language_api_key
AZURE_LANGUAGE_ENDPOINT=your_language_endpoint
```

### Running the Notebook
1. Load survey data from the specified Excel file.
2. Authenticate Azure and initialize NLP pipelines.
3. Execute key theme extraction and sentiment analysis.
4. Review and export structured insights for reporting.

## Future Enhancements
- Improve theme extraction accuracy using fine-tuned models.
- Integrate with Power BI for real-time visualization.
- Implement real-time API calls for streaming analysis.

## Contact
For questions or contributions, please reach out to the repository owner.