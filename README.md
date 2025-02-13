# Tabular QA System

A Tabular QA system for accurate data retrieval, processing, and automated answer generation, supporting multi-table querying.

## Features
- Query large and complex tables efficiently
- Multi-table querying support
- Automated answer generation from tabular data
- Handles contextual ambiguity and large datasets
- Integrates with OpenAI for NLP processing
- Uses Pinecone for efficient vector-based search

## Installation

```bash
# Clone the repository
git clone <your-repo-url>
cd <your-repo-folder>

# Install dependencies
pip install -r requirements.txt
```

## API Keys Setup
This project requires API keys for OpenAI and Pinecone.

```bash
export OPENAI_API_KEY="your-openai-api-key"
export PINECONE_API_KEY="your-pinecone-api-key"
```

## Usage

### Start the API Server
```bash
python main.py
```

### API Endpoints

#### 1. Query Data
**Endpoint:** `POST /query`

**Description:** Process a user query and return the answer from the tabular data.

**Request:**
```json
{
  "question": "What is the total revenue?"
}
```

**Response:**
```json
{
  "answer": "$1,234,567",
  "relevant_rows": [3, 7, 15],
  "relevant_columns": ["Revenue"]
}
```

#### 2. Upload Table
**Endpoint:** `POST /upload`

**Description:** Upload a new table for processing.

**Request:**
- `multipart/form-data` with CSV/XLSX file

**Response:**
```json
{
  "message": "Table uploaded successfully",
  "table_id": "12345"
}
```

## Contributing
Feel free to contribute by submitting issues or pull requests.

## License
This project is licensed under the MIT License.
