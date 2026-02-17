# Agentcore Crash Course

A comprehensive project for building and managing AI agents using LangGraph and the AWS Bedrock AgentCore framework.

## 📋 Overview

This project demonstrates how to create intelligent agents with:
- **LangGraph Integration**: Build complex agent workflows and state management
- **Vector Search**: FAISS-based vector store for semantic search and retrieval
- **Multi-Model Support**: Integration with Groq LLMs, HuggingFace embeddings, and AWS Bedrock
- **FAQ Management**: Load and query frequently asked questions from CSV files
- **Runtime Management**: Agent state management and memory handling

## 🚀 Quick Start

### Prerequisites
- Python 3.13 or higher
- `uv` package manager ([install here](https://astral.sh/uv/install.sh))

### Installation

1. **Install UV** (if not already installed):
```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```

2. **Clone and setup the project**:
```bash
cd Agentcore
uv sync
```

3. **Add dependencies** (if needed):
```bash
uv add <package_name>
```

## 📁 Project Structure

```
Agentcore/
├── 00_langgraph_agent.py          # Main agent implementation using LangGraph
├── 01_agentcore_runtime.py        # Runtime management and orchestration
├── 02_agentcore_memory.py         # Memory and state management
├── lauki_qna.csv                  # FAQ dataset
├── pyproject.toml                 # Project configuration and dependencies
├── .env                           # Environment variables (not included in repo)
├── .gitignore                     # Git ignore rules
└── README.md                      # This file
```

## 🛠️ Core Components

### 00_langgraph_agent.py
Main agent implementation that:
- Loads FAQ data from CSV files
- Creates embeddings using HuggingFace
- Implements vector search with FAISS
- Integrates with Groq LLMs for agent responses

### 01_agentcore_runtime.py
Handles agent runtime and orchestration:
- Agent execution management
- State handling and transitions
- Tool execution

### 02_agentcore_memory.py
Manages agent memory and context:
- Conversation history
- State persistence
- Memory checkpoints

## 📦 Dependencies

Key dependencies include:
- `bedrock-agentcore>=1.0.7` - AWS Bedrock integration
- `langgraph>=1.0.4` - Workflow orchestration
- `langchain-groq>=1.1.0` - Groq LLM support
- `sentence-transformers>=5.1.2` - Text embeddings
- `faiss-cpu>=1.13.0` - Vector similarity search

See `pyproject.toml` for the complete dependency list.

## 🔑 Environment Variables

Create a `.env` file in the root directory with the following variables:

```env
# Groq API key (if using Groq)
GROQ_API_KEY=your_groq_api_key_here

# AWS credentials (if using Bedrock)
AWS_ACCESS_KEY_ID=your_aws_access_key
AWS_SECRET_ACCESS_KEY=your_aws_secret_key
AWS_REGION=us-east-1

# Other API keys as needed
```

**Note:** The `.env` file is not included in version control for security.

## 🎯 Usage

Run the agent:
```bash
uv run python 00_langgraph_agent.py
```

## 🤝 Contributing

1. Create a feature branch
2. Make your changes
3. Test thoroughly
4. Submit a pull request

## 📝 License

This project is part of the Agentcore crash course.

## 🙋 Support

For issues or questions related to:
- **LangGraph**: See [LangGraph Documentation](https://langchain-ai.github.io/langgraph/)
- **AWS Bedrock**: See [AWS Bedrock Documentation](https://docs.aws.amazon.com/bedrock/)
- **Groq**: See [Groq Documentation](https://console.groq.com/docs)

---

**Happy building! 🚀**
