

2. The application will open in your default web browser.

3. Add content to your knowledge base:
   - Enter a website URL in the input field (e.g., `example.com` or `https://example.com`)
   - Click "Process URL"
   - The system will first try to find and process the sitemap at `/sitemap.xml`
   - If no sitemap is found, it will process the URL as a single page

4. Once content is loaded, you can:
   - Ask questions about the processed content in the chat interface
   - View statistics about your knowledge base
   - Clear the chat history or the entire database as needed

## System Architecture

- **UI Layer**: Streamlit web interface
- **RAG Components**:
  - Web Crawler: Extracts content from websites
  - Document Processing: Chunks and processes text
  - Vector Database: ChromaDB for storing embeddings
  - Retrieval System: Finds relevant content for queries
  - LLM Integration: OpenAI API for generating responses
- **Agent System**: Uses pydantic_ai_agent for structured interactions

## Examples

Try asking questions like:
- "What topics are covered in the knowledge base?"
- "Can you summarize the main content from [specific domain]?"
- "What are the key concepts discussed across these documents?"
- "Find information about [specific topic] from these sources"

## File Structure

- `ui.py`: Main Streamlit interface and application logic
- `db.py`: ChromaDB integration for vector database operations
- `crawler.py`: Website crawling and content extraction
- `pydantic_ai_agent.py`: Agent system for handling AI interactions

## Troubleshooting

- **URL Processing Issues**: Ensure URLs are properly formatted. The system will attempt to fix common issues.
- **No Content Found**: Some websites may block crawlers or have content protection measures.
- **Database Errors**: Use the "Clear Database" button to reset if you encounter issues.
- **API Rate Limits**: Be aware of OpenAI API rate limits when processing large volumes of content.

## License

[Insert License Information]

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.