# Research Assistant Project

## Project Functionality
1. **User Query Input**:
   - The application prompts the user to input a query (e.g., "What is the capital of France?").

2. **AI-Powered Research**:
   - The project uses two large language models (LLMs):
     - **OpenAI GPT-3.5 Turbo** (via `langchain-openai`).
     - **Anthropic Claude 3.5 Sonnet** (via `langchain-anthropic`).
   - These models process the query and generate responses.

3. **Tool Integration**:
   - The application integrates tools to enhance its capabilities:
     - **Search Tool**: Uses DuckDuckGo to find information online.
     - **Wikipedia Tool**: Fetches summarized information from Wikipedia.
     - **Save Tool**: Saves research outputs to a text file (`research_output.txt`) with a timestamp.

4. **Structured Output**:
   - The response is parsed into a structured format using Pydantic models, which includes:
     - Topic.
     - Summary.
     - Sources.
     - Tools used.

5. **Output Handling**:
   - The structured response is printed to the console.
   - If an error occurs during parsing, the raw response is displayed.

---

## Libraries Used
1. **`langchain`**:
   - A framework for building applications powered by large language models (LLMs).
   - Used for creating prompts, managing tools, and integrating LLMs.

2. **`langchain-openai`**:
   - Provides integration with OpenAI's GPT models.

3. **`langchain-anthropic`**:
   - Provides integration with Anthropic's Claude models.

4. **`langchain-community`**:
   - Includes community-contributed tools like `WikipediaQueryRun` and `DuckDuckGoSearchRun`.

5. **`wikipedia`**:
   - A Python library for interacting with Wikipedia's API.

6. **`duckduckgo-search`**:
   - A library for performing DuckDuckGo searches programmatically.

7. **`python-dotenv`**:
   - Loads environment variables from a `.env` file (e.g., API keys for OpenAI and Anthropic).

8. **`pydantic`**:
   - Used for data validation and parsing structured responses from the LLM.

---

## How It Works
1. **Environment Setup**:
   - API keys for OpenAI and Anthropic are loaded from the `.env` file.

2. **Agent Creation**:
   - A tool-calling agent is created using LangChain, combining the LLMs and tools.

3. **Query Execution**:
   - The agent processes the user query, invokes the necessary tools, and generates a response.

4. **Saving Results**:
   - The research output is saved to `research_output.txt` with a timestamp.

---


This project is designed to assist with research tasks by leveraging AI and external tools, making it a powerful assistant for gathering and summarizing information.