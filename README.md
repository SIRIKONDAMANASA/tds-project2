## Core Capabilities

### Smart Question Analysis
- Smart detection of query type (direct answer vs code execution needed)
- Contextual understanding and processing
## Getting Started

### System Requirements
- Python 3.8 or newer
- FastAPI framework
- scikit-learn library
- python-dotenv

### Setup Instructions

1. Get the code:
```bash
git clone https://github.com/SIRIKONDAMANASA/tds-project2.git
cd tds-project2
```

3. Configure environment variables:
```
GITHUB_API_KEY=your_api_token_here
VERCEL_API_KEY=your_api_token_here
```

4. Run the application:
```bash
uv run app.py
```

## API Usage

### Endpoint: `/api`

**Method**: POST

**Parameters**:
- `question` (required): The question to answer
- `file` (optional): A file to upload (ZIP or CSV)

### Example Request

```bash
curl -X POST "http://localhost:8000/api/" \
  -H "Content-Type: multipart/form-data" \
  -F "question=What is the output of pd.read_csv('data.csv').head()?" \
  -F "file=@data.csv"
```

## Error Handling

The API returns detailed error messages when:
- Code execution fails
- The LLM API returns an error
- File processing encounters issues

## Contributing

1. Fork the repository
2. Create a feature branch: `git checkout -b feature-name`
3. Commit your changes: `git commit -m 'Add some feature'`
4. Push to the branch: `git push origin feature-name`
5. Submit a pull request

## License

MIT
